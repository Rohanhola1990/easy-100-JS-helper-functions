** 1. Remove duplicates from an array **
const removeDuplicates = arr => [...new Set(arr)];

** 2. Chunk an array into smaller arrays **
const chunkArray = (arr, size) => arr.reduce((acc, _, i) => (i % size ? acc : [...acc, arr.slice(i, i + size)]), []);

** 3. Flatten a nested array **
const flattenArray = arr => arr.flat(Infinity);

** 4. Shuffle elements in an array **
const shuffleArray = arr => arr.sort(() => Math.random() - 0.5);

** 5. Find duplicates in an array **
const findDuplicates = arr => arr.filter((item, index) => arr.indexOf(item) !== index);

** 6. Get the intersection of two arrays **
const arrayIntersection = (arr1, arr2) => arr1.filter(item => arr2.includes(item));

** 7. Get the difference of two arrays **
const arrayDifference = (arr1, arr2) => arr1.filter(item => !arr2.includes(item));

** 8. Get the union of two arrays **
const arrayUnion = (arr1, arr2) => [...new Set([...arr1, ...arr2])];

** 9. Check if an array is empty **
const isArrayEmpty = arr => arr.length === 0;

** 10. Check if all elements in an array are unique **
const isArrayUnique = arr => new Set(arr).size === arr.length;

** 11. Sum elements in an array **
const sumArray = arr => arr.reduce((sum, num) => sum + num, 0);

** 12. Find the max value in an array **
const maxInArray = arr => Math.max(...arr);

** 13. Find the min value in an array **
const minInArray = arr => Math.min(...arr);

** 14. Convert an array to an object with keys **
const arrayToObject = (arr, key) => Object.fromEntries(arr.map(item => [item[key], item]));

** 15. Find the most frequent element in an array **
const mostFrequent = arr => arr.reduce((acc, curr) => (acc[curr] = (acc[curr] || 0) + 1) && acc, {});

** 16. Rotate an array by k steps **
const rotateArray = (arr, k) => [...arr.slice(-k), ...arr.slice(0, -k)];

** 17. Remove falsy values from an array **
const removeFalsyValues = arr => arr.filter(Boolean);

** 18. Group elements in an array by a key **
const groupBy = (arr, key) => arr.reduce((acc, item) => ((acc[item[key]] = acc[item[key]] || []).push(item), acc), {});

** 19. Check if an array contains a value **
const containsValue = (arr, value) => arr.includes(value);

** 20. Reverse an array **
const reverseArray = arr => [...arr].reverse();

** 21. Capitalize the first letter of a string **
const capitalize = str => str.charAt(0).toUpperCase() + str.slice(1);

** 22. Convert a string to kebab case **
const toKebabCase = str => str.replace(/\s+/g, '-').toLowerCase();

** 23. Convert a string to camel case **
const toCamelCase = str => str.replace(/[-_\s]+(.)?/g, (_, c) => (c ? c.toUpperCase() : ''));

** 24. Convert a string to snake case **
const toSnakeCase = str => str.replace(/\s+/g, '_').toLowerCase();

** 25. Reverse a string **
const reverseString = str => str.split('').reverse().join('');

** 26. Check if a string is a palindrome **
const isPalindrome = str => str === str.split('').reverse().join('');

** 27. Count vowels in a string **
const countVowels = str => (str.match(/[aeiou]/gi) || []).length;

** 28. Truncate a string **
const truncateString = (str, length) => (str.length > length ? `${str.slice(0, length)}...` : str);

** 29. Repeat a string n times **
const repeatString = (str, n) => str.repeat(n);

** 30. Remove spaces from a string **
const removeSpaces = str => str.replace(/\s+/g, '');

** 31. Generate a random string of a given length **
const randomString = length => Math.random().toString(36).substring(2, 2 + length);

** 32. Get a string between two characters **
const getStringBetween = (str, start, end) => str.split(start)[1].split(end)[0];

** 33. Replace all occurrences of a substring **
const replaceAll = (str, find, replace) => str.split(find).join(replace);

** 34. Convert a string to title case **
const toTitleCase = str => str.replace(/\w\S*/g, txt => txt.charAt(0).toUpperCase() + txt.slice(1).toLowerCase());

