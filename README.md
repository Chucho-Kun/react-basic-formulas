# react-basic-formulas
React Basic Formulas

const [ cart , useCart ] = useState({})

useEffect( () => {
  
},[])

## Sorting an array by date (string)

```
  const handleMostUpvoted = () => {
    setArticulos( prev => [...prev].sort( (a,b)=> b.upvotes -a.upvotes ) )
  }

  const handleMostRecent = () => {
    const nuevos = articulos.map( art => ({
      ...art , fecha: new Date(art.date)
    }) )
    setArticulos( nuevos.sort( (a,b) => b.fecha - a.fecha ) )
  };
```
## Handle Errors
```
  const errorChecks = [
  [(amount) => !amount, "Amount cannot be empty"],
  [(amount) => amount < 0.01, "Amount cannot be less than $0.01"],
  [(amount) => amount > maxAmount, "Amount cannot exceed the available balance"],
]

  const handleAmount = (e) => {
    const valor = e.target.value
    setAmount( valor )
    const error = errorChecks.find(([condition]) => condition(+e.target.value))
    setErrorMessage(!error ? '' : error[1])
  }
```
```
 <td>{!amount ? `0.00000000` : errorMessage ? 'n/a' : `${(amount * coin.rate).toFixed(8)}`}</td>
```
