---
description: L’exemple suivant illustre l’utilisation de l’API de compression en mode bloc.
ms.assetid: 7483BCE4-3B85-4659-98E3-670D2F7EE52D
title: Utilisation de l’API de compression en mode bloc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddd1ecaec03d332262ffb24462e73a9fcb789d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111455"
---
# <a name="using-the-compression-api-in-block-mode"></a>Utilisation de l’API de compression en mode bloc

L’exemple suivant illustre l’utilisation de l’API de compression en mode bloc. Pour générer un compresseur ou un décompresseur à l’aide du mode bloc, votre application doit inclure l’indicateur de **compression \_ brut** quand elle appelle [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) ou [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor). Le mode blocage permet au développeur de contrôler la taille du bloc, mais nécessite davantage de travail par l’application.

Le mode bloc échoue si la taille de la mémoire tampon d’entrée est supérieure à la taille de bloc interne de l’algorithme de compression. La taille de bloc interne est de 32 Ko pour MSZIP et 1 Go pour les algorithmes de compression XPRESS. La taille de bloc interne pour LZMS peut être configurée jusqu’à 64 Go avec une augmentation correspondante de l’utilisation de la mémoire. La valeur du paramètre *UncompressedBufferSize* de la [**décompression**](/windows/desktop/api/compressapi/nf-compressapi-decompress) doit être exactement égale à la taille d’origine des données non compressées, et pas seulement à la taille de la mémoire tampon de sortie. Cela signifie que votre application doit spécifier la taille de bloc et enregistrer la taille d’origine exacte des données non compressées pour une utilisation par le décompresseur. La taille de la mémoire tampon compressée n’est pas enregistrée automatiquement, et l’application doit également l’enregistrer pour la décompression.

Le mode mémoire tampon est recommandé dans la plupart des cas, car il fractionne automatiquement la mémoire tampon d’entrée en blocs d’une taille appropriée pour l’algorithme de compression sélectionné stocke la taille de la mémoire tampon non compressée dans la mémoire tampon compressée. Pour plus d’informations sur l’utilisation du mode mémoire tampon, consultez [utilisation de l’API de compression en mode mémoire tampon](using-the-compression-api-in-buffer-mode.md).

Les applications qui utilisent le mode mémoire tampon ou bloc ont la possibilité de spécifier une routine d’allocation de mémoire personnalisée dans son appel à [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) ou [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor).

**Windows 8 et Windows Server 2012 :** Pour utiliser l’exemple de code suivant, vous devez exécuter Windows 8 ou Windows Server 2012 et disposer de « compressapi. h » et de « cabinet.dll » et d’un lien vers le fichier « cabinet. lib ».

L’exemple suivant illustre l’utilisation de l’API de compression en mode bloc pour compresser un fichier à l’aide de l’algorithme de compression LZMS et d’une routine d’allocation de mémoire personnalisée. Votre application doit inclure l’indicateur de compression **\_ brut** pour utiliser l’API de compression en mode bloc. Tout d’abord, l’application appelle [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) avec l' **\_ algorithme compress \_ LZMS** \| **compresser \_ RAW** pour générer le compresseur. Le paramètre *AllocationRoutines* spécifie la routine d’allocation de mémoire. L’application définit ensuite la taille de bloc pour le compresseur à l’aide de [**SetCompressorInformation**](/windows/desktop/api/compressapi/nf-compressapi-setcompressorinformation).

L’application effectue des appels répétés à [**compresser**](/windows/desktop/api/compressapi/nf-compressapi-compress) pour compresser le bloc de données par bloc. L’application écrit la taille de bloc non compressée, la taille de bloc compressée et les données compressées dans la mémoire tampon de sortie.


