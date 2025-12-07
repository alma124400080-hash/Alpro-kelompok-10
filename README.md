Projek Mini Jarkom Kelompok 10
Anggota Kelompok:

Alma Riski Mardansyah (124400080)
Lusiana Maheswari (124400092)
M. Tegar Herawan Wijaya (124400070)


mahasiswa = []  

def tambah_mahasiswa():
    print("\n=== Tambah Data Mahasiswa ===")
    input("Nama        : ")
    input("NIM         : ")
    input("Tempat/Tgl Lahir : ")
    input("Alamat      : ")

    data = {
        "nama": nama,
        "nim": nim,
        "ttl": ttl,
        "alamat": alamat
    }
    mahasiswa.append(data)
    print("Data berhasil ditambahkan!\n")


def tampilkan_data():
    print("\n=== Data Mahasiswa ===")
    if len(mahasiswa) == 0:
        print("Belum ada data.\n")
        return
    
    for i, mhs in enumerate(mahasiswa, start=1):
        print(f"{i}. Nama: {mhs['nama']}")
        print(f"   NIM : {mhs['nim']}")
        print(f"   TTL : {mhs['ttl']}")
        print(f"   Alamat : {mhs['alamat']}\n")


def menu():
    while True:
        print("===== MENU DATA MAHASISWA =====")
        print("1. Tambah Data")
        print("2. Tampilkan Data")
        print("3. Keluar")
        
        pilihan = input("Pilih menu: ")
        
        if pilihan == "1":
            tambah_mahasiswa()
        elif pilihan == "2":
            tampilkan_data()
        elif pilihan == "3":
            print("Program selesai.")
            break
        else:
            print("Pilihan tidak valid!\n")

menu()
