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
