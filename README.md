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