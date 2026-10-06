## Hola, First time Study AI Engineers

#### Python Challanges
- Weathermap-AI #Session 2
  ```
    # STARTER — silakan modifikasi
    
    def weather_ai(temp, threshold=29):
        # TODO 1: implement if/elif/else
        # Hint bonus:
        # - kalau threshold - 3 <= temp < threshold + 3 => "sejuk"
        # - kalau temp >= threshold + 3 => "panas"
        # - kalau temp < threshold - 3 => "sejuk"
        # - kalau temp < threshold - 6 => "dingin"
        
        if temp >= threshold:
            return "panas"
        elif temp >= 27 and temp < threshold:
            return "sejuk"
        elif temp >= 24 and temp < 27:
            return "dingin"
        else:
            return "sangat dingin"
    
    temps = [19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33]
    threshold = 29
    
    # TODO 2: loop semua temps dan print hasilnya
    for t in temps:
        print(t, "=>", weather_ai(t, threshold=threshold))
    
    print("\n--- BONUS: Hasil sebagai dictionary ---")
    # TODO 3 (BONUS): simpan hasil sebagai list of dictionaries
    results = []
    for t in temps:
        result = {
            "temperature": t,
            "label": weather_ai(t, threshold=threshold),
            "threshold": threshold
        }
        results.append(result)
    
    # Print hasil yang terstruktur
    for r in results:
        print(f"Suhu {r['temperature']}°C => {r['label']} (threshold: {r['threshold']}°C)")
  ```
