const express = require("express");
const app = express();

// Load translation service
const Translation = require("./services/translation");
Translation.loadLanguages();

// Serve static files from the "static" folder
app.use(express.static("static"));

// Set up Pug as the view engine
app.set("view engine", "pug");
app.set("views", "views");

// Import routes
const api = require("./routes/api");
const frontend = require("./routes/frontend");

// Use routes
app.use("/api", api);
app.use(frontend);

// Start the server
app.listen(3000, () => {
  console.info("App gestartet auf Port: 3000");
});
