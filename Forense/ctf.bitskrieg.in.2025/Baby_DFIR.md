# Baby DFIR

[página del reto](https://ctf.bitskrieg.in)

En este reto, nos proporcionan un archivo "abc.ad1"

![imagen](https://github.com/user-attachments/assets/dc8a70df-3f8a-4cfe-a979-7262537942df)

Podemos utilizar un editor hexadecimal como xxd para inspeccionar el archivo (aunque yo lo he hecho en bruto)

![imagen](https://github.com/user-attachments/assets/5e6065e9-2a77-4a58-b5b8-1ccd5f9cb14d)

Si inspeccionamos a fondo este archivo, podemos encontrar lo que parece ser el archivo de flag

![imagen](https://github.com/user-attachments/assets/896f5dca-b0ed-479d-8bca-5fe91d194221)

Podemos utilizar herramientas com obindwalk para intentar extraer los archivos de este

![imagen](https://github.com/user-attachments/assets/9f20bbef-09f4-4ac1-9482-7767184a2064)

Y ahora buscando por los archivos obtenidos encontraremos nuestra flag

![imagen](https://github.com/user-attachments/assets/e6f35206-3211-4034-9979-db3615783b6f)

Podemos reducir la cantidad de archivos obtenidos eliminando caracteres hexadecimales del archivo inicial. Por Ejemplo

![imagen](https://github.com/user-attachments/assets/8520221e-42d3-4c0d-9714-803613dce49b)

<details>
  <summary>Mostrar la flag</summary>
BITSCTF{a_really_simple_intro_to_DFIR_12848a9e}
</details>

**Autor:** [Fernando Lorenzo](https://github.com/Fernandolv123)
