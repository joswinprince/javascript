## Java script examples

### Depth first search
```
const depthfirstprint = (graph,source) => {
const stack = [source];
console.log(source+" - source");
while(stack.length > 0)
{
    const current = stack.pop();
    console.log(current);
    for(let neighbor of graph[current])
{
    stack.push(neighbor);
}
}
};

const graph = {
    a:['c','b'],
    b:['d'],
    c:['e'],
    d:['f'],
    e:[],
    f:[]

};
depthfirstprint(graph,'d'); // expected [a,b,d,f,c,e]
```
