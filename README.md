Initialize three variables as counters: length, words, and vowels.
Read the sentence character by character.
If the character is a space, increment the words counter.
If the character is a period, increment the length counter.
If the character is a vowel (a, e, i, o, u), increment the vowels counter.
Otherwise, increment the length counter.
Return the length, words, and vowels counters.
HERE IS THE JAVASCRIPT:
function countSentence(sentence) {
  let length = 0;
  let wordCount = 0;
  let vowelCount = 0;

  for (let i = 0; i < sentence.length; i++) {
    length++;

    if (sentence[i] === ' ') {
      wordCount++;
    }

    const lowercaseChar = sentence[i].toLowerCase();
    if (lowercaseChar === 'a' || lowercaseChar === 'e' || lowercaseChar === 'i' || lowercaseChar === 'o' || lowercaseChar === 'u') {
      vowelCount++;
    }
  }

  wordCount++; // Account for the last word after the final space

  return [length, wordCount, vowelCount];
}

// Example usage:
const sentence = prompt("Enter a sentence:");
const [length, wordCount, vowelCount] = countSentence(sentence);

console.log("Length of the sentence:", length);
console.log("Number of words:", wordCount);
console.log("Number of vowels:", vowelCount);
#   A l g o r i t h m - c h e c k p o i n t  
 