** 35. Check if a string contains a substring **
const containsSubstring = (str, substring) => str.includes(substring);

** 36. Get a random element from an array **
const randomElement = arr => arr[Math.floor(Math.random() * arr.length)];

** 37. Calculate the factorial of a number **
const factorial = num => (num <= 1 ? 1 : num * factorial(num - 1));

** 38. Generate a random number in a range **
const randomInRange = (min, max) => Math.floor(Math.random() * (max - min + 1)) + min;

** 39. Check if a number is even **
const isEven = num => num % 2 === 0;

** 40. Check if a number is odd **
const isOdd = num => num % 2 !== 0;

** 41. Round a number to n decimal places **
const roundTo = (num, decimals) => Number(num.toFixed(decimals));

** 42. Calculate the power of a number **
const power = (base, exponent) => Math.pow(base, exponent);

** 43. Find the greatest common divisor (GCD) **
const gcd = (a, b) => (!b ? a : gcd(b, a % b));

** 44. Find the least common multiple (LCM) **
const lcm = (a, b) => (a * b) / gcd(a, b);

** 45. Check if a number is prime **
const isPrime = num => num > 1 && Array.from({ length: num - 2 }, (_, i) => i + 2).every(n => num % n !== 0);

** 46. Generate a random color **
const randomColor = () => `#${Math.floor(Math.random() * 16777215).toString(16)}`;

** 47. Get query parameters from a URL **
const getQueryParams = url => Object.fromEntries(new URL(url).searchParams.entries());

** 48. Deep clone an object **
const deepClone = obj => JSON.parse(JSON.stringify(obj));

** 49. Merge two objects **
const mergeObjects = (obj1, obj2) => ({ ...obj1, ...obj2 });

** 50. Check if an object is empty **
const isObjectEmpty = obj => Object.keys(obj).length === 0;

** 51. Get the keys of an object **
const getObjectKeys = obj => Object.keys(obj);

** 52. Get the values of an object **
const getObjectValues = obj => Object.values(obj);

** 53. Get the entries of an object **
const getObjectEntries = obj => Object.entries(obj);

** 54. Check if a key exists in an object **
const hasKey = (obj, key) => Object.prototype.hasOwnProperty.call(obj, key);

** 55. Convert an object to query string **
const objectToQueryString = obj => new URLSearchParams(obj).toString();

** 56. Freeze an object **
const freezeObject = obj => Object.freeze(obj);

** 57. Seal an object **
const sealObject = obj => Object.seal(obj);

** 58. Convert an array to a CSV string **
const arrayToCSV = arr => arr.map(row => row.join(',')).join('\n');

** 59. Parse a CSV string to an array **
const csvToArray = csv => csv.split('\n').map(row => row.split(','));

** 60. Check if a date is valid **
const isValidDate = date => !isNaN(new Date(date).getTime());

** 61. Format a date to YYYY-MM-DD **
const formatDate = date => new Date(date).toISOString().split('T')[0];

** 62. Get the difference in days between two dates **
const daysBetweenDates = (date1, date2) => Math.ceil((new Date(date2) - new Date(date1)) / (1000 * 60 * 60 * 24));

** 63. Add days to a date **
const addDays = (date, days) => new Date(new Date(date).setDate(new Date(date).getDate() + days));

** 64. Get the current timestamp **
const getTimestamp = () => Date.now();

** 65. Convert a timestamp to a date **
const timestampToDate = timestamp => new Date(timestamp).toLocaleDateString();

** 66. Check if a year is a leap year **
const isLeapYear = year => (year % 4 === 0 && year % 100 !== 0) || year % 400 === 0;

** 67. Get the day of the week from a date **
const getDayOfWeek = date => new Date(date).toLocaleString('en-US', { weekday: 'long' });

** 68. Check if a DOM element is visible **
const isVisible = el => !!(el.offsetWidth || el.offsetHeight || el.getClientRects().length);

** 69. Smooth scroll to an element **
const smoothScrollTo = id => document.getElementById(id).scrollIntoView({ behavior: 'smooth' });

** 70. Get the computed style of an element **
const getStyle = (el, prop) => window.getComputedStyle(el).getPropertyValue(prop);

** 71. Toggle a class on an element **
const toggleClass = (el, className) => el.classList.toggle(className);

