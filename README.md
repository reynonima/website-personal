import random

symbols = ['🍒', '🍋', '🔔', '⭐', '💎', '7️⃣']

def spin_slot():
    # 40% peluang menang, 60% kalah
    is_win = random.random() < 0.4

    if is_win:
        # Pilih satu simbol acak dan buat tiga simbol sama
        chosen_symbol = random.choice(symbols)
        result = [chosen_symbol] * 3
    else:
        # Pastikan simbol berbeda (tidak menang)
        result = random.sample(symbols, 3)

    print(" | ".join(result))

    if is_win:
        print("🎉 MENANG! Anda mendapatkan jackpot.")
    else:
        print("😢 Kalah. Coba lagi.")

# Jalankan beberapa kali untuk simulasi
for _ in range(10):
    spin_slot()
    print("-" * 20)
