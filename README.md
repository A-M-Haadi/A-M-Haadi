erDiagram
    MAHASISWA {
        string NIM PK "NIM (PK)"
        string Nama
        string Prodi
    }

    MATA_KULIAH {
        string Kode PK "Kode (PK)"
        string Nama
        int SKS
    }

    DOSEN {
        string NIP PK "NIP (PK)"
        string Nama_Dosen
    }

    MAHASISWA ||--|{ MENGAMBIL : "mengambil"
    MENGAMBIL }|--|| MATA_KULIAH : "diambil"

    DOSEN ||--|{ MENGAJAR : "mengajar"
    MENGAJAR }|--|| MATA_KULIAH : "diajar oleh"
