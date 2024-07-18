[][ Bee.js? ]
// open to name changes, just been saving JS-language considerations.

proposed JS quirks:
allPageArrays()                         prolly nevermind but maybe easier to start making new javascript methods by making the bad ones. 


Similarly? to how NextJS abstracts routing with pages folder
maybe  abstract modularization with a /functions folder. Maybe with <Context/> | <Native-Innovation> Leveraging main-file-root/paths 
<ContextProvider-Functions> 
commentFunctions: {        
        submitSoundCommentThought: (
            mapItemComment:any|null, commenterCanDetermineCheckboxCheckpointArray: any[],
            soundCommentFile:Blob|null, 
            newCommentThoughtsOk:string, newCommentStarrable:string, newCommentStarsShowAvg:boolean, newCommentStarsShowUsers:boolean 
) => any;

[BSS]/BEE-CSS
utility/tool stories:
* Allows {object} to define multiple :pseudo-classes (like on a button) --> :focus, :hover, :disabled       { hover: '', disabled: '' }
:engage -> style rules that invoke upon any activity-based-pseudo-class // that distinction leaves out -> ::before ::after?

The redundancy that led to this consideration can be seen below:
 :hover, :focus will have the same exact props/style-rules for either pseudoclass. 
they distinguish only by {cursor: pointer} considered an {.input} class but it has it's own similar rules that have to be changed. 
```
.input:hover{
    cursor: pointer;
    outline: none;
    border: 1px dashed $dedede;
    background-color: invisible;                                
    font-weight: bolder;
}

.input:focus{
    cursor: none;
    outline: none;
    border: 1px dashed $dedede;
    background-color: invisible;                                
    font-weight: bolder;
}
```

[non-opinionated-BLOB-accepting-native-global-state]
// seeing redux play soundfiles but with a "non-serializable-data" error // non-breaking


doWhile / useEffect seem like this but a do If() loop. nothing more specific past the name.  
do if([
        
])

 // lmaooo attempting-startup thoughts:
 some of us are "do if" people maybe we should be "do for" .... * thinks about any feasability in a do for loop lmao * 

LOLOLOLOLOL!! the Do-For Loop:
JS 2d-Matrix. Create array of arrays and it will execute a coding-statement, per array, till for block met (maybe) lol. 

// update: if it was modeled after the useEffect, a differentiating factor could be exportable/modularized useEffect()