```C++
#include <Windows.h>
#include <stdio.h>
#include <compressapi.h>

#define META_DATA_SIZE (2 * sizeof(ULONG))
#define BLOCK_SIZE (1 * 1024 * 1024)                //  Block size is 1MB

PVOID SimpleAlloc(PVOID Context, SIZE_T Size)
{
    UNREFERENCED_PARAMETER(Context);
    return malloc(Size);
}

VOID SimpleFree(PVOID Context, PVOID Memory)
{
    UNREFERENCED_PARAMETER(Context);
    if (Memory != NULL)
    {
        free(Memory);
    }
    return;
}

BOOL BlockModeCompress(
    _In_ PBYTE InputData, 
    _In_ DWORD InputSize, 
    _Deref_out_opt_ PBYTE *OutputData, 
    _Out_ DWORD *CompressedSize
    )
{
    COMPRESSOR_HANDLE Compressor    = NULL;
    DWORD ProcessedSoFar            = 0;
    SIZE_T OutputSoFar              = 0;
    DWORD CurrentBlockSize          = 0;
    SIZE_T CompressedDataSize       = 0;
    SIZE_T CompressedBlockSize      = 0;
    SIZE_T OutputDataSize           = 0;  
    BOOL Success                    = FALSE;

    //  Set maximum input block size for compressor.
    DWORD BlockSize                    = BLOCK_SIZE;

    COMPRESS_ALLOCATION_ROUTINES AllocationRoutines;

    //  Init. allocation routines
    AllocationRoutines.Allocate = SimpleAlloc;
    AllocationRoutines.Free = SimpleFree;
    AllocationRoutines.UserContext = NULL;

    *CompressedSize = 0;
    *OutputData = NULL;

    //  Create a LZMS compressor and set to Block mode.
    Success = CreateCompressor(
        COMPRESS_ALGORITHM_LZMS|COMPRESS_RAW,   //  Compression algorithm is LZMS
        &AllocationRoutines,                    //  Optional Memory allocation routines
        &Compressor);                           //  Handle

    if (!Success)
    {
        wprintf(L"Cannot create compressor handle: %d\n", GetLastError());
        goto done;
    }

    Success = SetCompressorInformation(
        Compressor,
        COMPRESS_INFORMATION_CLASS_BLOCK_SIZE,  //  Set block size for LZMS compressor
        &BlockSize,                             //  Block size information
        sizeof(DWORD));                         //  Information size

    if (!Success)
    {
        wprintf(L"Set compressor information error: %d\n", GetLastError());
        goto done;
    }     

    //  Query max. possible compressed block size.
    Success = Compress(
        Compressor,                 //  Compressor Handle
        NULL,                       //  Input buffer, Uncompressed data
        BlockSize,                  //  Uncompressed block size
        NULL,                       //  Compressed Buffer
        0,                          //  Compressed Buffer size
        &CompressedBlockSize);      //  Compressed Data size

    if (!Success)
    {
        DWORD ErrorCode = GetLastError();
        if (ErrorCode != ERROR_INSUFFICIENT_BUFFER)
        {
            wprintf(L"Query compressed block size error: %d\n", GetLastError());
            goto done;
        }
    }

    //  Get max. possible size for compressed data for given input data    
    OutputDataSize = (InputSize % BLOCK_SIZE == 0) ? 0 : 1;
    OutputDataSize += InputSize / BLOCK_SIZE;
    OutputDataSize = OutputDataSize * (META_DATA_SIZE + CompressedBlockSize) + sizeof(ULONG);

    *OutputData = (PBYTE)malloc(OutputDataSize);
    if (!*OutputData)
    {
        wprintf(L"Cannot allocate memory for compressed buffer.\n");
        Success = FALSE;
        goto done;       
    }

    //  Write uncompressed size to beginning of the buffer
    *((ULONG UNALIGNED *)*OutputData) = InputSize;
    OutputSoFar = sizeof(ULONG);

    //  Compress data block by block.
    while (ProcessedSoFar < InputSize)
    {
        if (OutputSoFar + META_DATA_SIZE >= OutputDataSize) 
        {
            Success = FALSE;
            wprintf(L"Compression fails.\n");
            goto done;
        }                      

        CurrentBlockSize = 
            (InputSize - ProcessedSoFar < BlockSize) ?
            (InputSize - ProcessedSoFar) : BlockSize;

        //  Compress a block.
        Success = Compress(
            Compressor,                                     //  Compressor Handle
            InputData + ProcessedSoFar,                     //  Uncompressed data
            CurrentBlockSize,                               //  Uncompressed data size
            *OutputData + OutputSoFar + META_DATA_SIZE,     //  Start of compressed buffer
            OutputDataSize - OutputSoFar - META_DATA_SIZE,  //  Compressed block size
            &CompressedDataSize);                           //  Compressed data size

        if (!Success) 
        {
            wprintf(L"Compression fails: %d\n", GetLastError());
            goto done;
        }

        //  Write block information to output data.
        *((ULONG UNALIGNED *)(*OutputData + OutputSoFar)) = (ULONG)CompressedDataSize;
        OutputSoFar += sizeof(ULONG);
        *((ULONG UNALIGNED *)(*OutputData + OutputSoFar)) = (ULONG)CurrentBlockSize;
        OutputSoFar += sizeof(ULONG);
        OutputSoFar += CompressedDataSize;

        ProcessedSoFar += CurrentBlockSize;
    }    
    
    
    if (OutputSoFar > UINT32_MAX)
    {
        *CompressedSize = 0;
        Success = FALSE;
    }
    else
    {
        *CompressedSize = static_cast<DWORD>(OutputSoFar);
    }

done:
    if (Compressor != NULL)
    {
        CloseCompressor(Compressor);
    }
    return Success;
}

void wmain(_In_ int argc, _In_ WCHAR *argv[])
{
    PBYTE CompressedBuffer          = NULL;
    PBYTE InputBuffer               = NULL;
    HANDLE InputFile                = INVALID_HANDLE_VALUE;
    HANDLE CompressedFile           = INVALID_HANDLE_VALUE;    
    BOOL DeleteTargetFile           = TRUE;
    BOOL Success;
    SIZE_T CompressedDataSize;
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
        wprintf(L"Cannot allocate memory for input buffer.\n");
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

    StartTime = GetTickCount64();

    //  Call BlockModeCompress() again to do compression.    
    Success = BlockModeCompress(        
        InputBuffer,            //  Input buffer, Uncompressed data
        InputFileSize,          //  Uncompressed data size
        &CompressedBuffer,      //  Compressed Buffer
        &CompressedDataSize);   //  Compressed Data size

    if (!Success)
    {
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
        wprintf(L"Cannot write compressed data to file: %d\n", GetLastError());
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



L’exemple suivant illustre la décompression de fichier à l’aide de l’API de compression en mode bloc.


```C++
#include <Windows.h>
#include <stdio.h>
#include <compressapi.h>

