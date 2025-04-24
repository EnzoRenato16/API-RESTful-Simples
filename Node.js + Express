const express = require('express');
const app = express();
const port = 3000;

const usuarios = [
  { id: 1, nome: 'João', idade: 22 },
  { id: 2, nome: 'Maria', idade: 28 },
  { id: 3, nome: 'José', idade: 30 }
];

app.get('/usuarios', (req, res) => {
  res.json(usuarios);
});

app.get('/usuarios/:id', (req, res) => {
  const usuario = usuarios.find(u => u.id === parseInt(req.params.id));
  if (!usuario) return res.status(404).send('Usuário não encontrado.');
  res.json(usuario);
});

app.listen(port, () => {
  console.log(`API rodando em http://localhost:${port}`);
});Node.js + Express
