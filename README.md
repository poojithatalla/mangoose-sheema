# mangoose-sheema
const mongoose = require('mongoose');

// Define the Product schema
const productSchema = new mongoose.Schema({
    title: { type: String, required: true },
    price: { type: Number, required: true },
    category: { type: String, required: true },
    inStock: { type: Boolean, required: true }
});

// Create the Product model
const Product = mongoose.model('Product', productSchema);

// Export the model to use in other parts of the application
module.exports = Product;
