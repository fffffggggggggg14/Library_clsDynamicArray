✅ 📄 وصف README احترافي لـ clsDynamicArray
clsDynamicArray

A lightweight, generic dynamic array implementation in C++ that mimics features similar to std::vector, with explicit control over memory, resizing, insertion, deletion, and element access.

🚀 Features
✔ Generic Template Support

Works with any data type (int, string, custom objects...).

✔ Dynamic Resizing

resize(new_len) to expand or shrink the array

Fully manages memory internally

✔ Element Access

set(index, value)

get(index)

Supports negative indexing (like Python)

✔ Insertion

Insert at any position using:

insert(index, data)

insert_beginning()

insert_last()

insert_after()

insert_before()

✔ Deletion

del(index)

del_first()

del_last()

del_data(value)

✔ Utilities

reverse()

cls() (clear array)

print()

find(value)

empty()

len()

✔ Memory-Safe Destructor

Automatically frees allocated memory.

📦 Example Usage
#include "clsDynamicArray.h"

int main() {
    clsDynamicArray<int> arr(3);

    arr.set(0, 10);
    arr.set(1, 20);
    arr.set(2, 30);

    arr.insert_last(40);
    arr.del(1);
    arr.reverse();
    
    arr.print(); // 40 30 10

    return 0;
}

🛠 Implementation Notes

Implements dynamic array operations manually (without STL).

Negative indices behave like Python: -1 → last element.

Ensures safe resizing through temporary buffers.
