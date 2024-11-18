# numbersystem.
This project demonstrates basic operations on arrays using JavaScript. It includes:

Separating even and odd numbers from an array.
Extracting prime numbers from an array and calculating their maximum, minimum, and sum.
The code is divided into two files:

index.js: Handles the even and odd number separation.
app.js: Handles prime number identification, maximum, minimum, and sum calculations.

const numbers = [
[ 3, 7, 2, 15, 9, 20, 5, 14, 12, 1, 8, 11, 6, 19, 4, 10, 17, 13, 16, 18,
]

const evenNumbers = [];
const oddNumbers = [];

for (let i = 0; i < numbers.length; i++) {
  if (numbers[i] % 2 === 0) {
    evenNumbers.push(numbers[i]);
  } else {
    oddNumbers.push(numbers[i]);
  }
}

console.log("Even Numbers:", evenNumbers);
console.log("Odd Numbers:", oddNumbers);


const numbers = [
  19, 23, 4, 16, 28, 13, 31, 8, 29, 14, 6, 35, 2, 11, 17, 5, 9, 27, 12, 30,
];

// Function to check if a number is prime
const isPrime = (num) => {
  if (num < 2) return false;
  for (let i = 2; i <= Math.sqrt(num); i++) {
    if (num % i === 0) return false;
  }
  return true;
};

// Create an array of prime numbers
const primeArray = [];
for (let i = 0; i < numbers.length; i++) {
  if (isPrime(numbers[i])) {
    primeArray.push(numbers[i]);
  }
}

// Find maximum, minimum, and sum
const maxPrime = Math.max(...primeArray);
const minPrime = Math.min(...primeArray);
const sumPrimes = primeArray.reduce((sum, num) => sum + num, 0);

console.log("Prime Numbers:", primeArray);
console.log("Maximum Prime:", maxPrime);
console.log("Minimum Prime:", minPrime);
console.log("Sum of Primes:", sumPrimes);
