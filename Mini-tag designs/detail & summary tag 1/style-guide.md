ICON

/* Adds an icon when the <details> is closed... */
details > summary::after {
    content: "+"; 
}


/* ...and switches it when <details> is open */
details[open] > summary::after {
    content: "-";
}




WORKING SOLUTION to remove the default arrow;

FIRST

details > summary {
    list-style: none;
}

details > summary::-webkit-details-marker {
    display: none;
}



SECOND

::marker { 
    display:none; 
} 

summary { 
    list-style: none; 
}




THIRD

details > summary {display:block} 



FOURTH

details > summary {
    list-style: none;
}
  
details > summary::marker, /* Latest Chrome, Edge, Firefox */ 
details > summary::-webkit-details-marker /* Safari */ {
    display: none;
}