** 72. Create a new DOM element **
const createElement = (tag, attrs = {}, ...children) => {
  const el = document.createElement(tag);
  Object.entries(attrs).forEach(([key, value]) => el.setAttribute(key, value));
  children.forEach(child => el.appendChild(child instanceof Node ? child : document.createTextNode(child)));
  return el;
};

** 73. Remove all children of an element **
const clearChildren = el => { while (el.firstChild) el.removeChild(el.firstChild); };

** 74. Get the scroll position of an element **
const getScrollPosition = el => ({ top: el.scrollTop, left: el.scrollLeft });

** 75. Debounce a function **
const debounce = (func, wait) => {
  let timeout;
  return (...args) => {
    clearTimeout(timeout);
    timeout = setTimeout(() => func.apply(this, args), wait);
  };
};

** 76. Throttle a function **
const throttle = (func, limit) => {
  let inThrottle;
  return (...args) => {
    if (!inThrottle) {
      func.apply(this, args);
      inThrottle = true;
      setTimeout(() => (inThrottle = false), limit);
    }
  };
};

** 77. Copy text to clipboard **
const copyToClipboard = text => navigator.clipboard.writeText(text);

** 78. Check if an element has a specific class **
const hasClass = (el, className) => el.classList.contains(className);

** 79. Get a random boolean value **
const randomBoolean = () => Math.random() >= 0.5;

** 80. Generate a UUID **
const generateUUID = () => 'xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx'.replace(/[xy]/g, c => {
  const r = (Math.random() * 16) | 0;
  return c === 'x' ? r.toString(16) : ((r & 0x3) | 0x8).toString(16);
});

** 81. Deep freeze an object **
const deepFreeze = obj => {
  Object.keys(obj).forEach(name => typeof obj[name] === 'object' && deepFreeze(obj[name]));
  return Object.freeze(obj);
};

** 82. Get the type of a variable **
const getType = value => Object.prototype.toString.call(value).slice(8, -1);

** 83. Check if a variable is null or undefined **
const isNullOrUndefined = value => value === null || value === undefined;

** 84. Convert a number to a currency string **
const toCurrency = (num, locale = 'en-US', currency = 'USD') => num.toLocaleString(locale, { style: 'currency', currency });

** 85. Get a random hexadecimal color **
const randomHexColor = () => `#${Math.floor(Math.random() * 16777215).toString(16).padStart(6, '0')}`;

** 86. Check if a string starts with a capital letter **
const startsWithCapital = str => /^[A-Z]/.test(str);

** 87. Remove HTML tags from a string **
const stripHtmlTags = str => str.replace(/<[^>]*>/g, '');

** 88. Check if a string is a valid URL **
const isValidUrl = str => {
  try {
    new URL(str);
    return true;
  } catch {
    return false;
  }
};

** 89. Get the current URL **
const getCurrentUrl = () => window.location.href;

** 90. Calculate the percentage of a number **
const calculatePercentage = (partial, total) => (total === 0 ? 0 : (partial / total) * 100).toFixed(2);

** 91. Check if a number is within a range **
const isInRange = (num, min, max) => num >= min && num <= max;

** 92. Convert degrees to radians **
const toRadians = degrees => (degrees * Math.PI) / 180;

** 93. Convert radians to degrees **
const toDegrees = radians => (radians * 180) / Math.PI;

** 94. Get a random date within a range **
const randomDate = (start, end) => new Date(start.getTime() + Math.random() * (end.getTime() - start.getTime()));

** 95. Capitalize every word in a string **
const capitalizeWords = str => str.replace(/\b\w/g, char => char.toUpperCase());

** 96. Get the nth Fibonacci number **
const fibonacci = n => (n <= 1 ? n : fibonacci(n - 1) + fibonacci(n - 2));

** 97. Remove duplicates from an array of objects based on a key **
const uniqueByKey = (arr, key) => [...new Map(arr.map(item => [item[key], item])).values()];

** 98. Parse a JSON string safely **
const safeJsonParse = str => {
  try {
    return JSON.parse(str);
  } catch {
    return null;
  }
};

** 99. Check if a variable is an array **
const isArray = value => Array.isArray(value);

** 100. Get the last element of an array **
const lastElement = arr => arr[arr.length - 1];
