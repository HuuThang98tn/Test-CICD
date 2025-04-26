readme_content_vi = """\
# Cấu trúc Dự án Jetpack Compose

Đây là một cấu trúc dự án Jetpack Compose theo hướng Clean Architecture, kết hợp:

- ✅ **Jetpack Compose**: xây dựng UI hiện đại bằng Kotlin
- ✅ **Hilt**: tiêm dependency tự động
- ✅ **ViewModel**: quản lý trạng thái, giữ data tách biệt khỏi UI
- ✅ **Navigation Compose**: điều hướng giữa các màn hình

---

## 📁 Cấu trúc thư mục

```bash
com/
└── yourapp/
    ├── MainActivity.kt                      # Điểm khởi tạo, chứa setContent(App())
    ├── App.kt                               # Khởi tạo Compose + Hilt + Navigation
    ├── di/
    │   └── AppModule.kt                     # Module DI cho Hilt
    ├── navigation/
    │   └── AppNavGraph.kt                   # Biểu đồ điều hướng
    ├── ui/
    │   ├── theme/
    │   │   ├── Color.kt                     # Màu sắc
    │   │   ├── Shape.kt                     # Bo góc
    │   │   ├── Theme.kt                     # Giao diện tổng thể
    │   │   └── Type.kt                      # Font chữ
    │   └── components/
    │       └── MyButton.kt                  # Button dùng lại
    └── features/
        ├── home/
        │   ├── presentation/
        │   │   ├── HomeScreen.kt
        │   │   ├── HomeViewModel.kt
        │   │   └── components/
        │   │       └── HomeCard.kt
        │   ├── domain/
        │   │   ├── model/
        │   │   │   └── User.kt
        │   │   └── usecase/
        │   │       └── GetUsersUseCase.kt
        │   └── data/
        │       ├── repository/
        │       │   └── UserRepositoryImpl.kt
        │       ├── remote/
        │       │   └── ApiService.kt
        │       └── local/
        │           └── UserDao.kt
        └── detail/
            ├── presentation/
            │   └── DetailScreen.kt
            ├── domain/
            └── data/
