### JavaScript to create course outline
	- ```javascript
	  function directChildText(node, sep) {
	    return Array.from(node.childNodes)
	      .filter(node => node.nodeType == node.TEXT_NODE)
	      .map(node => node.nodeValue.trim())
	      .join(sep || '')
	  }
	  function parseMinutes(duration) {
	    const [minutes, seconds] = duration.split(':').map(Number);
	    return minutes + seconds / 60;
	  }
	  function formatTime(totalMinutes) {
	    const hours = Math.floor(totalMinutes / 60);
	    const minutes = Math.floor(totalMinutes % 60);
	    const seconds = Math.round((totalMinutes % 1) * 60);
	    const format = n => String(n).padStart(2, '0');
	  
	    return `${format(hours)}:${format(minutes)}:${format(seconds)}`;
	  }
	  
	  sections = Array.from(document.querySelectorAll('.course-section'))
	    .map(section => {
	      const title = directChildText(section.querySelector('.section-title'));
	      const totalTime = Array.from(section.querySelectorAll('.section-item a.item'))
	        .map(item => directChildText(item).match(/\((?<duration>\d+:\d+)\)/))
	        .filter(match => match !== null)
	        .map(match => parseMinutes(match.groups.duration))
	        .reduce((x, y) => x + y, 0);
	      return {title, totalTime};
	    });
	  
	  console.log(`Total duration: ${formatTime(sections.reduce((acc, s) => acc + s.totalTime, 0))}`)
	  console.log(sections.map(s => `### ${s.title} (${formatTime(s.totalTime)})`).join('\n'))
	  ```