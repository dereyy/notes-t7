FROM node:20-alpine

# Set direktori kerja di dalam container
WORKDIR /app

# Salin hanya file dependency dulu untuk cache efficiency
COPY package*.json ./

# Install dependencies (termasuk ejs)
RUN npm install

# Setelah itu baru salin semua file project lainnya
COPY . .

# Ekspos port yang digunakan (pastikan sama dengan di app kamu)
EXPOSE 5000

# Jalankan aplikasi
CMD ["node", "index.js"]
