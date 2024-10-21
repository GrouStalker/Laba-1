import numpy as np
import matplotlib.pyplot as plt

# Р Р°Р·РјРµСЂ РјР°СЃСЃРёРІР°
n = np.linspace(1, 200000, 200)  # РѕС‚ 1 РґРѕ 200000

# Р’СЂРµРјРµРЅРЅС‹Рµ СЃР»РѕР¶РЅРѕСЃС‚Рё
# Р›СѓС‡С€РёР№ СЃР»СѓС‡Р°Р№
selection_sort_best = n**2
insertion_sort_best = n
bubble_sort_best = n
merge_sort_best = n * np.log2(n)
shell_sort_best = n * np.log2(n)  # РїСЂРµРґРїРѕР»РѕР¶РёРј, С‡С‚Рѕ С€Р°Рі РѕРїС‚РёРјР°Р»РµРЅ
quick_sort_best = n * np.log2(n)
heap_sort_best = n * np.log2(n)

# РЎСЂРµРґРЅРёР№ СЃР»СѓС‡Р°Р№
selection_sort_avg = n**2
insertion_sort_avg = n**2
bubble_sort_avg = n**2
merge_sort_avg = n * np.log2(n)
shell_sort_avg = n * np.log2(n)
quick_sort_avg = n * np.log2(n)
heap_sort_avg = n * np.log2(n)

# РҐСѓРґС€РёР№ СЃР»СѓС‡Р°Р№
selection_sort_worst = n**2
insertion_sort_worst = n**2
bubble_sort_worst = n**2
merge_sort_worst = n * np.log2(n)
shell_sort_worst = n**2
quick_sort_worst = n**2
heap_sort_worst = n * np.log2(n)

# РџРѕСЃС‚СЂРѕРµРЅРёРµ РіСЂР°С„РёРєРѕРІ
plt.figure(figsize=(15, 10))

# Р“СЂР°С„РёРє РґР»СЏ Р»СѓС‡С€РµРіРѕ СЃР»СѓС‡Р°СЏ
plt.subplot(3, 1, 1)
plt.plot(n, selection_sort_best, label='Selection Sort O(n)', color='red')
plt.plot(n, insertion_sort_best, label='Insertion Sort O(n)', color='blue')
plt.plot(n, bubble_sort_best, label='Bubble Sort O(n)', color='green')
plt.plot(n, merge_sort_best, label='Merge Sort O(n log n)', color='orange')
plt.plot(n, shell_sort_best, label='Shell Sort O(n log n)', color='purple')
plt.plot(n, quick_sort_best, label='Quick Sort O(n log n)', color='brown')
plt.plot(n, heap_sort_best, label='Heap Sort O(n log n)', color='cyan')
plt.title('Р’СЂРµРјРµРЅРЅС‹Рµ СЃР»РѕР¶РЅРѕСЃС‚Рё Р°Р»РіРѕСЂРёС‚РјРѕРІ СЃРѕСЂС‚РёСЂРѕРІРєРё (Р›СѓС‡С€РёР№ СЃР»СѓС‡Р°Р№)')
plt.xlabel('Р Р°Р·РјРµСЂ РјР°СЃСЃРёРІР° (n)')
plt.ylabel('Р’СЂРµРјРµРЅРЅР°СЏ СЃР»РѕР¶РЅРѕСЃС‚СЊ')
plt.yscale('log')
plt.legend()
plt.grid()

# Р“СЂР°С„РёРє РґР»СЏ СЃСЂРµРґРЅРµРіРѕ СЃР»СѓС‡Р°СЏ
plt.subplot(3, 1, 2)
plt.plot(n, selection_sort_avg, label='Selection Sort O(n^2)', color='red')
plt.plot(n, insertion_sort_avg, label='Insertion Sort O(n^2)', color='blue')
plt.plot(n, bubble_sort_avg, label='Bubble Sort O(n^2)', color='green')
plt.plot(n, merge_sort_avg, label='Merge Sort O(n log n)', color='orange')
plt.plot(n, shell_sort_avg, label='Shell Sort O(n log n)', color='purple')
plt.plot(n, quick_sort_avg, label='Quick Sort O(n log n)', color='brown')
plt.plot(n, heap_sort_avg, label='Heap Sort O(n log n)', color='cyan')
plt.title('Р’СЂРµРјРµРЅРЅС‹Рµ СЃР»РѕР¶РЅРѕСЃС‚Рё Р°Р»РіРѕСЂРёС‚РјРѕРІ СЃРѕСЂС‚РёСЂРѕРІРєРё (РЎСЂРµРґРЅРёР№ СЃР»СѓС‡Р°Р№)')
plt.xlabel('Р Р°Р·РјРµСЂ РјР°СЃСЃРёРІР° (n)')
plt.ylabel('Р’СЂРµРјРµРЅРЅР°СЏ СЃР»РѕР¶РЅРѕСЃС‚СЊ')
plt.yscale('log')
plt.legend()
plt.grid()

# Р“СЂР°С„РёРє РґР»СЏ С…СѓРґС€РµРіРѕ СЃР»СѓС‡Р°СЏ
plt.subplot(3, 1, 3)
plt.plot(n, selection_sort_worst, label='Selection Sort O(n^2)', color='red')
plt.plot(n, insertion_sort_worst, label='Insertion Sort O(n^2)', color='blue')
plt.plot(n, bubble_sort_worst, label='Bubble Sort O(n^2)', color='green')
plt.plot(n, merge_sort_worst, label='Merge Sort O(n log n)', color='orange')
plt.plot(n, shell_sort_worst, label='Shell Sort O(n^2)', color='purple')
plt.plot(n, quick_sort_worst, label='Quick Sort O(n^2)', color='brown')
plt.plot(n, heap_sort_worst, label='Heap Sort O(n log n)', color='cyan')
plt.title('Р’СЂРµРјРµРЅРЅС‹Рµ СЃР»РѕР¶РЅРѕСЃС‚Рё Р°Р»РіРѕСЂРёС‚РјРѕРІ СЃРѕСЂС‚РёСЂРѕРІРєРё (РҐСѓРґС€РёР№ СЃР»СѓС‡Р°Р№)')
plt.xlabel('Р Р°Р·РјРµСЂ РјР°СЃСЃРёРІР° (n)')
plt.ylabel('Р’СЂРµРјРµРЅРЅР°СЏ СЃР»РѕР¶РЅРѕСЃС‚СЊ')
plt.yscale('log')
plt.legend()
plt.grid()

plt.tight_layout()
plt.show()
