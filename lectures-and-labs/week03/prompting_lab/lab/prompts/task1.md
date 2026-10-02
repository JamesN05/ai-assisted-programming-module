# Task 1 — Bad vs Good Prompt

## Bad Prompt

# Paste the vague/bad prompt you started with

# "Write a function to get the second largest number from a list"

## Good Prompt (SPEC)

# Paste your improved SPEC-formatted prompt

## AI Output (trimmed)

# Paste the accepted/truncated AI output you saved

def second_largest(numbers: list[int]) -> int:
    largest: int | None = None
    second: int | None = None

    for number in numbers:
        if largest is None or number > largest:
            second, largest = largest, number
        elif number != largest and (second is None or number > second):
            second = number

    if second is None:
        raise ValueError("need at least two distinct numbers")

    return second

# This returns the **second distinct-largest** value, so `[5, 5, 4]` returns `4`. It raises `ValueError` if the list has fewer than two distinct numbers. It runs in **O(n)** time. I checked it with normal, duplicate, negative-number, and too-short inputs.

## Why better

# Bullet points explaining why the SPEC prompt is better
