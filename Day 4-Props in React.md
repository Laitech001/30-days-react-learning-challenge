## What I Learned Today

# Props are properties we pass from a parent component to a child component to give it data.
They allow us to:
1. Reuse components with different data
2. Make components dynamic
3. Keep code clean and maintainable.

## Rules
1. Props always flow top → down
2. Child cannot send props back (use state or callbacks instead)
3. Use props to display data, text, numbers, images, or functions
4. When mapping arrays, always use key.

## my understanding!
props are like property that are waiting for a paticular value are they going to display.

## Real world example
# child component code
function ProductCard({ name, price, image }) {
  return (
    <div>
      <img src={image} alt={name} />
      <h2>{name}</h2>
      <p>₦{price}</p>
    </div>
  );
}
export default ProductCard;
this code above is the template that's waiting for a particular value.

# parent component code
import ProductCard from './productcard'
const products = [
  { id: 1, name: "iPhone 13", price: 750000, image: "iphone.jpg" },
  { id: 2, name: "Samsung S22", price: 680000, image: "samsung.jpg" }
];

function Shop() {
  return (
    <div>
      {products.map(product => (
        <ProductCard
          key={product.id}
          name={product.name}
          price={product.price}
          image={product.image}
        />
      ))}
    </div>
  );
}
the code above give value to the child component.

