# Total-Shopping-Cart
let cart = [
  { item: "Phone", price: 700, quantity: 1 },
  { item: "Headphones", price: 150, quantity: 2 },
  { item: "Charger", price: 30, quantity: 1 }
];

const check = cart.every((item, price) => {
  console.log(item.price > 50);
});
console.log("Not all items are over 50$");

const check2 = cart.some((item, price) => {
console.log(`${item.price}` < 500);
});
console.log("Some items are over 500$");

let total = cart.reduce((sum, item) => {
   return sum + (item.price * item.quantity);
 }, 0);
 console.log("total:", total);

 if(total > 1000) {
   total = total * 0.9;
   console.log("Discount applied! Your total is", total);
 } else {
   console.log("No discount applied");
 }
