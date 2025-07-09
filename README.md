{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": 2,
   "id": "627a75f9-d047-452c-8535-a502963a7ef3",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter the string string\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Reversed string: gnirts\n"
     ]
    }
   ],
   "source": [
    "string= input(\"Enter the string\")\n",
    "reversed_string = string[::-1]\n",
    "print(\"Reversed string:\", reversed_string)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "id": "6db60594-7d71-46ca-bb98-2b818246688e",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter a string:  string\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "The string is not a palindrome.\n"
     ]
    }
   ],
   "source": [
    "user_input = input(\"Enter a string: \")\n",
    "cleaned_input = user_input.replace(\" \", \"\").lower()\n",
    "if cleaned_input == cleaned_input[::-1]:\n",
    "    print(\"The string is a palindrome.\")\n",
    "else:\n",
    "    print(\"The string is not a palindrome.\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "id": "33c0083f-0a23-40f3-b6e5-cdeea94f1846",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter a number:  17\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Factorial of 17 is 355687428096000\n"
     ]
    }
   ],
   "source": [
    "def factorial(n):\n",
    "    if n == 0 or n == 1:\n",
    "        return 1\n",
    "    else:\n",
    "        return n * factorial(n - 1)\n",
    "\n",
    "\n",
    "num = int(input(\"Enter a number: \"))\n",
    "\n",
    "if num < 0:\n",
    "    print(\"Factorial is not defined for negative numbers.\")\n",
    "else:\n",
    "    result = factorial(num)\n",
    "    print(f\"Factorial of {num} is {result}\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "id": "8498439c-4bd0-4f9d-8f58-879a15a999d9",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter a number: 8\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Fibonacci series of 8 is [0, 1, 1, 2, 3, 5, 8, 13]\n"
     ]
    }
   ],
   "source": [
    "def Fibonacci_series(n):\n",
    "  fib_series=[]\n",
    "  a,b=0,1\n",
    "  for i in range(n):\n",
    "    fib_series.append(a)\n",
    "    a,b=b,a+b\n",
    "  return fib_series\n",
    "\n",
    "num = int(input('Enter a number:'))\n",
    "\n",
    "print('Fibonacci series of',num,'is',Fibonacci_series(num))"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "id": "99c2da75-129b-468b-944c-b8f8fd556e55",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter a number: 9\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "9 is not a prime number.\n"
     ]
    }
   ],
   "source": [
    "num = int(input('Enter a number:'))\n",
    "if num<=1:\n",
    "  print(f'{num} is not a prime number.')\n",
    "else:\n",
    "  for i in range(2, int(num**0.5)+1):\n",
    "    if num % i == 0:\n",
    "      print(f\"{num} is not a prime number.\")\n",
    "      break\n",
    "  else:\n",
    "    print(f\"{num} is a prime number.\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "id": "18819e71-5b4e-4f94-b6cd-de9cba6d2749",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter the first number: 1\n",
      "Enter the second number: 7\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "GCD of 1 and 7 is 1\n"
     ]
    }
   ],
   "source": [
    "def gcd(a,b):\n",
    "  while b != 0:\n",
    "    a,b =b,a % b\n",
    "  return a\n",
    "n1 = int(input('Enter the first number:'))\n",
    "n2 = int(input('Enter the second number:'))\n",
    "print(f\"GCD of {n1} and {n2} is {gcd(n1,n2)}\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "id": "12b1a875-41cc-4a70-8c53-72b7f95d6398",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter the string: ishpreet\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Number of vowels in the string is 3\n"
     ]
    }
   ],
   "source": [
    "text = input(\"Enter the string:\")\n",
    "vowels = \"aeiouAEIOU\"\n",
    "count = sum(text.count(vowel) for vowel in vowels)\n",
    "print(f\"Number of vowels in the string is {count}\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 11,
   "id": "786e2169-b696-4339-8ffa-06b2e72bb414",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Duplicate elements in the list are []\n"
     ]
    }
   ],
   "source": [
    "def fin_duplicates(lst):\n",
    "  seen=set()\n",
    "  duplicates = set()\n",
    "  for item in lst:\n",
    "    if item in seen:\n",
    "      duplicates.add(item)\n",
    "    else:\n",
    "      seen.add(item)\n",
    "    return list(duplicates)\n",
    "my_list = [1,2,3,4,5,6,5,2,6,3,2]\n",
    "print(f\"Duplicate elements in the list are {fin_duplicates(my_list)}\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 29,
   "id": "3d5a8071-cf07-4e0b-92ae-ec60c1f0a3f5",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter first string:  ishpreet\n",
      "Enter second string:  kaur\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "The strings are not anagrams.\n"
     ]
    }
   ],
   "source": [
    "def are_anagrams(str1, str2):\n",
    "    str1 = str1.replace(\" \", \"\").lower()\n",
    "    str2 = str2.replace(\" \", \"\").lower()\n",
    "\n",
    "    return sorted(str1) == sorted(str2)\n",
    "\n",
    "\n",
    "string1 = input(\"Enter first string: \")\n",
    "string2 = input(\"Enter second string: \")\n",
    "\n",
    "if are_anagrams(string1, string2):\n",
    "    print(\"The strings are anagrams.\")\n",
    "else:\n",
    "    print(\"The strings are not anagrams.\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 28,
   "id": "1a159ca0-9016-4a4c-a659-19dcd9b3fe25",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter sorted list 1 (space-separated):  1 2 3\n",
      "Enter sorted list 2 (space-separated):  3 2 1\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Merged sorted list: [1, 2, 3, 3, 2, 1]\n"
     ]
    }
   ],
   "source": [
    "def merge_sorted_lists(list1, list2):\n",
    "    merged_list = []\n",
    "    i = j = 0\n",
    "\n",
    "    while i < len(list1) and j < len(list2):\n",
    "        if list1[i] <= list2[j]:\n",
    "            merged_list.append(list1[i])\n",
    "            i += 1\n",
    "        else:\n",
    "            merged_list.append(list2[j])\n",
    "            j += 1\n",
    "\n",
    "\n",
    "    merged_list.extend(list1[i:])\n",
    "    merged_list.extend(list2[j:])\n",
    "\n",
    "    return merged_list\n",
    "\n",
    "\n",
    "list1 = list(map(int, input(\"Enter sorted list 1 (space-separated): \").split()))\n",
    "list2 = list(map(int, input(\"Enter sorted list 2 (space-separated): \").split()))\n",
    "\n",
    "\n",
    "result = merge_sorted_lists(list1, list2)\n",
    "print(\"Merged sorted list:\", result)\n",
    "\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 14,
   "id": "ff0f1630-3016-4b79-b255-b0f55f612c5d",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter the value of n:  1\n",
      "Enter the numbers (space-separated):  5\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Missing numbers in the range 1 to 1 are: -4\n"
     ]
    }
   ],
   "source": [
    "\t\n",
    "n = int(input(\"Enter the value of n: \"))\n",
    "\n",
    "numbers = list(map(int, input(\"Enter the numbers (space-separated): \").split()))\n",
    "\n",
    "expected_sum = (n * (n + 1)) // 2\n",
    "actual_sum = sum(numbers)\n",
    "\n",
    "missing_numbers = expected_sum - actual_sum\n",
    "\n",
    "print(\"Missing numbers in the range 1 to\", n, \"are:\", missing_numbers)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 15,
   "id": "96d9faa5-9f3b-4dd0-b630-f183e44c4fcb",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter a number: 17\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "17 is not an Armstrong number.\n"
     ]
    }
   ],
   "source": [
    "num = int(input('Enter a number:'))\n",
    "\n",
    "num_str = str(num)\n",
    "n = len(num_str)\n",
    "\n",
    "sum_of_power = sum(int(digit) ** n for digit in num_str)\n",
    "\n",
    "if sum_of_power == num:\n",
    "    print(f\"{num} is an Armstrong number.\")\n",
    "else:\n",
    "    print(f\"{num} is not an Armstrong number.\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 16,
   "id": "5abbb375-5912-4b14-904c-e6dc5bf73561",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter a sentence:  am ishpreet kaur\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "The sentence is not a pangram.\n"
     ]
    }
   ],
   "source": [
    "import string\n",
    "\n",
    "def is_pangram(sentence):\n",
    "\n",
    "    sentence = sentence.lower()\n",
    "\n",
    "\n",
    "    alphabet = set(string.ascii_lowercase)\n",
    "\n",
    "\n",
    "    sentence_set = set(sentence)\n",
    "\n",
    "    return alphabet.issubset(sentence_set)\n",
    "\n",
    "\n",
    "text = input(\"Enter a sentence: \")\n",
    "\n",
    "if is_pangram(text):\n",
    "    print(\"The sentence is a pangram.\")\n",
    "else:\n",
    "    print(\"The sentence is not a pangram.\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 18,
   "id": "4561d731-42fa-481b-ade1-8140d1f04bc7",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter the items :  1 2 3 2 4 2 5\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "List with duplicates removed: ['3', '4', '2', '1', '5']\n"
     ]
    }
   ],
   "source": [
    "items = input(\"Enter the items : \").split()\n",
    "\n",
    "unique_items = list(set(items))\n",
    "\n",
    "print(\"List with duplicates removed:\", unique_items)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 19,
   "id": "8c764ba0-b471-4ff8-9c7d-6546759848d8",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter the numbers (space-separated):  26\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "There is no second largest number.\n"
     ]
    }
   ],
   "source": [
    "num = list(map(int, input(\"Enter the numbers (space-separated): \").split()))\n",
    "\n",
    "first = second = float('-inf')\n",
    "\n",
    "for n in num:\n",
    "  if n > first:\n",
    "    second = first\n",
    "    first = num\n",
    "  elif first > num > second:\n",
    "    second = num\n",
    "\n",
    "if second == float('-inf'):\n",
    "  print(\"There is no second largest number.\")\n",
    "else:\n",
    "  print(\"The second largest number is:\", second)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 20,
   "id": "e12d6351-8314-47f3-9bde-c273d2b65e6e",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter the elements:  ishpreet\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Element counts\n",
      "ishpreet: 1\n"
     ]
    }
   ],
   "source": [
    "elements = input(\"Enter the elements: \").split()\n",
    "\n",
    "element_count = {}\n",
    "\n",
    "for element in elements:\n",
    "    if element in element_count:\n",
    "        element_count[element] += 1\n",
    "    else:\n",
    "        element_count[element] = 1\n",
    "\n",
    "print(\"Element counts\")\n",
    "for element, count in element_count.items():\n",
    "    print(f\"{element}: {count}\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 21,
   "id": "9c7c2b9c-cb90-4390-94e8-685197590418",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter the number of rows:  2\n",
      "Enter the number of columns:  2\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Enter the matrix row by row:\n"
     ]
    },
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      " 1 2 2 3\n",
      " 3 2 2 1\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Transpose of the matrix:\n",
      "[1, 3]\n",
      "[2, 2]\n"
     ]
    }
   ],
   "source": [
    "rows = int(input(\"Enter the number of rows: \"))\n",
    "cols = int(input(\"Enter the number of columns: \"))\n",
    "\n",
    "print(\"Enter the matrix row by row:\")\n",
    "matrix = []\n",
    "for i in range(rows):\n",
    "  row = list(map(int,input().split()))\n",
    "  matrix.append(row)\n",
    "\n",
    "transpose = []\n",
    "for j in range(cols):\n",
    "  transpose_row=[]\n",
    "  for i in range(rows):\n",
    "     transpose_row.append(matrix[i][j])\n",
    "  transpose.append(transpose_row)\n",
    "\n",
    "print(\"Transpose of the matrix:\")\n",
    "for row in transpose:\n",
    "  print(row)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 24,
   "id": "6393b9c1-e0da-4f54-af6f-988f7d833b77",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter the first list:  ishpreet kaur is a student\n",
      "Enter the second list:  Namrata gupta is a student\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Intersection of the lists: ['is', 'student', 'a']\n"
     ]
    }
   ],
   "source": [
    "list1 = input(\"Enter the first list: \").split()\n",
    "list2 = input(\"Enter the second list: \").split()\n",
    "\n",
    "intersection = list(set(list1) & set(list2))\n",
    "\n",
    "print(\"Intersection of the lists:\", intersection)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 25,
   "id": "2f891d28-d6fa-4a90-9159-107fe5e3b802",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Flattened list: [1, 2, 3, 4, 5, 6]\n"
     ]
    }
   ],
   "source": [
    "nested_list = [[1,2], [3,4], [5,6]]\n",
    "\n",
    "flattened_list=[]\n",
    "for sublist in nested_list:\n",
    "  flattened_list.extend(sublist)\n",
    "\n",
    "print(\"Flattened list:\", flattened_list)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 26,
   "id": "b0f5df34-7577-40a5-8eb8-729bb5788d27",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter a string:  ishpreet\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Number of words in the string: 1\n"
     ]
    }
   ],
   "source": [
    "text = input(\"Enter a string: \")\n",
    "\n",
    "word_count = len(text.split())\n",
    "\n",
    "print(\"Number of words in the string:\", word_count)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "42a0fa4d-46f8-4729-b32a-46d94077f32a",
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python [conda env:base] *",
   "language": "python",
   "name": "conda-base-py"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.12.7"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
