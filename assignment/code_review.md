Analyze the following React code snippet and suggest improvements:

```javascript
import React, { useState } from 'react';

function ProductList({ products, searchTerm }) {
  // Filter products that match the searchTerm
  const filteredProducts = products.filter(product =>
    product.name.toLowerCase().includes(searchTerm.toLowerCase())
  );
  
  // Calculate total stock of filtered products (an "expensive" computation placeholder)
  const totalStock = filteredProducts.reduce((acc, product) => acc + product.stock, 0);

  return (
    <div>
      <h2>Products</h2>
      {filteredProducts.map(p => (
        <div key={p.id}>
          <strong>{p.name}</strong>: {p.stock} in stock
        </div>
      ))}
      <p>Total Stock: {totalStock}</p>
    </div>
  );
}

function App() {
  const [searchTerm, setSearchTerm] = useState('');

  const products = [
    { id: 1, name: 'Laptop', stock: 5 },
    { id: 2, name: 'Keyboard', stock: 20 },
    { id: 3, name: 'Monitor', stock: 10 },
    { id: 4, name: 'Mouse', stock: 15 },
    { id: 5, name: 'Printer', stock: 2 },
    { id: N, name: 'Mac', stock: 3 }
  ];

  return (
    <div>
      <input 
        placeholder="Search products..." 
        value={searchTerm} 
        onChange={(e) => setSearchTerm(e.target.value)} 
      />
      <ProductList products={products} searchTerm={searchTerm} />
    </div>
  );
}

export default App;
