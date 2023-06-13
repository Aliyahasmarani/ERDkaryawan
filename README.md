# pertemuan12_semester2

```s
NAMA    : ALIYAH ASMARANI
NIM     : 312210203
KELAS   : TI.22.A.2
MATKUL  : BASIS DATA
```

## ERDkaryawan
!

## membuat tabel 

```
CREATE TABLE departemen (
    -> id_departemen INT PRIMARY KEY,
    -> nama_departemen VARCHAR (50));
```

```
CREATE TABLE karyawan (
    -> id_karyawan INT PRIMARY KEY,
    -> nama_karyawan VARCHAR (50),
    -> id_departemen INT,
    -> id_manager INT);
```

```
CREATE TABLE supervisor(
    -> id_supervisor INT PRIMARY KEY,
    -> id_departemen INT,
    -> id_karyawan INT);
```

```
CREATE TABLE project(
    -> id_project INT PRIMARY KEY,
    -> nama_project VARCHAR (50),
    -> id_departemen INT);
```

```
CREATE TABLE karyawan_project(
    -> id_karyawan INT,
    -> id_project INT);
```

## menyambungkan tabel

```
ALTER TABLE karyawan ADD CONSTRAINT FOREIGN KEY (id_departemen) REFERENCES departemen (id_departemen);
ALTER TABLE supervisor ADD CONSTRAINT FOREIGN KEY (id_departemen) REFERENCES departemen (id_departemen);
ALTER TABLE supervisor ADD CONSTRAINT FOREIGN KEY (id_karyawan) REFERENCES karyawan (id_karyawan);
ALTER TABLE karyawan_project ADD CONSTRAINT FOREIGN KEY (id_karyawan) REFERENCES karyawan (id_karyawan);
ALTER TABLE karyawan ADD CONSTRAINT FOREIGN KEY (id_manager) REFERENCES karyawan (id_karyawan);
```

![1](https://github.com/Aliyahasmarani/ERDkaryawan/assets/115197672/b624ec56-f662-474e-9b79-b6f5f594f463)





