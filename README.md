# .NET Tools ASDF

1. install ASDF
```zsh
brew install asdf
```

2. เพิ่ม asdf ใน shell configuration:
	•	สำหรับ zsh (default ใน macOS):
```.zsh
echo -e '\n. $(brew --prefix asdf)/asdf.sh' >> ~/.zshrc
source ~/.zshrc
```

3. เพิ่มปลั๊กอิน .NET Core ให้ asdf
```zsh
asdf plugin add dotnet-core https://github.com/emersonsoares/asdf-dotnet-core.git
```

4. ตรวจสอบเวอร์ชันของ .NET Core ที่สามารถติดตั้งได้
```.zsh
asdf list-all dotnet-core
```

5. ติดตั้งเวอร์ชันที่ต้องการ (ตัวอย่างเช่น SDK 8.0.0)
```.zsh
asdf install dotnet-core 8.0.0
```

6. ตั้งค่าเวอร์ชันเป็นค่าเริ่มต้น (สำหรับทั้งระบบ)
```.zshrc
asdf global dotnet-core 8.0.0
```

สำหรับไดเรกทอรีปัจจุบัน (โปรเจกต์เฉพาะ)
```.zsh
asdf local dotnet-core 8.0.0
```

7. ตรวจสอบการติดตั้ง

```.zsh
dotnet --version
```

8. การสลับเวอร์ชัน .NET Core
```
asdf global dotnet-core <VERSION>
```
