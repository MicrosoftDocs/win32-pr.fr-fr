---
description: Les exemples suivants illustrent l’utilisation de l’API de compression en mode mémoire tampon.
ms.assetid: 0A062E5D-E5FA-4098-B76E-E136FC74D853
title: Utilisation de l’API de compression en mode mémoire tampon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a63b8a7dabc7b61c85abb192f855f094a6e271a99997b9e98b849614d53527
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048937"
---
# <a name="using-the-compression-api-in-buffer-mode"></a>Utilisation de l’API de compression en mode mémoire tampon

Les exemples suivants illustrent l’utilisation de l’API de compression en mode mémoire tampon. Le mode mémoire tampon a été développé pour faciliter l’utilisation et fractionne automatiquement la mémoire tampon d’entrée en blocs d’une taille appropriée pour l’algorithme de compression sélectionné. Le mode mémoire tampon met en forme et stocke automatiquement la taille de la mémoire tampon non compressée dans le tampon compressé, où elle est disponible pour le décompresseur. La taille de la mémoire tampon compressée n’est pas enregistrée automatiquement et l’application doit l’enregistrer pour la décompression. N’incluez pas l’indicateur **Compress \_ RAW** lors de l’appel de [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) ou [**CREATEDECOMPRESSOR**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) si vous souhaitez utiliser l’API de compression en mode mémoire tampon.

Le mode mémoire tampon est recommandé dans la plupart des cas. Pour plus d’informations sur l’utilisation du mode bloc, consultez [utilisation de l’API de compression en mode bloc](using-the-compression-api-in-block-mode.md)

Les applications qui utilisent le mode mémoire tampon ou bloc ont la possibilité de spécifier une routine d’allocation de mémoire personnalisée lors de l’appel de [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) ou [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor). Consultez la section [utilisation de l’API de compression en mode bloc](using-the-compression-api-in-block-mode.md) pour obtenir un exemple de routine d’allocation personnalisée simple.

**Windows 8 et Windows Server 2012 :** pour utiliser l’exemple de code suivant, vous devez exécuter Windows 8 ou Windows Server 2012 et disposer de « compressapi. h » et de « cabinet.dll » et d’un lien vers le fichier « Cabinet. lib ».

L’extrait de code suivant illustre la compression de fichiers avec l’algorithme de compression XPRESS et l’encodage Huffman à l’aide de l’API de compression en mode mémoire tampon. L’application accepte un fichier, compresse son contenu et génère un fichier compressé. Tout d’abord, l’application appelle [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) avec l' **\_ algorithme de compression \_ Xpress \_ Huff** pour générer un compresseur. Elle appelle ensuite [**Compress**](/windows/desktop/api/compressapi/nf-compressapi-compress), avec *CompressedBufferSize* défini sur 0, pour interroger la taille requise de la mémoire tampon compressée. Elle alloue une mémoire tampon de sortie à la valeur *CompressedBufferSize* . L’application appelle **compresser** une deuxième fois pour effectuer la compression réelle. Enfin, l’application écrit les données compressées dans le fichier de sortie.


