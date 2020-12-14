---
title: CodeNation - Week 6
date: "2020-12-12T15:28:03.284Z"
description: "React"
---

##React

Week-6 saw the beginning of a bit of an addiction to React. Seeing how powerful it is as a web development tool and the potential is has had me a little bit in awe.

I was most amazed by the posibility of being able to create a component that can be used multiple times.

```javascript
import React from 'react';
import './ProjectCard.css';

export const ProjectCard = (props) => {
    return (
        <div className="project">
            <div className="img-container">
                <img src={props.image} alt={props.altText}>
                </img>
            </div>
            <div className="description">
                <h3>
                    {props.header}
                </h3>
                <p>
                    {props.details}
                </p>
            </div>
        </div>
    );
};
```
Then using a state which in this case has data hardcoded into an array of objects. (You could use an API).

```javascript
let[projects] = useState([{name:"Gatsby Blog", 
                            desc:"Check out my gastby Blog!", 
                            alt:"gatsby", 
                            img:Gatsby},
                        {name:"Follow me on Twitter!", 
                            desc:"See who I'm connecting with!", 
                            alt:"twitter", 
                            img:Twitter},
                        {name:"Find me on Facebook", 
                            desc:"See what my upcoming projects are",
                            alt:"facebook",
                            img:Facebook}]);
```
Which can then be iterated over using built in JavaScript functions to programitically display that content.

```jsx
{projects.map((project) => {
        return(
          <ProjectCard image={project.img} 
          altText={project.alt} 
          header={project.name} 
          details={project.desc}/>
        )
      })}
```

Giving you a simple way to display multiple of the same component with varying types of data passed through via props.

![](./react-components.png)
