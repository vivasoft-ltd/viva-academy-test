# ১. Let, Const, Var (লেট, কনস্ট, ভার)

জাভাস্ক্রিপ্টে ভেরিয়েবল ডিক্লেয়ার করার জন্য `var`, `let`, ও `const` ব্যবহার করা হয়। এদের মধ্যে **স্কোপ (Scope)** ও **রিডিক্লেয়ার/রিঅ্যাসাইন** এর পার্থক্য রয়েছে।

---

## 🔍 পার্থক্যসমূহ (ES6+ অনুযায়ী)
| বৈশিষ্ট্য          | `var`                          | `let`                          | `const`                        |
|--------------------|--------------------------------|--------------------------------|--------------------------------|
| **স্কোপ**          | ফাংশন-স্কোপড                 | ব্লক-স্কোপড                  | ব্লক-স্কোপড                  |
| **রিঅ্যাসাইন**     | হ্যাঁ                         | হ্যাঁ                         | না (প্রিমিটিভ টাইপের ক্ষেত্রে) |
| **রিডিক্লেয়ার**    | হ্যাঁ (নতুন ভেরিয়েবল তৈরি করে না) | না (একই স্কোপে)              | না                            |
| **হোইস্টিং**       | `undefined` হিসাবে হোইস্ট হয়  | রেফারেন্স এরর (TDZ)           | রেফারেন্স এরর (TDZ)           |

---

## 📝 ব্যাখ্যা ও উদাহরণ

### ১. `var` (পুরনো স্টাইল)
- **ফাংশন-স্কোপড**: শুধুমাত্র ফাংশনের ভিতরে লক থাকে।
- **রিডিক্লেয়ার সম্ভব**: একই নামে একাধিক ভেরিয়েবল বানানো যায় (ঝুঁকিপূর্ণ!)।

```javascript
var age = 25;
var age = 30; // রিডিক্লেয়ার সম্ভব (কিন্তু খারাপ প্র্যাকটিস)
console.log(age); // 30
```
Will discuss later.
