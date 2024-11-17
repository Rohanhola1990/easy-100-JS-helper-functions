# 100 easy JS helper functions

| **#** | **Description** | **Function** |
| --- | --- | --- |
| 1. | Remove duplicates from an array | `const removeDuplicates = arr => [...new Set(arr)];` |
| 2. | Check if a number is even | `const isEven = num => num % 2 === 0;` |
| 3. | Find the maximum number in an array | `const findMax = arr => Math.max(...arr);` |
| 4. | Reverse a string | `const reverseString = str => str.split('').reverse().join('');` |
| 5. | Capitalize the first letter of a string | `const capitalize = str => str.charAt(0).toUpperCase() + str.slice(1);` |
| 6. | Generate a random number between two values | `const randomBetween = (min, max) => Math.random() * (max - min) + min;` |
| 7. | Check if a string is a palindrome | `const isPalindrome = str => str === str.split('').reverse().join('');` |
| 8. | Convert a string to camelCase | `const toCamelCase = str => str.replace(/([-_][a-z])/g, group => group.toUpperCase().replace('-', '').replace('_', ''));` |
| 9. | Flatten a nested array | `const flattenArray = arr => arr.flat(Infinity);` |
| 10. | Get the current timestamp | `const getTimestamp = () => Date.now();` |
| 11. | Convert an object to a query string | `const toQueryString = obj => Object.entries(obj).map(([key, val]) => \`\${key}=\${val}\`).join('&');` |
| 12. | Debounce a function | `const debounce = (func, delay) => { let timer; return (...args) => { clearTimeout(timer); timer = setTimeout(() => func(...args), delay); }; };` |
| 13. | Throttle a function | `const throttle = (func, limit) => { let lastFunc; let lastRan; return function(...args) { if (!lastRan) { func(...args); lastRan = Date.now(); } else { clearTimeout(lastFunc); lastFunc = setTimeout(() => { if ((Date.now() - lastRan) >= limit) { func(...args); lastRan = Date.now(); } }, limit - (Date.now() - lastRan)); } }; };` |
| 14. | Get a random element from an array | `const randomElement = arr => arr[Math.floor(Math.random() * arr.length)];` |
| 15. | Count occurrences of elements in an array | `const countOccurrences = arr => arr.reduce((acc, curr) => (acc[curr] = ++acc[curr] || 1, acc), {});` |
| 16. | Check if two arrays are equal | `const arraysEqual = (arr1, arr2) => JSON.stringify(arr1) === JSON.stringify(arr2);` |
| 17. | Shuffle an array | `const shuffleArray = arr => arr.sort(() => Math.random() - 0.5);` |
| 18. | Convert RGB to Hex | `const rgbToHex = (r, g, b) => "#" + [r, g, b].map(x => x.toString(16).padStart(2, "0")).join("");` |
| 19. | Convert Hex to RGB | `const hexToRgb = hex => { const bigint = parseInt(hex.slice(1), 16); return [bigint >> 16 & 255, bigint >> 8 & 255, bigint & 255]; };` |
| 20. | Check if a value is an object | `const isObject = val => val && typeof val === 'object' && !Array.isArray(val);` |
| 21. | Deep clone an object | `const deepClone = obj => JSON.parse(JSON.stringify(obj));` |
| 22. | Merge two objects | `const mergeObjects = (obj1, obj2) => ({ ...obj1, ...obj2 });` |
| 23. | Check if an object is empty | `const isEmptyObject = obj => Object.keys(obj).length === 0;` |
| 24. | Capitalize the first letter of a string | `const capitalize = str => str.charAt(0).toUpperCase() + str.slice(1);` |
| 25. | Reverse a string | `const reverseString = str => str.split('').reverse().join('');` |
| 26. | Count vowels in a string | `const countVowels = str => (str.match(/[aeiou]/gi) || []).length;` |
| 27. | Generate a random string | `const randomString = length => Math.random().toString(36).substr(2, length);` |
| 28. | Check if a string is a palindrome | `const isPalindrome = str => { const cleaned = str.toLowerCase().replace(/[^a-z]/g, ''); return cleaned === cleaned.split('').reverse().join(''); };` |
| 29. | Flatten a nested array | `const flattenArray = arr => arr.reduce((acc, val) => acc.concat(Array.isArray(val) ? flattenArray(val) : val), []);` |
| 30. | Get unique values from an array | `const uniqueValues = arr => [...new Set(arr)];` |
| 31. | Get the max value in an array | `const maxInArray = arr => Math.max(...arr);` |
| 32. | Get the min value in an array | `const minInArray = arr => Math.min(...arr);` |
| 33. | Remove falsy values from an array | `const removeFalsy = arr => arr.filter(Boolean);` |
| 34. | Generate a range of numbers | `const range = (start, end) => Array.from({ length: end - start + 1 }, (_, i) => start + i);` |
| 35. | Chunk an array | `const chunkArray = (arr, size) => { const result = []; for (let i = 0; i < arr.length; i += size) { result.push(arr.slice(i, i + size)); } return result; };` |
| 36. | Find the intersection of two arrays | `const intersectArrays = (arr1, arr2) => arr1.filter(val => arr2.includes(val));` |
| 37. | Find the difference between two arrays | `const diffArrays = (arr1, arr2) => arr1.filter(val => !arr2.includes(val));` |
| 38. | Get the current timestamp | `const currentTimestamp = () => Date.now();` |
| 39. | Format a date to `YYYY-MM-DD` | `const formatDate = date => date.toISOString().split('T')[0];` |
| 40. | Check if a year is a leap year | `const isLeapYear = year => year % 4 === 0 && (year % 100 !== 0 || year % 400 === 0);` |
| 41. | Calculate the factorial of a number | `const factorial = n => (n <= 1 ? 1 : n * factorial(n - 1));` |
| 42. | Find the Fibonacci sequence up to `n` | `const fibonacci = n => { const seq = [0, 1]; for (let i = 2; i < n; i++) { seq.push(seq[i - 1] + seq[i - 2]); } return seq; };` |
| 43. | Check if a number is prime | `const isPrime = num => { if (num <= 1) return false; for (let i = 2; i <= Math.sqrt(num); i++) { if (num % i === 0) return false; } return true; };` |
| 44. | Find the greatest common divisor (GCD) | `const gcd = (a, b) => (!b ? a : gcd(b, a % b));` |
| 45. | Find the least common multiple (LCM) | `const lcm = (a, b) => (a * b) / gcd(a, b);` |
| 46. | Round a number to `n` decimal places | `const roundTo = (num, decimals) => Number(Math.round(num + 'e' + decimals) + 'e-' + decimals);` |
| 47. | Convert degrees to radians | `const degreesToRadians = degrees => (degrees * Math.PI) / 180;` |
| 48. | Convert radians to degrees | `const radiansToDegrees = radians => (radians * 180) / Math.PI;` |
| 49. | Generate a random number within a range | `const randomInRange = (min, max) => Math.random() * (max - min) + min;` |
| 50. | Shuffle an array | `const shuffleArray = arr => arr.sort(() => Math.random() - 0.5);` |
| 51. | Calculate the sum of an array | `const sumArray = arr => arr.reduce((sum, num) => sum + num, 0);` |
| 52. | Calculate the average of an array | `const averageArray = arr => sumArray(arr) / arr.length;` |
| 53. | Find the median of an array | `const median = arr => { const sorted = [...arr].sort((a, b) => a - b); const mid = Math.floor(sorted.length / 2); return sorted.length % 2 === 0 ? (sorted[mid - 1] + sorted[mid]) / 2 : sorted[mid]; };` |
| 54. | Find the mode of an array | `const mode = arr => { const freq = {}; arr.forEach(num => (freq[num] = (freq[num] || 0) + 1)); const maxFreq = Math.max(...Object.values(freq)); return Object.keys(freq).filter(key => freq[key] === maxFreq); };` |
| 55. | Flatten a deeply nested array | `const deepFlatten = arr => arr.reduce((acc, val) => acc.concat(Array.isArray(val) ? deepFlatten(val) : val), []);` |
| 56. | Remove duplicates in a nested array | `const uniqueNested = arr => deepFlatten(arr).filter((val, i, self) => self.indexOf(val) === i);` |
| 57. | Convert a string to camel case | `const toCamelCase = str => str.replace(/([-_][a-z])/gi, group => group.toUpperCase().replace('-', '').replace('_', ''));` |
| 58. | Convert a string to kebab case | `const toKebabCase = str => str.replace(/\s+/g, '-').toLowerCase();` |
| 59. | Convert a string to snake case | `const toSnakeCase = str => str.replace(/\s+/g, '_').toLowerCase();` |
| 60. | Get the first `n` elements of an array | `const firstN = (arr, n) => arr.slice(0, n);` |
| 61. | Get the last `n` elements of an array | `const lastN = (arr, n) => arr.slice(-n);` |
| 62. | Count occurrences of a value in an array | `const countOccurrences = (arr, val) => arr.reduce((count, el) => (el === val ? count + 1 : count), 0);` |
| 63. | Find the longest word in a string | `const longestWord = str => str.split(' ').reduce((longest, word) => (word.length > longest.length ? word : longest), '');` |
| 64. | Reverse a string | `const reverseString = str => str.split('').reverse().join('');` |
| 65. | Capitalize the first letter of each word in a string | `const capitalizeWords = str => str.replace(/\b\w/g, char => char.toUpperCase());` |
| 66. | Remove falsy values from an array | `const removeFalsy = arr => arr.filter(Boolean);` |
| 67. | Find unique values in two arrays | `const uniqueValues = (arr1, arr2) => [...new Set([...arr1, ...arr2])];` |
| 68. | Find common values in two arrays | `const commonValues = (arr1, arr2) => arr1.filter(val => arr2.includes(val));` |
| 69. | Generate a random hexadecimal color code | `const randomHexColor = () => '#' + Math.floor(Math.random() * 16777215).toString(16);` |
| 70. | Generate an array of `n` random numbers within a range | `const randomArray = (n, min, max) => Array.from({ length: n }, () => randomInRange(min, max));` |
| 71. | Convert a string to title case | `const toTitleCase = str => str.toLowerCase().replace(/\b\w/g, char => char.toUpperCase());` |
| 72. | Check if an array is sorted | `const isSorted = arr => arr.every((val, i, a) => !i || a[i - 1] <= val);` |
| 73. | Convert an object to an array of key-value pairs | `const objectToArray = obj => Object.entries(obj);` |
| 74. | Convert an array of key-value pairs to an object | `const arrayToObject = arr => Object.fromEntries(arr);` |
| 75. | Check if an object is empty | `const isEmptyObject = obj => Object.keys(obj).length === 0;` |
| 76. | Deep clone an object or array | `const deepClone = obj => JSON.parse(JSON.stringify(obj));` |
| 77. | Merge two objects | `const mergeObjects = (obj1, obj2) => ({ ...obj1, ...obj2 });` |
| 78. | Find the intersection of multiple arrays | `const intersectArrays = (...arrays) => arrays.reduce((acc, arr) => acc.filter(val => arr.includes(val)));` |
| 79. | Find the union of multiple arrays | `const unionArrays = (...arrays) => [...new Set(arrays.flat())];` |
| 80. | Get the difference between two arrays | `const difference = (arr1, arr2) => arr1.filter(val => !arr2.includes(val));` |
| 81. | Check if a string contains a specific substring | `const containsSubstring = (str, sub) => str.includes(sub);` |
| 82. | Get the average of numbers in an array | `const average = arr => arr.reduce((sum, num) => sum + num, 0) / arr.length;` |
| 83. | Remove leading and trailing whitespace from a string | `const trimWhitespace = str => str.trim();` |
| 84. | Check if a string starts with a given substring | `const startsWith = (str, prefix) => str.startsWith(prefix);` |
| 85. | Check if a string ends with a given substring | `const endsWith = (str, suffix) => str.endsWith(suffix);` |
| 86. | Remove a specific element from an array | `const removeElement = (arr, elem) => arr.filter(item => item !== elem);` |
| 87. | Create a deep comparison between two objects | `const deepEqual = (obj1, obj2) => JSON.stringify(obj1) === JSON.stringify(obj2);` |
| 88. | Flatten an array of arrays | `const flattenArray = arr => arr.flat();` |
| 89. | Check if a number is prime | `const isPrime = num => num > 1 && [...Array(num).keys()].slice(2).every(i => num % i !== 0);` |
| 90. | Create a debounced function | `const debounce = (func, delay) => { let timeout; return (...args) => { clearTimeout(timeout); timeout = setTimeout(() => func(...args), delay); }; };` |
| 91. | Create a throttled function | `const throttle = (func, limit) => { let lastFunc; let lastRan; return (...args) => { if (!lastRan) { func(...args); lastRan = Date.now(); } else { clearTimeout(lastFunc); lastFunc = setTimeout(() => { if (Date.now() - lastRan >= limit) { func(...args); lastRan = Date.now(); } }, limit - (Date.now() - lastRan)); } }; };` |
| 92. | Find the maximum value in an array | `const maxValue = arr => Math.max(...arr);` |
| 93. | Find the minimum value in an array | `const minValue = arr => Math.min(...arr);` |
| 94. | Generate a random string of a specified length | `const randomString = len => Array(len).fill().map(() => String.fromCharCode(Math.floor(Math.random() * 26) + 97)).join('');` |
| 95. | Check if an array contains a specific value | `const includesValue = (arr, value) => arr.includes(value);` |
| 96. | Create a unique identifier (UUID) | `const generateUUID = () => ([1e7] + -1e3 + -4e3 + -8e3 + -1e11).replace(/[018]/g, c => (c ^ crypto.getRandomValues(new Uint8Array(1))[0] & 15 >> c / 4).toString(16));` |
| 97. | Get the query string from a URL | `const getQueryString = url => new URL(url).search;` |
| 98. | Get a specific query parameter value from a URL | `const getQueryParam = (url, param) => new URL(url).searchParams.get(param);` |
| 99. | Convert a query string to an object | `const queryToObject = query => Object.fromEntries(new URLSearchParams(query));` |
| 100. | Convert an object to a query string | `const objectToQuery = obj => new URLSearchParams(obj).toString();` |
