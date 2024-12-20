We will be hoping between different breakout rooms to assist you with your questions, check on you and move through diff rounds. 

The candidates are in different breakout rooms so they don't get disturbed by conversations with others. 

This interview round is split into two main sessions. 

(1)Live coding round:
    - Solve the question #1 and question #2 given below. 
    - Please keep your screen sharing turned on as you write the code.
  
(2) Verbal round: 
    - We will ask you certain questions to understand your coding fundamentals and debugging skills. 
    - One such code snippet is listed below (question #3). Review this code snippet. How would you make it better?

==================================================================================================================================

**Question #1 (coding):**

Create a simple Task Manager Application. Head over to the script.js file at the link and finish each of the six listed tasks. 

https://codesandbox.io/p/sandbox/task-manager-forked-s3fdqk?workspaceId=ws_ViJ1rbg6MKaud3LqCYmeHZ



**Question #2 (coding)**

Modify the sales table in your coding submission as follows:

- Desktop view:
    - The table should appear as a grid (you already did this in the submitted assignment)
    - Remove pagination and implement infinite scroll. Bonus points for virtual scroll
      
- Mobile view:
    - Each row of the table should appear as an individual card. Each card should have all the info contained in a row. 
    - Remove pagination and implement infinite scroll. Bonus points for virtual scroll



**Question #3 (review):**

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






If needed, as theortical question:
1. Create Reusable Accordian Component
2. What is the diff between 401 and 403 error. What is the diff between authorization and authentication?
3. API
   - Design APIs for Book My Show Dashboard page
  - Design APIs for Uber/Ola page (after the User have started ride)

