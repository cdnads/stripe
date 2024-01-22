const express = require('express');
const fetch = require('node-fetch');

const app = express();
const PORT = process.env.PORT || 3000;

app.get('/fetch-content/', async (req, res) => {
  const { productId } = req.params;
  try {
    const response = await fetch(`https://bricaree.com/asp-payment-box/?product_id=2862&refresh=1705872924769`);
    const data = await response.text();
    res.send(data);
  } catch (error) {
    console.error('Error fetching data:', error);
    res.status(500).send('Internal Server Error');
  }
});

app.listen(PORT, () => {
  console.log(`Server is running on http://localhost:${PORT}`);
});