```C++
#include <Windows.h>
#include <stdio.h>
#include <compressapi.h>

void wmain(_In_ int argc, _In_ WCHAR *argv[])
{
    COMPRESSOR_HANDLE Compressor    = NULL;
    PBYTE CompressedBuffer          = NULL;
    PBYTE InputBuffer               = NULL;
    HANDLE InputFile                = INVALID_HANDLE_VALUE;
    HANDLE CompressedFile           = INVALID_HANDLE_VALUE;    
    BOOL DeleteTargetFile           = TRUE;
    BOOL Success;
    SIZE_T CompressedDataSize, CompressedBufferSize;
    DWORD InputFileSize, ByteRead, ByteWritten;
    LARGE_INTEGER FileSize;    
    ULONGLONG StartTime, EndTime;
    double TimeDuration;

    if (argc != 3)
    {
        wprintf(L"Usage:\n\t%s <input_file_name> <compressd_file_name>\n", argv[0]);
        return;
    }

    //  Open input file for reading, existing file only.
    InputFile = CreateFile(
        argv[1],                  //  Input file name
        GENERIC_READ,             //  Open for reading
        FILE_SHARE_READ,          //  Share for read
        NULL,                     //  Default security
        OPEN_EXISTING,            //  Existing file only
        FILE_ATTRIBUTE_NORMAL,    //  Normal file
        NULL);                    //  No attr. template

    if (InputFile == INVALID_HANDLE_VALUE)
    {
        wprintf(L"Cannot open \t%s\n", argv[1]);
        goto done;
    }

    //  Get input file size.
    Success = GetFileSizeEx(InputFile, &FileSize);
    if ((!Success)||(FileSize.QuadPart > 0xFFFFFFFF))
    {
        wprintf(L"Cannot get input file size or file is larger than 4GB.\n");        
        goto done;
    }
    InputFileSize = FileSize.LowPart;

    //  Allocate memory for file content.
    InputBuffer = (PBYTE)malloc(InputFileSize);
    if (!InputBuffer)
    {
        wprintf(L"Cannot allocate memory for uncompressed buffer.\n");
        goto done;
    }                              

    //  Read input file.
    Success = ReadFile(InputFile, InputBuffer, InputFileSize, &ByteRead, NULL);
    if ((!Success)||(ByteRead != InputFileSize))
    {
        wprintf(L"Cannot read from \t%s\n", argv[1]);
        goto done;
    }

    //  Open an empty file for writing, if exist, overwrite it.
    CompressedFile = CreateFile(
        argv[2],                  //  Compressed file name
        GENERIC_WRITE|DELETE,     //  Open for writing; delete if cannot compress
        0,                        //  Do not share
        NULL,                     //  Default security
        CREATE_ALWAYS,            //  Create a new file; if exist, overwrite it
        FILE_ATTRIBUTE_NORMAL,    //  Normal file
        NULL);                    //  No template

    if (CompressedFile == INVALID_HANDLE_VALUE)
    {
        wprintf(L"Cannot create file \t%s\n", argv[2]);
        goto done;
    }

    //  Create an XpressHuff compressor.
    Success = CreateCompressor(
        COMPRESS_ALGORITHM_XPRESS_HUFF, //  Compression Algorithm
        NULL,                           //  Optional allocation routine
        &Compressor);                   //  Handle

    if (!Success)
    {
        wprintf(L"Cannot create a compressor %d.\n", GetLastError());
        goto done;
    }

    //  Query compressed buffer size.
    Success = Compress(
        Compressor,                  //  Compressor Handle
        InputBuffer,                 //  Input buffer, Uncompressed data
        InputFileSize,               //  Uncompressed data size
        NULL,                        //  Compressed Buffer
        0,                           //  Compressed Buffer size
        &CompressedBufferSize);      //  Compressed Data size

    //  Allocate memory for compressed buffer.
    if (!Success)
    {
        DWORD ErrorCode = GetLastError();

        if (ErrorCode != ERROR_INSUFFICIENT_BUFFER)
        {
            wprintf(L"Cannot compress data: %d.\n", ErrorCode);
            goto done;
        }
            
        CompressedBuffer = (PBYTE)malloc(CompressedBufferSize);
        if (!CompressedBuffer)
        {
            wprintf(L"Cannot allocate memory for compressed buffer.\n");
            goto done;
        }
    }

    StartTime = GetTickCount64();

    //  Call Compress() again to do real compression and output the compressed
    //  data to CompressedBuffer.
    Success = Compress(
        Compressor,             //  Compressor Handle
        InputBuffer,            //  Input buffer, Uncompressed data
        InputFileSize,          //  Uncompressed data size
        CompressedBuffer,       //  Compressed Buffer
        CompressedBufferSize,   //  Compressed Buffer size
        &CompressedDataSize);   //  Compressed Data size

    if (!Success)
    {
        wprintf(L"Cannot compress data: %d\n", GetLastError());
        goto done;
    }

    EndTime = GetTickCount64();

    //  Get compression time.
    TimeDuration = (EndTime - StartTime)/1000.0;

    //  Write compressed data to output file.
    Success = WriteFile(
        CompressedFile,     //  File handle
        CompressedBuffer,   //  Start of data to write
        CompressedDataSize, //  Number of byte to write
        &ByteWritten,       //  Number of byte written
        NULL);              //  No overlapping structure

    if ((ByteWritten != CompressedDataSize) || (!Success))
    {
        wprintf(L"Cannot write compressed data to file: %d.\n", GetLastError());
        goto done;
    }

    wprintf(
        L"Input file size: %d; Compressed Size: %d\n", 
        InputFileSize, 
        CompressedDataSize);
    wprintf(L"Compression Time(Exclude I/O): %.2f seconds\n", TimeDuration);
    wprintf(L"File Compressed.\n");

    DeleteTargetFile = FALSE;

done:
    if (Compressor != NULL)
    {
        CloseCompressor(Compressor);
    }

    if (CompressedBuffer) 
    {
        free(CompressedBuffer);
    }

    if (InputBuffer)
    {
        free(InputBuffer);
    }

    if (InputFile != INVALID_HANDLE_VALUE)
    {
        CloseHandle(InputFile);
    }

    if (CompressedFile != INVALID_HANDLE_VALUE)
    {
        //  Compression fails, delete the compressed file.
        if (DeleteTargetFile)
        {
            FILE_DISPOSITION_INFO fdi;
            fdi.DeleteFile = TRUE;      //  Marking for deletion
            Success = SetFileInformationByHandle(
                CompressedFile,
                FileDispositionInfo,
                &fdi,
                sizeof(FILE_DISPOSITION_INFO));    
            if (!Success) {
                wprintf(L"Cannot delete corrupted compressed file.\n");
            }
        }
        CloseHandle(CompressedFile);
    }
}
```



