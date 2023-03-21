# How to create and export modules

## Steps

    # Make a different js file where all module function present
    # after creating functions we have to export them
        ## Syntax:
        //Student.js
            const fnName=()=>{
                //......
                return ...something....
            }

            exports.<Any name> = <fnName>

        // index.js
            const varName = require("./Student.js")

            console.log(varName.<fnName>);

            // we can destructure module by simply write inside { } here
                We cant use varName if we do destructr=ure module

                const { getName } = require("./student");

                console.log(getName());//

## muliple export Syntax

    module.exports={
        funName1,
        funName2,
        funName3,
        ............

    }

Student.js
.................
const getName = () => {
return "Sanmay Paine";
};

const getAge = () => {
return 25;
};

const city = () => {
return "Basirhat";
};

module.exports = {
getName,
getAge,
city,
};

index.js
..........
const { getName } = require("./student");

console.log(getName());
