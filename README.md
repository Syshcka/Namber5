byte_size('?') # 4
byte_size('Hello World') # 11
from functools import reduce


def count_occurences(arr, val):
    return reduce(
        (lambda x, y: x + 1 if y == val and type(y) == type(val) else x + 0),
        arr)

def difference(a, b):
    b = set(b)
    return [item for item in a if item not in b]
function prompt(question, callback) {
  let stdin = process.stdin,
    stdout = process.stdout

  stdin.resume()
  stdout.write(question)

  stdin.once('data', function (data) {
    callback(data.toString().trim())
  })
}

prompt(
  'Введите числа через запятую, например "3.9, 6, 7.8, 6", без кавычек: ',
  function (input) {
    let a = input.split(',')
    console.log('Введено:', a)
    let b = 0

    a.forEach((num) => {
      b += parseFloat(num)
    })
    console.log('Среднее арифметическое данных чисел:', b / a.length)
    prompt('Нажмите Enter, чтобы выйти: ', function (input) {
      process.exit()
    })
  },
)

def insertion_sort(arr):

    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1
        while j >= 0 and key < arr[j]:
            arr[j + 1] = arr[j]
            j -= 1
            arr[j + 1] = key

Number.prototype[Symbol.iterator] = function* () {
  for (let i = 0; i < this; i++) yield i + 1
}

console.log([...5]) // [1, 2, 3, 4, 5]

Object.prototype.forEach = Array.prototype.forEach

Object.defineProperty(Object.prototype, 'length', {
  get: () => Object.keys(this).length,
})

let a = {
  0: 123,
  1: 'test',
}

a.forEach((e) => console.log(e))

console.log(a.forEach) // forEach() { [native code] }
