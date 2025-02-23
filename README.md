def count_words(file_path):
    try:
        with open(file_path, "r", encoding="utf-8") as file:
            text = file.read()
            words = text.split()
            return len(words)
    except FileNotFoundError:
        print("Файл не знайден")
        return 0

file_path = "quote.txt"
word_count = count_words(file_path)
print(f"Кількість слів у файлі {file_path}: {word_count}") 
