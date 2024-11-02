Jika Anda sudah menambahkan file ke GitHub namun ingin menerapkan `.gitignore` yang baru, Anda bisa mengikuti langkah-langkah ini:

1. **Tambahkan file yang ingin di-ignore ke `.gitignore`**  
   Pastikan file yang ingin di-ignore sudah ditambahkan dalam `.gitignore`.

2. **Hapus cache Git**  
   Perintah ini akan membersihkan file dari cache Git (seolah-olah menghapus tracking terhadap file yang di-ignore):
   ```bash
   git rm -r --cached .
   ```

3. **Tambahkan semua file kembali**  
   Setelah membersihkan cache, tambahkan file yang tersisa (yang tidak di-ignore oleh `.gitignore`):
   ```bash
   git add .
   ```

4. **Commit perubahan**  
   Commit perubahan untuk menghapus file yang tidak diinginkan dari tracking Git:
   ```bash
   git commit -m "Update .gitignore to remove tracked files"
   ```

5. **Push perubahan ke GitHub**  
   Setelah commit, dorong perubahan ini ke repository GitHub Anda:
   ```bash
   git push origin main
   ```
   
Langkah ini akan membuat Git hanya melacak file yang tidak di-ignore oleh `.gitignore` Anda.
