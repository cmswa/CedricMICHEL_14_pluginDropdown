# React simple dropdown

## Install

```bash
npm i cm_plugin_dropdown --save
```

## Example

The dropdown takes two params : 

### list
This is the list of elements that you want in the dropdown

### setValue
This is the function you want to trigger when an element is choose 

```jsx
import React from 'react';
import { Dropdown } from 'cm_plugin_dropdown';
import 'cm_plugin_dropdown/dist/index.css';

/**
	* @param {array} list Element array
	* @param {fonction} setValue Fonction
	*/
function departementsDropdown() {

    //retrieval and storage of the value of the chosen element in the dropdown
    const [department, setDepartment] = useState('')

    //each time the dropdown value changes, a console.log with the new value will be displayed
    useEffect(() => {
        console.log("You chose "+department+"!");
    }, [department])

    //list of departments that will appear in the dropdown
    const departmentsNames = ['Sales', 'Marketing', 'Engineering', 'Human Ressources', 'Legal']

    return (
        <Dropdown list={departmentsNames} setValue={setDepartment} />
    )
}

export default departementsDropdown
