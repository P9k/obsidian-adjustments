# obsidian-adjustments
A collection of code (snippets) to customize the [Obsidian note-taking app](https://obsidian.md/)

# Mermaid diagrams
Customize the look of Gantt charts generated with the built-in [Mermaid functionality](https://mermaid-js.github.io/mermaid/#/gantt) of Obsidian

### Gantt.css
This CSS snippet generates a custom look for Gantt charts that focuses on high readability in combination with the [Cybertron Theme](https://github.com/nickmilo/Cybertron)

Installation is pretty simple:

- Put `Gantt.css` into the `snippets`-directory under `.obsidian` 
- Activate **CSS snippet** under Obsidian's **Settings** -> **Appearance**

This is what the theme outputs in Obsidian:

![alt text](https://github.com/P9k/obsidian-adjustments/blob/main/Gantt-Example.png?raw=true)


### Example code for Gantt chart with more spacing for section labels

The default settings for the left padding (i.e. the spacing for the section labels) is `75px`. 

This example illustrates how the spacing can be enlarged by increasing the value for `leftPadding` while intiliazing the Mermaid code in Obsidian:

````
```mermaid
%%{init:  {"gantt": {"leftPadding": 100 }  } }%%
gantt
	title Test-Gantt
	dateFormat  YYYY-MM
    axisFormat %m/%y
	
	section First Section
	A task : done,  2022-01, 2022-03
	Another task : active, 2022-03, 2022-06
	My milestone M1 :milestone, m1, 2022-04, 10d
	
	section Another
	Task in sec : done, crit, 2022-04, 2022-06
	another task : 2022-06, 2022-07

	section Bnother
	Pretty Task : active, 2022-03 , 2022-06
	another task : active, crit, 2022-06, 2022-07
	
	section Cnother
	Pretty Task : crit, 2022-03 , 2022-06
	another task : 2022-06, 2022-07

	section Dnother
	Pretty Task : 2022-03 , 2022-06
	another task : 2022-06, 2022-07
	
	section Enother
	Pretty Task : 2022-03 , 2022-06
	another task : 2022-06, 2022-07
	
	section Fnother
	Pretty Task : 2022-03 , 2022-06
	another task : 2022-06, 2022-07
	
	section Gnother
	Pretty Task : 2022-03 , 2022-06
	another task : 2022-06, 2022-07
```
````
