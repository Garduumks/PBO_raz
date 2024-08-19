~~~dart
void main() {
  // Menggunakan aritmatika
  List<int> numbers = [10, 20, 30, 40, 50];
  
  // Fungsi untuk menghitung total dari list
  int sum(List<int> numbers) {
    int total = 0;
    for (int number in numbers) {
      total += number;
    }
    return total;
  }

  // Fungsi untuk menghitung rata-rata dari list
  double average(List<int> numbers) {
    if (numbers.isEmpty) {
      return 0.0;
    }
    return sum(numbers) / numbers.length;
  }

  // Fungsi untuk menampilkan hasil
  void printResults() {
    double avg = average(numbers);
    if (avg > 25) {
      print("Rata-rata lebih dari 25: $avg");
    } else {
      print("Rata-rata 25 atau kurang: $avg");
    }
  }

  // Menampilkan hasil
  printResults();
  
  // Closure contoh
  var multiplier = createMultiplier(2);
  print("Hasil kali 3 dengan multiplier 2: ${multiplier(3)}");
}

// Fungsi yang mengembalikan closure
Function createMultiplier(int multiplier) {
  return (int value) => value * multiplier;
}
~~~