# ১. Let, Const, Var টাইপস্ক্রিপ্টে

টাইপস্ক্রিপ্টে `let`, `const`, ও `var` ব্যবহার করে ভেরিয়েবল ডিক্লেয়ার করা হয়, কিন্তু **স্ট্যাটিক টাইপিং** এর কারণে জাভাস্ক্রিপ্টের চেয়ে কিছু অতিরিক্ত সুবিধা থাকে।

---

## 🔍 পার্থক্য (টাইপস্ক্রিপ্টে)
| বৈশিষ্ট্য          | `var`                          | `let`                          | `const`                        |
|--------------------|--------------------------------|--------------------------------|--------------------------------|
| **স্কোপ**          | ফাংশন-স্কোপড                 | ব্লক-স্কোপড                  | ব্লক-স্কোপড                  |
| **টাইপ অ্যানোটেশন** | `var age: number = 25;`       | `let name: string = "আসিফ";`  | `const PI: number = 3.14;`     |
| **রিঅ্যাসাইন**     | হ্যাঁ                         | হ্যাঁ                         | না (প্রিমিটিভ টাইপের ক্ষেত্রে) |
| **রিডিক্লেয়ার**    | হ্যাঁ                         | না                            | না                            |

---

## 📝 উদাহরণ ও ব্যাখ্যা

### ১. `let` (টাইপ অ্যানোটেশন সহ)
```typescript
let সংখ্যা: number = 10;
সংখ্যা = 20; // ✅ রিঅ্যাসাইন সম্ভব
// সংখ্যা = "২০"; // ❌ Error: Type 'string' is not assignable to 'number'