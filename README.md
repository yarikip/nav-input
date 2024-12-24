# nav-input
# nav-input
// Функция проверки имени
export function isValidName(name) {
  if (typeof name !== 'string') {
    return false; // Имя должно быть строкой
  }
  
  const words = name.trim().split(' '); // Разделяем строку на слова
  if (words.length < 2) {
    return false; // Должно быть хотя бы два слова
  }
  
  return words.every(word => word[0] === word[0].toUpperCase()); // Проверяем, что каждое слово начинается с заглавной буквы
}

// Примеры использования isValidName
console.log(isValidName('Test Name')); // true
console.log(isValidName('TestName')); // false
console.log(isValidName('test Name')); // false

// Функция проверки пароля
export function isValidPassword(password) {
  if (typeof password !== 'string' || password.length < 8) {
    return false; // Длина пароля должна быть не менее 8 символов
  }
  
  const hasDigit = /\d/; // Регулярное выражение для проверки наличия цифры
  return hasDigit.test(password); // Проверяем наличие хотя бы одной цифры
}

// Примеры использования isValidPassword
console.log(isValidPassword('qwerty123')); // true
console.log(isValidPassword('qwertyqwerty')); // false
console.log(isValidPassword('qwerty1')); // false