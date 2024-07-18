a useEffect like tool that would allow distincting between running on load or running when dependency array is mutated

TL;Dr:
invalid dependency array definition:

},[] || [CURR_DAY_STARS])`

#### me:
so there would be no way to:
only run when {CURR_DAY_STARS] updates
NOT also on load?`
... no

#### me:
` 
chat will dependency array with logical || like below:
run during componentLoad
& run during array update

useEffect(() => {

},[] || [CURR_DAY_STARS])`

#### ChatGPT
In React, the useEffect hook takes a dependency array as its second argument. The effect runs:

After the initial render (component load).
Whenever any of the values in the dependency array change.
Using a logical OR (||) inside the dependency array is not valid syntax. The dependency array should directly list the dependencies. If you want the effect to run when either the component loads or a specific dependency (CURR_DAY_STARS) changes, you should just include that dependency in the array.

Here’s how you can set it up:
{...}
export default SomeComponent;
This setup ensures that the effect runs both when the component is first loaded and whenever CURR_DAY_STARS is updated.

`#### me:
so there would be no way to:
only run when [CURR_DAY_STARS] updates
NOT also on load?``

#### ChatGPT
To achieve the behavior where an effect only runs when a dependency updates and not on the initial load, you need to implement a workaround, as React's useEffect will always run on the initial render regardless of how the dependency array is set.

Here's one common approach:

Track the First Render: Use a state variable to keep track of whether the component has been rendered for the first time.
Conditionally Run the Effect: Use this state to conditionally run the effect logic only when the dependency changes after the first render.
Here's how you can implement this:

javascript
{...}
Explanation:
useRef: The hasRendered ref is used to track whether the component has completed its initial render. Unlike state, changing a ref does not trigger a re-render.
Effect Logic: Inside the useEffect, you check hasRendered.current. On the initial render, hasRendered.current will be false, so the effect will skip its logic. After the initial render, hasRendered.current will be set to true, allowing the effect to run on subsequent updates to CURR_DAY_STARS.
With this approach, the effect runs only when CURR_DAY_STARS changes after the initial render.
