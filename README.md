# Richest Customer Wealth (Flutter & FlutterFlow)

A cross-platform application designed to solve and visualize the **Richest Customer Wealth** problem. Built using Flutter and FlutterFlow, this project provides an interactive interface to identify the maximum wealth among a group of customers by calculating the sum of their bank accounts across different branches.

**Try it out here:** [Live Demo](example.com)

---

## Features

* **Cross-Platform Support:** Seamless deployment to Web, iOS, Android, and Desktop via Flutter’s unified codebase.
* **Matrix Input Handling:** Easily manage 2D arrays (customers × bank accounts) within the UI.
* **Wealth Calculation:** Real-time processing to determine the individual wealth of each customer and identify the maximum value.
* **Interactive Visualization:** Clear data tables and highlight indicators for the "Richest" customer.
* **Automated Deployment:** Streamlined web hosting via GitHub Actions and GitHub Pages.

---

## Technologies Used

* **Framework:** Flutter
* **Language:** Dart
* **Visual Builder:** FlutterFlow
* **CI/CD:** GitHub Actions

---

## Logic & Algorithm

The "Richest Customer Wealth" algorithm evaluates a grid (matrix) of integers where `accounts[i][j]` is the amount of money the $i^{th}$ customer has in the $j^{th}$ bank. The goal is to find the maximum wealth among all customers.

The logic follows a $O(m \times n)$ time complexity:

$$Wealth_i = \sum_{j=0}^{n-1} accounts[i][j]$$

$$\text{Maximum Wealth} = \max(Wealth_0, Wealth_1, \dots, Wealth_{m-1})$$

**Example:**

* **Input:** `[[1, 2, 3], [3, 2, 1]]`
* **Customer 1:** $1 + 2 + 3 = 6$
* **Customer 2:** $3 + 2 + 1 = 6$
* **Result:** `6`

---

## Getting Started

To run this project locally, ensure you have the [Flutter SDK](https://flutter.dev/docs/get-started/install) installed.

**1. Clone the repository:**

```bash
git clone https://github.com/ITJosue/FlutterFlow-Leetcode-Richest-Customer-Wealth.git
cd FlutterFlow-Leetcode-Richest-Customer-Wealth

```

**2. Fetch dependencies:**

```bash
flutter pub get

```

**3. Run the application:**

```bash
flutter run

```

---

## Code Example

The core logic of the application is handled by this Dart function:

```dart
int maximumWealth(List<List<int>> accounts) {
  int maxWealthSoFar = 0;
  
  for (var customer in accounts) {
    int currentCustomerWealth = customer.reduce((a, b) => a + b);
    if (currentCustomerWealth > maxWealthSoFar) {
      maxWealthSoFar = currentCustomerWealth;
    }
  }
  
  return maxWealthSoFar;
}

```

---

Would you like me to help you set up the **GitHub Actions** workflow file to automate your web deployment for this new project?
