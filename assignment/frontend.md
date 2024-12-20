Welcome to the coding battleground challenge. You will compete with other candidates live through a series of live coding and verbal questions. 

Each candidate will be assigned a separate breakout room to avoid unwanted chatter. The Wingman team members will be hopping between different breakout rooms 
to help answer any questions, provide real-time feedback, and move you through the rounds/questions. 

This interview is split into two main rounds: 

(1) Live coding round
    - Solve the question #1 and question #2 given below. 
    - Please share your screen as you write the code. You can choose any coding environment. 
  
(2) Verbal round 
    - We will ask questions to understand your coding fundamentals and debugging skills. 
    - One such code snippet is listed below (question #3). Review this code snippet and suggest how you would make it better.

==================================================================================================

**Question #1 (live coding):**

Create a simple Task Manager Application. Head over to the script.js file at the link and finish each of the six listed tasks. 

https://codesandbox.io/p/sandbox/task-manager-forked-s3fdqk?workspaceId=ws_ViJ1rbg6MKaud3LqCYmeHZ



**Question #2 (live coding)**

Modify the sales table in your coding submission as follows:

- Desktop view:
    - The table should appear as a grid (you already did this in the submitted assignment)
    - Remove pagination and implement infinite scroll. Bonus points for virtual scroll
      
- Mobile view:
    - Each row of the table should appear as an individual card. Each card should have all the info contained in a row. 
    - Remove pagination and implement infinite scroll. Bonus points for virtual scroll



**Question #3 (verbal review):**

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
   {id: N, name: ‘Mac’, stock: 3}
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
```


