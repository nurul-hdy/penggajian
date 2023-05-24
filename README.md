# 
class Karyawan:
    def __init__(self, nama, gaji):
        self.nama = nama
        self.gaji = gaji

    def hitung_gaji(self):
        return self.gaji


class Manajer(Karyawan):
    def __init__(self, nama, gaji, tunjangan):
        super().__init__(nama, gaji)
        self.tunjangan = tunjangan

    def hitung_gaji(self):
        return self.gaji + self.tunjangan


def main():
    karyawan1 = Karyawan("Johny", 9000000)
    manajer1 = Manajer("Kaylie", 8000000, 3000000)

    daftar_karyawan = [karyawan1, manajer1]

    print("Daftar Gaji Karyawan:")
    for karyawan in daftar_karyawan:
        print(f"Nama: {karyawan.nama}")
        print(f"Gaji: {karyawan.hitung_gaji()}")
        print()


if __name__ == "__main__":
    main()