#define META_DATA_SIZE (2 * sizeof(ULONG))

PVOID SimpleAlloc(PVOID Context, SIZE_T Size)
{
    UNREFERENCED_PARAMETER(Context);
    return malloc(Size);
}

VOID SimpleFree(PVOID Context, PVOID Memory)
{
    UNREFERENCED_PARAMETER(Context);
    if (Memory != NULL)
    {
        free(Memory);
    }
    return;
}

BOOL BlockModeDecompress(
    _In_ PBYTE InputData, 
    _In_ DWORD InputSize, 
    _Deref_out_opt_ PBYTE *OutputData, 
    _Out_ DWORD *DecompressedSize
    )
{
    DECOMPRESSOR_HANDLE Decompressor    = NULL;
    DWORD ProcessedSoFar                = 0;    
    DWORD CompressedBlockSize           = 0;
    DWORD UncompressedBlockSize         = 0;
    DWORD DecompressedSoFar             = 0;
    DWORD OutputDataSize                = 0;
    BOOL Success                        = FALSE;

    COMPRESS_ALLOCATION_ROUTINES AllocationRoutines;

    //  Init. allocation routines
    AllocationRoutines.Allocate = SimpleAlloc;
    AllocationRoutines.Free = SimpleFree;
    AllocationRoutines.UserContext = NULL;

    *DecompressedSize = 0;
    *OutputData = NULL;

    //  Create a LZMS decompressor and set to Block mode.
    Success = CreateDecompressor(
        COMPRESS_ALGORITHM_LZMS|COMPRESS_RAW,   //  Compression algorithm is LZMS
        &AllocationRoutines,                    //  Memory allocation routines
        &Decompressor);                         //  handle

    if (!Success)
    {
        wprintf(L"Cannot create decompressor handle: %d\n", GetLastError());
        goto done;
    }

    //  Read uncompressed size
    ProcessedSoFar = 0;
    OutputDataSize = *((ULONG UNALIGNED *)(InputData + ProcessedSoFar));
    ProcessedSoFar += sizeof(ULONG);

    *OutputData = (PBYTE)malloc(OutputDataSize);
    if (!*OutputData)
    {
        wprintf(L"Cannot allocate memory for uncompressed buffer.\n");
        Success = FALSE;
        goto done;
    }  

    //  Decompress data block by block.
    while (ProcessedSoFar < InputSize)
    {
        if (ProcessedSoFar + META_DATA_SIZE > InputSize)
        {
            Success = FALSE;
            wprintf(L"Data corrupt.\n");
            goto done;     
        }

        //  Read block information.
        CompressedBlockSize = *((ULONG UNALIGNED *)(InputData + ProcessedSoFar));
        ProcessedSoFar += sizeof(ULONG);
        UncompressedBlockSize = *((ULONG UNALIGNED *)(InputData + ProcessedSoFar));
        ProcessedSoFar += sizeof(ULONG);

        if (ProcessedSoFar + CompressedBlockSize > InputSize)
        {
            Success = FALSE;
            wprintf(L"Data corrupt.\n");
            goto done;     
        }

        if (DecompressedSoFar + UncompressedBlockSize > OutputDataSize)
        {
            Success = FALSE;
            wprintf(L"Output buffer not enough to hold decompressed data.\n");
            goto done;     
        }

        //  Decompress a block
        Success = Decompress(
            Decompressor,                   //  Decompressor Handle
            InputData + ProcessedSoFar,     //  Compressed data
            CompressedBlockSize,            //  compressed data size
            *OutputData + DecompressedSoFar, //  Start of decompressed buffer
            UncompressedBlockSize,          //  Uncompressed block size
            NULL);                          //  Decompressed data size
        if (!Success) 
        {
            wprintf(L"Decompression failure: %d\n", GetLastError());
            goto done;
        }
        ProcessedSoFar += CompressedBlockSize;
        DecompressedSoFar += UncompressedBlockSize;
    }

    *DecompressedSize = DecompressedSoFar;

done:
    if (Decompressor != NULL)
    {
        CloseDecompressor(Decompressor);
    }
    return Success;
}

