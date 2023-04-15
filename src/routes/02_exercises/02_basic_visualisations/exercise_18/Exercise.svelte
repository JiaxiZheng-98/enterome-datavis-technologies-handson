

<script>
  import {scaleLog} from 'd3-scale';
  import {axisBottom} from 'd3-axis';
  import {select} from 'd3-selection';

    // Dimensions
    const width = 800;
    const height = 100;
    const margin = { top: 5, right: 5, bottom: 5, left: 5 };
    const innerWidth = width - margin.left - margin.right;
    const innerHeight = height - margin.top - margin.bottom;
  
    // Array
    const values = [2, 4, 6, 7, 9];
    const scale = scaleLog().
                domain([2, 9])
                .range([30, 500]);
    
    
    
  let xAxis;
	$: {
		select(xAxis).call(axisBottom(scale));
	}

  </script>
  
  <svg viewBox="0 0 {width} {height}">
      {#each values as value}
      <circle cx={scale(value)}
              cy={value}
              r=20
              fill="red" />
      {/each}

    <g transform="translate(0, 80)"
		 bind:this={xAxis}>
        <text  x=250  y=20 fill="currentcolor">x Axis</text>
    </g>

  </svg>

