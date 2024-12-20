# Wingman Coding Battleground Challenge

Welcome to the Wingman Coding Battleground Challenge for the Frontend Engineering Role. You will compete live with other candidates through live coding and verbal questions to win the role. 

Each candidate will be assigned a separate breakout room to ensure focused participation. The **Wingman team members** will hop between breakout rooms to answer your questions, provide real-time feedback, and guide you through the rounds/questions.

## Interview Structure

This interview is divided into two main rounds:

#### 1. Live Coding Round
- Solve Question #1 and Question #2 listed below.
- Share your screen while writing code. You may use any coding environment.

#### 2. Verbal Round
- We will evaluate your coding fundamentals and debugging skills.
- One such code snippet is listed below (Question #3). Review this code snippet and suggest improvements.

---

## Questions

### **Question #1: Task Manager Application**
Create a simple Task Manager Application by completing the six listed tasks in the linked `script.js` file. 

**Link to code sandbox:**  
[Task Manager Application](https://codesandbox.io/p/sandbox/task-manager-forked-s3fdqk?workspaceId=ws_ViJ1rbg6MKaud3LqCYmeHZ)

---

### **Question #2: Sales Table Modification**

Modify the sales table you created in the submitted dashboard assignment as follows:

#### Desktop View:
- The table should appear in a **grid layout**.  *(You already did it during your assignment.)*
- Remove pagination and implement **infinite scroll**. Bonus points for **virtual scroll**.

#### Mobile View:
- Display each table row as an **individual card**. Each card should include all the data from the row.
- Remove pagination and implement **infinite scroll**. Bonus points for **virtual scroll**.

---

### **Question #3: Code Review Task**

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
