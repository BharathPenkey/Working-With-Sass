# Working-With-Sass
learning sass and building a ui with complete scss


saas
its an extension to css helps to write more flexible styles
use variables ,functions and conditional statements 
split our sass files into modules ,making it easy to keep on top of css for large projects

- when we write sass browsers will not understand it need to be tranlated into css
sass is written by ruby

you should know programming fundamentals and css


2 install and compile sass

dowload rubyinstaller and preprops.io  we should add files in the preprops .io i.e adding project and next if we save in .scss it automatically compiles and appears in css file which you have created 

sass -> in sass we dont use semi colons and curly braces 
scss ->  it is similar to normal css but we can use variables ,nesting and mixins ,functions ,for mixins you can pass variables as well

for dummy image you can do src="http://placehold.it/150x150"


//            variables 
variables  to store and used where they are needed 
we can do  // comment in sass
all varible proceed with $ sign

$deepBlue:#032f3e ; //  creation of variables 
background-color :$deepblue // using variables or calling variables

// 4         nested styles 

1 lesstime to create a styles 
2 keeps all your stand in a block

rule 

childs will be inside 

#main-nav {
    ul{

    }
}


above is equal to main-nav ul {

}


!important  nesting to deep is not prefered you may loose control 

main-nav ul li {}   like li nested inside ui

main-nav li {} li nested inside main-nav


but we should use clear fixings rule 


//    mixins 
// is a chunk of reusable or sass we inject 
instead of creating same things we can also pass a variables to mixins


lets create a single mixins for 2 banners (images)

how do we create a mixin 
@mixin mixinName {
    // code for css 
}

for import mixin
.classname{
    @include mixinName;
    @include mixinName()
}

@include mixinName(banner); (without parentheses):

This is used when the mixinName(banner) mixin doesn't accept any arguments. It's a straightforward inclusion of the mixin.
If your mixin doesn't have any parameters, you can use it without parentheses.
@include mixinName(banner)(); (with parentheses):

This is used when the mixinName(banner) mixin is defined with parameters (even if they are optional parameters with default values).
If your mixin accepts parameters, you need to use parentheses to indicate that you are invoking the mixin.
In your specific case, the mixinName(banner) mixin doesn't have any parameters, so both @include mixinName(banner); and @include mixinName(banner)(); will work the same way. The parentheses are optional when the mixin doesn't take any arguments.

It's good practice to include parentheses when calling mixins even if they don't have parameters. This makes your code consistent and prepares it for potential future changes where you might add parameters to the mixin.


//   6 importing files external

in scss folder create a different files for variables ,mixins and import all in style.scss file 

to import what comes first will import at top 
we import by @import "variables"; // dont need .scss as it checks and automatically import 


 makes nice and clean and update easily especially our files get bigger and bigger 

 
//7 pseudo classes 
  
  we should use & ampersand 
how we use in scss
main-nav a:hover{
    // normal css pseudo class
}

instead we write as in
 a tag {
     & :hover{
        background:#333
     }
}

and we can use &:after {//3 lines of code and we use every time so we can create a mixin as well}

//8       math operators

addition ,subtraction,multiplication,division 
width:(40px/2,40px*2,40px-20px)



// 9   grid with math sass  and also pass variables into mixins

for dummy images  src="http://placehold.it/150x150"    change the sizes as per requirement 


//10       colour   functions 

sass provides a tons of functions to make changes of our css or styles

functions link   https://sass-lang.com/documentation/modules/


lets see couple of functions to change the hover effects on some elements



// 11  content key word post the content 

while using mixin media quary  what ever the propeties we give that will  be taken by the content keyword which we declare in mixins media quary

// 12 if statements 
  some times media quaries will have min-width then we can not use above mixin so we 
  should have done based on conditions thats where this comes 

   (max-width: nth($args,1))  so 1 it  takes //500px
so above one takes 1st position value when we pass arguments i.e @include mQ(500px,4,9)
                                                                               1   2  3



// sass in react 

npm i sass