void wmain(_In_ int argc, _In_ WCHAR *argv[])
{       
    PBYTE CompressedBuffer              = NULL;
    PBYTE DecompressedBuffer            = NULL;
    HANDLE InputFile                    = INVALID_HANDLE_VALUE;
    HANDLE DecompressedFile             = INVALID_HANDLE_VALUE;    
    BOOL DeleteTargetFile               = TRUE;    
    BOOL Success;
    DWORD DecompressedDataSize;
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

    //  Allocate memory for compressed content.
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
            
    StartTime = GetTickCount64();

    //  Decompress data and write data to DecompressedBuffer.
    Success = BlockModeDecompress(        
        CompressedBuffer,           //  Compressed data
        InputFileSize,              //  Compressed data size
        &DecompressedBuffer,        //  Decompressed buffer        
        &DecompressedDataSize);     //  Decompressed data size

    if (!Success)
    {
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



Une application utilisant le mode mémoire tampon ou bloc a la possibilité de personnaliser l’allocation de mémoire utilisée par l’API de compression lorsqu’elle appelle [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) ou [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor). En mode bloc, l’application doit gérer les informations de bloc de compression, telles que la taille des données compressées et la taille des données non compressées. dans le cas contraire, la [**décompression**](/windows/desktop/api/compressapi/nf-compressapi-decompress) ne pourra pas décompresser les informations.

L’extrait de code suivant montre une routine d’allocation personnalisée simple.


```C++
PVOID SimpleAlloc(PVOID Context, SIZE_T Size)
{
return malloc(Size);
}

VOID SimpleFree(PVOID Context, PVOID Memory)
{
if (Memory != NULL)
{
        free(Memory);
}
return;
}

//  Init. allocation routines
AllocationRoutines.Allocate = SimpleAlloc;
AllocationRoutines.Free = SimpleFree;
AllocationRoutines.UserContext = NULL;
```



 

 



