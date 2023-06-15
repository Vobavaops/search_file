#include <iostream>
#include <filesystem>
#include <string>

namespace fs = std::filesystem;

void searchFile(const fs::path& directory, const std::string& fileName) {
    for (const auto& entry : fs::recursive_directory_iterator(directory)) {
        if (fs::is_regular_file(entry) && entry.path().filename() == fileName) {
            std::cout << "Файл найден: " << entry.path() << std::endl;
            return;
        }
    }

    std::cout << "Файл не найден" << std::endl;
}

int main() {
    std::cout << "Введите путь к директории: ";
    std::string directoryPath;
    std::getline(std::cin, directoryPath);

    std::cout << "Введите имя файла для поиска: ";
    std::string fileName;
    std::getline(std::cin, fileName);

    searchFile(directoryPath, fileName);

    return 0;
}
