# Power-quality-analyzer
# Power Quality Analyzer

print("==============================")
print("      POWER QUALITY ANALYZER")
print("==============================")

voltage = float(input("Enter voltage (V): "))
current = float(input("Enter current (A): "))
frequency = float(input("Enter frequency (Hz): "))
power_factor = float(input("Enter power factor (0-1): "))

fault = False

# Voltage check
if voltage < 200:
    print("⚠️ Under-voltage detected")
    fault = True
elif voltage > 250:
    print("⚠️ Over-voltage detected")
    fault = True

# Frequency check
if frequency < 49 or frequency > 51:
    print("⚠️ Frequency variation detected")
    fault = True

# Power factor check
if power_factor < 0.8:
    print("⚠️ Low power factor detected")
    fault = True

# Final result
if fault:
    print("\n🔴 POWER QUALITY: POOR")
    print("⚠️ Power quality improvement required")
else:
    print("\n🟢 POWER QUALITY: GOOD")
    print("✅ Voltage, frequency and power factor are within limits")
