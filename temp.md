{"function": "function isPrime(number) {\n // Handle edge cases:\n if (number <= 1) return { isPrime: false, factors: []
    };\n if (number <=3) return { isPrime: true, factors: [] };\n if (number % 2===0 || number % 3===0) return {
    isPrime: false, factors: [2,3].filter(factor=> number % factor === 0) };\n\n // Optimized primality test:\n for (let
    i = 5; i * i <= number; i +=6) {\n if (number % i===0 || number % (i + 2)===0) {\n let factors=[];\n for (let j=2; j
        <=number; j++) {\n if (number % j===0) {\n factors.push(j);\n }\n }\n return { isPrime: false, factors: factors
        };\n }\n }\n\n return { isPrime: true, factors: [] };\n}", "exampleUsage"
        : "console.log(isPrime(2)); // Output: { isPrime: true, factors: [] }\nconsole.log(isPrime(15)); // Output: { isPrime: false, factors: [3, 5] }\nconsole.log(isPrime(97)); // Output: { isPrime: true, factors: [] }\nconsole.log(isPrime(100)); // Output: { isPrime: false, factors: [2, 2, 5, 5] }"
        }