
<h2>DNA Pairing</h2>

<p>The DNA strand is missing the pairing element. Take each character, get its pair, and return the results as a 2d array.</p>
<p>Base pairs are a pair of AT and CG. Match the missing element to the provided character.

Return the provided character as the first element in each array.</p>

<p>
<p>For example, for the input GCG, return [["G", "C"], ["C","G"],["G", "C"]]  

The character and its pair are paired up in an array, and all the arrays are grouped into one encapsulating array.</p>  
<ul>  
<li>pairElement("ATCGA") should return [["A","T"],["T","A"],["C","G"],["G","C"],["A","T"]].</li>
<li>pairElement("TTGAG") should return [["T","A"],["T","A"],["G","C"],["A","T"],["G","C"]].</li>
<li>pairElement("CTCTA") should return [["C","G"],["T","A"],["C","G"],["T","A"],["A","T"]].</li>
</ul>
</p><br/>
<p>======================================================</p>

  function pairElement(str) {  
  
  str=str.toUpperCase();  
  var newarray= [];  
  var strary = str.split("");  
		 var len=strary.length;  
		 for(var i=0;i<len;i++) 
		 {    
		   switch(strary[i])  
		   {  
		   case 'A':   
		          newarray.push(['A','T']);   
				  break;  
		   case 'C':   
                  newarray.push(['C','G']);  
				  break;  
		   case 'G':   
		          newarray.push(['G','C']);  
				  break;  
		   case 'T':   
		         newarray.push(['T','A']);  
				  break;  		  
		   }  
  
		 }
		 return newarray;  
}  
   
pairElement("GCG");  
