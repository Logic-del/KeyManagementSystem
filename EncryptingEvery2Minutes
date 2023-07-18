import readline from "readline";
import fs from "fs";

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});

let logitechBinaryMapping = {
  "a": "10000000",
  "b": "01000000",
  "c": "11000000",
  "d": "00100000",
  "e": "10100000",
  "f": "01100000",
  "g": "11100000",
  "h": "00010000",
  "i": "10010000",
  "j": "01010000",
  "k": "11010000",
  "l": "00110000",
  "m": "10110000",
  "n": "01110000",
  "o": "11110000",
  "p": "00001000",
  "q": "10001000",
  "r": "01001000",
  "s": "11001000",
  "t": "00101000",
  "u": "10101000",
  "v": "01101000",
  "w": "11101000",
  "x": "00011000",
  "y": "10011000",
  "z": "01011000",
  "A": "10000001",
  "B": "01000001",
  "C": "11000001",
  "D": "00100001",
  "E": "10100001",
  "F": "01100001",
  "G": "11100001",
  "H": "00010001",
  "I": "10010001",
  "J": "01010001",
  "K": "11010001",
  "L": "00110001",
  "M": "10110001",
  "N": "01110001",
  "O": "11110001",
  "P": "00001001",
  "Q": "10001001",
  "R": "01001001",
  "S": "11001001",
  "T": "00101001",
  "U": "10101001",
  "V": "01101001",
  "W": "11101001",
  "X": "00011001",
  "Y": "10011001",
  "Z": "01011001",
  "1": "00111000",
  "2": "10111000",
  "3": "01111000",
  "4": "11111000",
  "5": "00000100",
  "6": "10000100",
  "7": "01000100",
  "8": "11000100",
  "9": "00100100",
  "0": "10100100",
  "!": "11100100",
  "@": "00010100",
  "#": "10010100",
  "$": "01010100",
  "%": "11010100",
  "^": "00110100",
  "&": "10110100",
  "*": "01110100",
  "(": "11110100",
  ")": "00001100",
  "-": "10001100",
  "_": "01001100",
  "+": "11001100",
  "=": "00101100",
  "{": "10101100",
  "[": "11101100",
  "}": "00011100",
  "]": "10011100",
  "|": "01011100",
  "\\":"11011100",
  ":": "00111100",
  ";": "10111100",
  "'": "01111100",
  "\"": "11111100",
  "<": "00000010",
  ">": "10000010",
  ",": "01000010",
  ".": "11000010",
  "/": "00100010",
  "?": "10100010",
  "`": "01100010",
  "~": "11100010",
};

function generateRandomValue(existingValues) {
  let randomValue;
  do {
    randomValue = Math.random().toString(36).substr(2, 8);
  } while (existingValues.includes(randomValue));
  return randomValue;
}


function writeKey(data) {
  fs.writeFileSync("LogitechKey.json", JSON.stringify(data));
  console.log("Logitech data saved to LogitechKey.json");
};

function loadFromJSON() {
  try {
    const data = fs.readFileSync("LogitechKey.json", "utf8");
    return JSON.parse(data);
  } catch (err) {
    console.error("Error loading Logitech data from LogitechKey.json:", err);
    return null;
  }
};

const savedData = loadFromJSON();
if (savedData) {
  logitechBinaryMapping = savedData;
}

  setInterval(() => {
    const randomizedMapping = {};
  for (const key in logitechBinaryMapping) {
    randomizedMapping[key] = generateRandomValue();
  }
  logitechBinaryMapping = randomizedMapping;
  writeKey(logitechBinaryMapping);
  }, 20 * 6000);
  Ask();