L’extrait de code suivant illustre la décompression de fichier à l’aide de l’API de compression en mode mémoire tampon.


```C++
#include <Windows.h>
#include <stdio.h>
#include <compressapi.h>

void wmain(_In_ int argc, _In_ WCHAR *argv[])
{
    DECOMPRESSOR_HANDLE Decompressor    = NULL;
    PBYTE CompressedBuffer              = NULL;
    PBYTE DecompressedBuffer            = NULL;
    HANDLE InputFile                    = INVALID_HANDLE_VALUE;
    HANDLE DecompressedFile             = INVALID_HANDLE_VALUE;    
    BOOL DeleteTargetFile               = TRUE;    
    BOOL Success;
    SIZE_T DecompressedBufferSize, DecompressedDataSize;
    DWORD InputFileSize, ByteRead, ByteWritten;
    ULONGLONG StartTime, EndTime;
    LARGE_INTEGER FileSize;    
    double TimeDuration;

    if (argc != 3) 
    {
        wprintf(L"Usage:\n\t%s <compressed_file_name> <decompressed_file_name>\n", argv[0]);
        return;
    }

    //  Open input file for reading, existing file only.
    InputFile = CreateFile(
        argv[1],                  //  Input file name, compressed file
        GENERIC_READ,             //  Open for reading
        FILE_SHARE_READ,          //  Share for read
        NULL,                     //  Default security
        OPEN_EXISTING,            //  Existing file only
        FILE_ATTRIBUTE_NORMAL,    //  Normal file
        NULL);                    //  No template

    if (InputFile == INVALID_HANDLE_VALUE)
    {
        wprintf(L"Cannot open \t%s\n", argv[1]);
        goto done;
    }

    //  Get compressed file size.
    Success = GetFileSizeEx(InputFile, &FileSize);
    if ((!Success)||(FileSize.QuadPart > 0xFFFFFFFF))
    {
        wprintf(L"Cannot get input file size or file is larger than 4GB.\n");        
        goto done;
    }
    InputFileSize = FileSize.LowPart;

    //  Allocation memory for compressed content.
    CompressedBuffer = (PBYTE)malloc(InputFileSize);
    if (!CompressedBuffer)
    {
        wprintf(L"Cannot allocate memory for compressed buffer.\n");
        goto done;
    }

    //  Read compressed content into buffer.
    Success = ReadFile(InputFile, CompressedBuffer, InputFileSize, &ByteRead, NULL);
    if ((!Success) || (ByteRead != InputFileSize))
    {
        wprintf(L"Cannot read from \t%s\n", argv[1]);
        goto done;
    }

    //  Open an empty file for writing, if exist, destroy it.
    DecompressedFile = CreateFile(
        argv[2],                  //  Decompressed file name
        GENERIC_WRITE|DELETE,     //  Open for writing
        0,                        //  Do not share
        NULL,                     //  Default security
        CREATE_ALWAYS,            //  Create a new file, if exists, overwrite it.
        FILE_ATTRIBUTE_NORMAL,    //  Normal file
        NULL);                    //  No template

    if (DecompressedFile == INVALID_HANDLE_VALUE)
    {
        wprintf(L"Cannot create file \t%s\n", argv[2]);
        goto done;
    }

    //  Create an XpressHuff decompressor.
    Success = CreateDecompressor(
        COMPRESS_ALGORITHM_XPRESS_HUFF, //  Compression Algorithm
        NULL,                           //  Optional allocation routine
        &Decompressor);                 //  Handle

    if (!Success)
    {
        wprintf(L"Cannot create a decompressor: %d.\n", GetLastError());
        goto done;
    }

    //  Query decompressed buffer size.
    Success = Decompress(
        Decompressor,                //  Compressor Handle
        CompressedBuffer,            //  Compressed data
        InputFileSize,               //  Compressed data size
        NULL,                        //  Buffer set to NULL
        0,                           //  Buffer size set to 0
        &DecompressedBufferSize);    //  Decompressed Data size

    //  Allocate memory for decompressed buffer.
    if (!Success)
    {
        DWORD ErrorCode = GetLastError();

        // Note that the original size returned by the function is extracted 
        // from the buffer itself and should be treated as untrusted and tested
        // against reasonable limits.
        if (ErrorCode != ERROR_INSUFFICIENT_BUFFER) 
        {
            wprintf(L"Cannot decompress data: %d.\n",ErrorCode);
            goto done;
        }

        DecompressedBuffer = (PBYTE)malloc(DecompressedBufferSize);
        if (!DecompressedBuffer)
        {
            wprintf(L"Cannot allocate memory for decompressed buffer.\n");
            goto done;
        }           
    }
        
    StartTime = GetTickCount64();

    //  Decompress data and write data to DecompressedBuffer.
    Success = Decompress(
        Decompressor,               //  Decompressor handle
        CompressedBuffer,           //  Compressed data
        InputFileSize,              //  Compressed data size
        DecompressedBuffer,         //  Decompressed buffer
        DecompressedBufferSize,     //  Decompressed buffer size
        &DecompressedDataSize);     //  Decompressed data size

    if (!Success)
    {
        wprintf(L"Cannot decompress data: %d.\n", GetLastError());
        goto done;
    }

EndTime = GetTickCount64();

    //  Get decompression time.
    TimeDuration = (EndTime - StartTime)/1000.0;

    //  Write decompressed data to output file.
    Success = WriteFile(
        DecompressedFile,       //  File handle
        DecompressedBuffer,     //  Start of data to write
        DecompressedDataSize,   //  Number of byte to write
        &ByteWritten,           //  Number of byte written
        NULL);                  //  No overlapping structure
    if ((ByteWritten != DecompressedDataSize) || (!Success))
    {
        wprintf(L"Cannot write decompressed data to file.\n");
        goto done;
    }
    
    wprintf(
        L"Compressed size: %d; Decompressed Size: %d\n",
        InputFileSize,
        DecompressedDataSize);
    wprintf(L"Decompression Time(Exclude I/O): %.2f seconds\n", TimeDuration);
    wprintf(L"File decompressed.\n");

    DeleteTargetFile = FALSE;

done:
    if (Decompressor != NULL)
    {
        CloseDecompressor(Decompressor);
    }

    if (CompressedBuffer) 
    {
        free(CompressedBuffer);
    }

    if (DecompressedBuffer)
    {
        free(DecompressedBuffer);
    }

    if (InputFile != INVALID_HANDLE_VALUE)
    {
        CloseHandle(InputFile);
    }

    if (DecompressedFile != INVALID_HANDLE_VALUE)
    {
        //  Compression fails, delete the compressed file.
        if (DeleteTargetFile)
        {
            FILE_DISPOSITION_INFO fdi;
            fdi.DeleteFile = TRUE;      //  Marking for deletion
            Success = SetFileInformationByHandle(
                DecompressedFile,
                FileDispositionInfo,
                &fdi,
                sizeof(FILE_DISPOSITION_INFO));    
            if (!Success) {
                wprintf(L"Cannot delete corrupted decompressed file.\n");
            }
        }
        CloseHandle(DecompressedFile); 
    }
}
```



 

 



