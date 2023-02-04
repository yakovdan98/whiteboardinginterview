# whiteboardinginterview
function turnToURL(str){
    const arr = str.split(" ");
    let output = "";
    for(let i = 0; i < arr.length;i++){
        output += arr[i];
        if(i < arr.length-1){
            output += "%20";
        }
    }
    return output;
}

function toURLRecursive(str){
    const arr = str.split(" ");
    return helper(arr, 0);
}

function helper(arr, index){
    if(index === arr.length - 1){
        return arr[index];
    }
    return arr[index] + "%20" + helper(arr, index + 1); 
    
}

console.log(turnToURL("Jasmine Ann Jones"));
console.log(toURLRecursive("Jasmine Ann Jones"));
