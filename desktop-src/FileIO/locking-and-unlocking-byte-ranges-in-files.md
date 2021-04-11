---
description: Exemple de code illustrant le verrouillage et le déverrouillage de la plage d’octets à l’aide des fonctions LockFileEx et UnlockFileEx.
ms.assetid: 9d54fe11-b1ad-4723-a42a-00bc6dc64072
title: Verrouillage et déverrouillage des plages d’octets dans les fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7789c56cea100d00168494fac97bdb46e036953c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320390"
---
# <a name="locking-and-unlocking-byte-ranges-in-files"></a>Verrouillage et déverrouillage des plages d’octets dans les fichiers

Bien que le système permet à plusieurs applications d’ouvrir un fichier et d’y écrire, les applications ne doivent pas écrire sur le travail de l’autre. Une application peut empêcher ce problème en verrouillant temporairement une plage d’octets dans un fichier.

Les fonctions [**lockfile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) et [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex) verrouillent une plage spécifiée d’octets dans un fichier. La plage peut s’étendre au-delà de la fin actuelle du fichier. Le verrouillage d’une partie d’un fichier donne aux threads du processus de verrouillage un accès exclusif à la plage d’octets spécifiée à l’aide du handle de fichier spécifié. Les tentatives d’accès à une plage d’octets verrouillée par un autre processus échouent toujours. Si le processus de verrouillage tente d’accéder à une plage d’octets verrouillés via un deuxième descripteur de fichier, la tentative échoue.

> [!Note]  
> Les fichiers mappés en mémoire ne sont pas pris en charge avec les verrous de plage d’octets.

 

La fonction [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex) permet à une application de spécifier l’un des deux types de verrous. Un *verrou exclusif* interdit à tous les autres processus d’accéder en lecture et en écriture à la plage d’octets spécifiée d’un fichier. Un *verrou partagé* refuse à tous les processus un accès en écriture à la plage d’octets spécifiée d’un fichier, y compris le processus qui verrouille d’abord la plage d’octets. Cela peut être utilisé pour créer une plage d’octets en lecture seule dans un fichier.

Une application déverrouille la plage d’octets à l’aide de la fonction [**UnlockFile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) ou [**UnlockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfileex) et doit déverrouiller toutes les zones verrouillées avant de fermer un fichier.

Pour obtenir un exemple d’utilisation de [**lockfile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile), consultez [Ajout d’un fichier à un autre fichier](appending-one-file-to-another-file.md).

Les exemples suivants montrent comment utiliser [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex). Le premier exemple est une démonstration simple pour créer un fichier, y écrire des données, puis verrouiller une section au milieu.

**Remarque**  Cet exemple ne modifie pas les données une fois que le fichier est verrouillé.


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved

#include <windows.h>
#include <stdio.h>
#include <stdlib.h>

#define NUMWRITES 10
#define TESTSTRLEN 11

const char TestData[NUMWRITES][TESTSTRLEN] = 
{ 
    "TestData0\n",
    "TestData1\n",
    "TestData2\n",
    "TestData3\n",
    "TestData4\n",
    "TestData5\n",
    "TestData6\n",
    "TestData7\n",
    "TestData8\n",
    "TestData9\n"
};

int main(int argc, char *argv[])
{
    BOOL fSuccess = FALSE;

    // Create the file, open for both read and write.
    HANDLE hFile = CreateFile(TEXT("datafile.txt"),
                       GENERIC_READ | GENERIC_WRITE,
                       0,          // open with exclusive access
                       NULL,       // no security attributes
                       CREATE_NEW, // creating a new temp file
                       0,          // not overlapped index/O
                       NULL);
    
    if (hFile == INVALID_HANDLE_VALUE) 
    {
        // Handle the error.
        printf("CreateFile failed (%d)\n", GetLastError());
        return (1);
    }

    // Write some data to the file.
    DWORD dwNumBytesWritten = 0;

    for (int i=0; i<NUMWRITES; i++)
    {
        fSuccess = WriteFile(hFile,
                             TestData[i],
                             TESTSTRLEN,
                             &dwNumBytesWritten,
                             NULL);  // sync operation.
        if (!fSuccess) 
        {
           // Handle the error.
           printf("WriteFile failed (%d)\n", GetLastError());
           return (2);
        }
    } 

    FlushFileBuffers(hFile);

    // Lock the 4th write-section.  
    // First, set up the Overlapped structure with the file offset 
    // required by LockFileEx, three lines in to the file.
    OVERLAPPED sOverlapped;
    sOverlapped.Offset = TESTSTRLEN * 3;
    sOverlapped.OffsetHigh = 0;

    // Actually lock the file.  Specify exclusive access, and fail 
    // immediately if the lock cannot be obtained.
    fSuccess = LockFileEx(hFile,         // exclusive access, 
                          LOCKFILE_EXCLUSIVE_LOCK | 
                          LOCKFILE_FAIL_IMMEDIATELY,
                          0,             // reserved, must be zero
                          TESTSTRLEN,    // number of bytes to lock
                          0,
                          &sOverlapped); // contains the file offset
    if (!fSuccess) 
    {
       // Handle the error.
       printf ("LockFileEx failed (%d)\n", GetLastError());
       return (3);
    }
    else printf("LockFileEx succeeded\n");

    /////////////////////////////////////////////////////////////////
    // Add code that does something interesting to locked section,  /
    // which should be line 4                                       /
    /////////////////////////////////////////////////////////////////

    // Unlock the file.
    fSuccess = UnlockFileEx(hFile, 
                            0,             // reserved, must be zero
                            TESTSTRLEN,    // num. of bytes to unlock
                            0,
                            &sOverlapped); // contains the file offset
    if (!fSuccess) 
    {
       // Handle the error.
       printf ("UnlockFileEx failed (%d)\n", GetLastError());
       return (4);
    }
    else printf("UnlockFileEx succeeded\n");

    // Clean up handles, memory, and the created file.
    fSuccess = CloseHandle(hFile);
    if (!fSuccess) 
    {
       // Handle the error.
       printf ("CloseHandle failed (%d)\n", GetLastError());
       return (5);
    }

    fSuccess = DeleteFile(TEXT("datafile.txt"));
    if (!fSuccess) 
    {
        // Handle the error.
       printf ("DeleteFile failed (%d)\n", GetLastError());
       return (6);
    }
    return (0);
}
```



L’exemple suivant est une démonstration avancée du verrouillage de plage d’octets, l’utilisation de plusieurs threads et d’une base de données simple effectuant des opérations aléatoires sur un seul fichier de données. Pour plus d’informations, consultez les commentaires de code incorporé et la section qui suit l’exemple de code.


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved

#define UNICODE
#define _CRT_RAND_S
#include <stdlib.h>
#include <windows.h>

#include <stdio.h>

#include <malloc.h>
#include <conio.h>
#include <process.h>
#include <winioctl.h>

#define RECORD_SIZE 0x300
#define NUM_RECORDS 0x1000
#define NUM_THREADS 8

#define NUM_FILEOPS 500

#define BITMAP_SIZE ((NUM_RECORDS) / 8)
#define DATA_SIZE   ((RECORD_SIZE) - sizeof(RECORD_HEADER))

#define MSG_PRINTF(S,...) wprintf(L"[THREAD_ID %d] " S, \
    GetCurrentThreadId(), \
    __VA_ARGS__)

#if defined BRLS_DEBUG

#define DBG_PRINTF(S,...) wprintf(L"[THREAD_ID %d] " S, \
    GetCurrentThreadId(), \
    __VA_ARGS__)

#else

#define DBG_PRINTF(...)
#define PrintBitmap(...)

#endif


#define MASTER_RECORD_TYPE_CODE 'rtsM'
#define DATA_RECORD_TYPE_CODE   'ataD'


//
//  Record type definitions.
//
typedef struct _RECORD_HEADER {
    ULONG TypeCode;     // Either MASTER_RECORD_TYPE_CODE or DATA_RECORD_TYPE_CODE.
    ULONG SeqNumber;    // Starts at 1 and is incremented every time contents are modified.
} RECORD_HEADER;

typedef struct _MASTER_RECORD {
    RECORD_HEADER Header;
    BYTE Bitmap[BITMAP_SIZE];  // A bitmap indicating which records are allocated.
} MASTER_RECORD;

typedef struct _DATA_RECORD {
    RECORD_HEADER Header;
    BYTE Data[DATA_SIZE];       // Record raw data.
} DATA_RECORD;


//
//  Types of I/O for IoRecord.
//
typedef enum {
    IoRead,
    IoWrite,
    IoLock,
    IoUnlock
} IO_TYPE;


//
//  Types of operations for OperateOnRecord.
//
typedef enum {
    CreateRecord = 0,
    DeleteRecord,
    ModifyRecord,
    MaxOprRecord
} OPERATION;


//
//  Parameter block for I/Os passed to IoRecord.
//
typedef struct _IO_PARAM {
    IO_TYPE Type;
    union _IO_PARAM_PARAMS {
        struct {
            PVOID Data;
            ULONG RecSize;
        } IoInfo;
        struct {
            BOOL Exclusive;
        } LockInfo ;
    } Params;
} IO_PARAM, *PIO_PARAM;

void ErrorExitThread()
//
//  This function is called immediately after an unrecoverable error is logged.
//
{
    MSG_PRINTF(L"An error has been logged, calling ExitThread.\n");
    ExitThread(1);
}

BOOL IoRecord(HANDLE hFile, ULONG RecNumber, PIO_PARAM pIoParam)
//
//  This function performs I/O (read, write, lock or unlock) in a record, according
//  to the parameters passed in the IO_PARAM block.
//
//  Arguments:
//      hFile       - Handle to the file containing the records.
//      RecNumber   - Number of the record to be operated on.
//      pIoParam    - Pointer to IO_PARAM structure.
//
//  Return value:
//      TRUE if the I/O succeeded, FALSE if not.
//
{
    OVERLAPPED Overlapped;
    BOOL Result;
    ULARGE_INTEGER RecOffset;
    DWORD NumBytes;

    //  Initialize Overlapped.
    SecureZeroMemory(&Overlapped, sizeof(OVERLAPPED));
    Overlapped.hEvent = CreateEvent(NULL,
        FALSE,
        FALSE,
        NULL);

    if (NULL == Overlapped.hEvent) 
    {
        MSG_PRINTF(L"CreateEvent for Overlapped.hEvent failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    //  Calculate record position.
    RecOffset.QuadPart = RecNumber * RECORD_SIZE;

    Overlapped.Offset     = RecOffset.LowPart;
    Overlapped.OffsetHigh = RecOffset.HighPart;

    //  Issue the operation.
    switch (pIoParam->Type) 
    {
    case IoLock:
        Result = LockFileEx(hFile,
            pIoParam->Params.LockInfo.Exclusive ? LOCKFILE_EXCLUSIVE_LOCK : 0,
            0,
            RECORD_SIZE,
            0,
            &Overlapped);
        break;
    case IoUnlock:
        Result = UnlockFileEx(hFile,
            0,
            RECORD_SIZE,
            0,
            &Overlapped);
        break;
    case IoRead:
        Result = ReadFile(hFile,
            pIoParam->Params.IoInfo.Data,
            pIoParam->Params.IoInfo.RecSize,
            NULL,
            &Overlapped);
        break;
    case IoWrite:
        Result = WriteFile(hFile,
            pIoParam->Params.IoInfo.Data,
            pIoParam->Params.IoInfo.RecSize,
            NULL,
            &Overlapped);
        break;
    default:
        Result = FALSE;
        break;
    }

    if (!Result) 
    {
        if (GetLastError() == ERROR_IO_PENDING) 
        {
            //  Wait until the operation finishes.
            if (GetOverlappedResult(hFile,
                &Overlapped,
                &NumBytes,
                TRUE) == FALSE) 
            {
                MSG_PRINTF(L"GetOverlappedResult for Overlapped.hEvent failed with error 0x%08x.\n", 
                    GetLastError());
                ErrorExitThread();
            }
            Result = TRUE;
        } else {
            MSG_PRINTF(L"IoRecord failed with error 0x%08x. Failure passed to caller.\n", 
                GetLastError());
        }
    }
    CloseHandle(Overlapped.hEvent);
    return Result;
}


//
//  The following functions are wrappers around IoRecord, they just set the correct
//  parameters in the IO_PARAM block to correspond to the requested operation and
//  pass that to IoRecord.
//
BOOL ReadRecord(HANDLE hFile, ULONG RecNumber, PVOID Record, ULONG RecSize)
{
    IO_PARAM IoParam;

    IoParam.Type                  = IoRead;
    IoParam.Params.IoInfo.Data    = Record;
    IoParam.Params.IoInfo.RecSize = RecSize;

    return IoRecord(hFile, RecNumber, &IoParam);
}


BOOL WriteRecord(HANDLE hFile, ULONG RecNumber, PVOID Record, ULONG RecSize)
{
    IO_PARAM IoParam;

    IoParam.Type                  = IoWrite;
    IoParam.Params.IoInfo.Data    = Record;
    IoParam.Params.IoInfo.RecSize = RecSize;

    return IoRecord(hFile, RecNumber, &IoParam);
}


BOOL LockRecord(HANDLE hFile, ULONG RecNumber, BOOL Exclusive)
{
    IO_PARAM IoParam;

    IoParam.Type                      = IoLock;
    IoParam.Params.LockInfo.Exclusive = Exclusive;

    return IoRecord(hFile, RecNumber, &IoParam);
}


BOOL UnlockRecord(HANDLE hFile, ULONG RecNumber)
{
    IO_PARAM IoParam;

    IoParam.Type = IoUnlock;

    return IoRecord(hFile, RecNumber, &IoParam);
}


ULONG ReserveFirstFreeRecord(BYTE* Bitmap)
//
//  This function iterates through the bitmap and reserves the first free record
//  it can find in the bitmap.
//
//  Arguments:
//      Bitmap  - Pointer to the bitmap.
//
//  Return value:
//      Either zero, if there are no free records, or the position of the record
//      that was just reserved.
//          
{
    int i;
    BYTE Bit = 1;

    for (i = 0; i < NUM_RECORDS; i++) 
    {
        if (Bitmap[i / 8] & Bit) 
        {
            Bit <<= 1;
            if (Bit == 0) { Bit = 1; }
        } else {
            Bitmap[i / 8] |= Bit;
            return i;
        }
    }

    return 0;
}


BOOL TestBit(BYTE* Bitmap, ULONG Bit)
//
//  This function tests if a given bit is set in the bitmap.
//
//  Arguments:
//      Bitmap  - Pointer to the bitmap.
//      Bit     - Position of the bit in the bitmap.
//
//  Return value:
//      TRUE if the bit is set, FALSE otherwise.
//
{
    ULONG Byte = Bit / 8;

    Bit = Bit % 8;

    return (BOOL)(Bitmap[Byte] & (1 << Bit));
}


void ClearBit(BYTE* Bitmap, ULONG Bit)
//
//  This function clears a given bit in the bitmap.
//
//  Arguments:
//      Bitmap  - Pointer to the bitmap.
//      Bit     - Position of the bit in the bitmap.
//
{
    ULONG Byte = Bit / 8;

    Bit = Bit % 8;

    Bitmap[Byte] &= ~(1 << Bit);
}


#ifdef BRLS_DEBUG
void PrintBitmap(BYTE* Bitmap)
//
//   This function prints the whole bitmap, for debugging purposes.
//
//   Arguments:
//      Bitmap  - Pointer to the bitmap.
//
{
    int i;

    for (i = 0; i < BITMAP_SIZE; i++) 
    {
        wprintf(L"%1x", Bitmap[i]);
    }

    wprintf(L"\n");
}
#endif


void InitRecord(RECORD_HEADER* Record, BOOL Master, ULONG SeqNumber)
//
//  This function initializes a in-memory record structure with the correct
//  type code and sequence number. In case of the Master Record, the bitmap
//  is initialized too.
//
//  Arguments:
//      Record      - Pointer to the record structure.
//      Master      - TRUE if this is a Master Record, FALSE otherwise.
//      SeqNumber   - Initial sequence number.
//
{
    ULONG RecSize   = Master ? sizeof(MASTER_RECORD)   : sizeof(DATA_RECORD);
    ULONG TypeCode  = Master ? MASTER_RECORD_TYPE_CODE : DATA_RECORD_TYPE_CODE;

    SecureZeroMemory(Record, RecSize);

    Record->TypeCode  = TypeCode;
    Record->SeqNumber = Master ? 0 : SeqNumber;

    if (Master) 
    {
        ((MASTER_RECORD*)Record)->Bitmap[0] = 1;
    }
}


DATA_RECORD* PrepareRecord(ULONG SeqNumber)
//
//  This function allocates a new in-memory record structure and initializes it
//  as a brand new data record.
//
//  Arguments:
//      SeqNumber   - Sequence number with which to initialize the record.
//
//  Return value:
//      Pointer to the record structure.
//
{
    DATA_RECORD* Record = NULL;

    Record = (DATA_RECORD*) malloc(sizeof(DATA_RECORD));

    if (Record == NULL) 
    {
        MSG_PRINTF(L"Critical error: malloc for CreateRecord failed.\n");
        ErrorExitThread();
    }

    InitRecord((RECORD_HEADER*)Record, FALSE, SeqNumber);

    return Record;
}


void WriteData(DATA_RECORD* Record)
//
//  This function fills a in-memory data record structure with random data.
//  Errors do not interrupt execution.
//
//  Arguments:
//      Record  - Pointer to the record structure.
//
{
    PUINT iData;
    int i;
    errno_t err;

    iData = (PUINT)Record->Data;

    for (i = 0; i < DATA_SIZE; i += sizeof(ULONG), iData++) 
    {
        err = rand_s(iData);
        if (err != 0) 
        {
            MSG_PRINTF(L"rand_s for WriteData failed with error 0x%08x, continuing execution.\n", 
                err);
        }
    }
}


BOOL OperateOnRecord(HANDLE hFile, PULONG RecNumber, OPERATION Operation)
//
//  This function executes a high-level operation in a record (create, modify or delete).
//
//  Arguments:
//      hFile       - Handle to the file containing the record to be operated on.
//      RecNumber   - Pointer to a ULONG that either will receive the number of the
//                    record created by this operation or just contains the number
//                    of the record that will be modified or deleted.
//      Operation   - Operation to be performed (CreateRecord, ModifyRecord or
//                    DeleteRecord).
//
//  Return value:
//      TRUE if the operation succeeded, FALSE otherwise.
//
{
    BOOL Result;
    BOOL Exists;
    BOOL ExclusiveLock;
    MASTER_RECORD MasterRecord;
    DATA_RECORD*  Record;

    //  Fail operations on Master Record.
    if ((Operation != CreateRecord) && (*RecNumber == 0)) 
    {
        MSG_PRINTF(L"Cannot operate on Master Record.\n");
        return FALSE;
    }

    //  Lock Master Record. If we're just modifying a record, we can get a
    //  shared lock.
    ExclusiveLock = (Operation != ModifyRecord);

    Result = LockRecord(hFile, 0, ExclusiveLock);
    if (!Result) 
    {
        MSG_PRINTF(L"LockRecord (MasterRecord) for OperateOnRecord failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    //  Read in Master Record.
    Result = ReadRecord(hFile, 0, (PVOID)&MasterRecord, sizeof(MASTER_RECORD));
    if (!Result) 
    {
        MSG_PRINTF(L"ReadRecord (MasterRecord) for OperateOnRecord failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    if (MasterRecord.Header.TypeCode != MASTER_RECORD_TYPE_CODE) 
    {
        MSG_PRINTF(L"Master Record corruption error: wrong typecode!\n");
        ErrorExitThread();
    }

    DBG_PRINTF(L"MasterRecord bitmap (before): ");
    PrintBitmap(MasterRecord.Bitmap);

    if (Operation != CreateRecord) 
    {
        //  Test the bit in the bitmap corresponding to this record.
        Exists = TestBit(MasterRecord.Bitmap, *RecNumber);

        //  Clear the bit if we are deleting the record.
        if ((Operation == DeleteRecord) && Exists) 
        {
            ClearBit(MasterRecord.Bitmap, *RecNumber);
        }

    } else {

        //  Reserve the first free record.
        *RecNumber = ReserveFirstFreeRecord(MasterRecord.Bitmap);

        if (*RecNumber != 0) 
        {
            Exists = TRUE;
        } else {
            Exists = FALSE;
            MSG_PRINTF(L"File is full!\n");
        }
    }

    DBG_PRINTF(L"MasterRecord bitmap (after): ");
    PrintBitmap(MasterRecord.Bitmap);

    if ((Operation != ModifyRecord) && Exists) 
    {
        //  Update the Master Record's sequence number.
        MasterRecord.Header.SeqNumber++;

        //  Write Master Record down.
        Result = WriteRecord(hFile, 0, (PVOID)&MasterRecord, sizeof(MASTER_RECORD));
        if (!Result) 
        {
            MSG_PRINTF(L"WriteRecord (MasterRecord) for CreateRecord failed with error 0x%08x.\n", 
                GetLastError());
            ErrorExitThread();
        }
    }

    //  Unlock Master Record.
    Result = UnlockRecord(hFile, 0);
    if (!Result) 
    {
        MSG_PRINTF(L"UnlockRecord (MasterRecord) for OperateOnRecord failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    if (!Exists) 
    {
        if (*RecNumber != 0) 
        {
            MSG_PRINTF(L"Record %d not present!\n", *RecNumber);
        }
        return FALSE;
    }

    //  For record deletion, processing is done and skip to write.
    //  Otherwise, there is more to do.
    if (Operation != DeleteRecord) 
    {
        //  Prepare a new record in memory.
        Record = PrepareRecord(1);

        //  Lock the record exclusively.
        Result = LockRecord(hFile, *RecNumber, TRUE);
        if (!Result) 
        {
            MSG_PRINTF(L"LockRecord for ModifyRecord failed with error 0x%08x.\n", 
                GetLastError());
            ErrorExitThread();
        }

        if (Operation == ModifyRecord) 
        {
            //  Read the record in from the file if we're modifying it.
            Result = ReadRecord(hFile, *RecNumber, Record, RECORD_SIZE);
            if (!Result) 
            {
                MSG_PRINTF(L"ReadRecord for ModifyRecord failed with error 0x%08x.\n", 
                    GetLastError());
                ErrorExitThread();
            }

            //  Update record sequence number.
            Record->Header.SeqNumber++;
        }

        //  Write to the in-memory record.
        WriteData(Record);

        //  Write the record to the file.
        Result = WriteRecord(hFile, *RecNumber, Record, RECORD_SIZE);
        if (!Result) 
        {
            MSG_PRINTF(L"WriteRecord for ModifyRecord failed with error 0x%08x.\n", 
                GetLastError());
            ErrorExitThread();
        }

        //  Unlock the record.
        Result = UnlockRecord(hFile, *RecNumber);
        if (!Result) 
        {
            MSG_PRINTF(L"UnlockRecord for ModifyRecord failed with error 0x%08x.\n", 
                GetLastError());
            ErrorExitThread();
        }

        //  Free the record structure.
        free(Record);
    }

    return TRUE;
}


ULONG RandomOption(ULONG NumOpts)
//
//  This function returns a random number between 0 and (NumOpts - 1).
//  It basically is a random option select.
//
//  Arguments:
//      NumOpts - Number of options to choose from.
//
//  Return value:
//      A random option (random ULONG x | 0 <= x < NumOpts).
//
{
    UINT Random;
    errno_t err;

    err = rand_s(&Random);
    if (err != 0) 
    {
        MSG_PRINTF(L"rand_s for RandomOption failed with error 0x%08x\n", 
            err);
    }

    return Random % NumOpts;
}


DWORD WINAPI WorkerThread(PVOID data)
//
//  This is the tight loop executed by each of the threads operating in the file.
//  Each thread has its own handle to the same file. After obtaining that handle,
//  they go into a tight loop in which a record number and a record operation are
//  chosen at random and that operation is then performed in that record.
//
//  Arguments:
//      Data    - PVOID to a string containing the file name (so it can be opened).
//
//  Return value:
//      It should not return.
//
{
    HANDLE hFile;
    LPCWSTR FileName = (LPCWSTR)data;
    ULONG RecNumber;
    OPERATION Operation;
    BOOL Result;

    UINT i;

    hFile = CreateFile(FileName,
        GENERIC_READ | GENERIC_WRITE,
        FILE_SHARE_READ | FILE_SHARE_WRITE,
        NULL,
        OPEN_EXISTING,
        FILE_ATTRIBUTE_NORMAL | FILE_FLAG_OVERLAPPED,
        NULL);

    if (hFile == INVALID_HANDLE_VALUE) 
    {
        MSG_PRINTF(L"CreateFile failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    //  Main loop for doing the random operations.
    for (i = 0; i < NUM_FILEOPS; i++) 
    {
        RecNumber = RandomOption(NUM_RECORDS);
        Operation = (OPERATION)RandomOption(MaxOprRecord);

        //  Output message as to what action is being attempted.
        switch (Operation) 
        {
        case CreateRecord:
            MSG_PRINTF(L"attempting record creation.\n");
            break;
        case ModifyRecord:
            MSG_PRINTF(L"attempting modification of record %d.\n", RecNumber);
            break;
        case DeleteRecord:
            MSG_PRINTF(L"attempting deletion of record %d.\n", RecNumber);
            break;
        }

        //  Perform the actual operation and handle the result, 
        //  then loop again until done.
        Result = OperateOnRecord(hFile, &RecNumber, Operation);

        if (Result) 
        {
            switch (Operation) 
            {
            case CreateRecord:
                MSG_PRINTF(L"created record %d.\n", RecNumber);
                break;

            case ModifyRecord:
                MSG_PRINTF(L"modified record %d.\n", RecNumber);
                break;

            case DeleteRecord:
                MSG_PRINTF(L"deleted record %d.\n", RecNumber);
                break;
            }
        }
    }

    CloseHandle(hFile);
    MSG_PRINTF(L"%d file operations complete. Exiting thread.\n", i);

    return 0;
}


BOOL InitNewFile(LPCWSTR FileName)
//
//  This function initializes a file with records. If the file already exists, it
//  just returns, assuming it has a valid Master Record on it. If it does not 
//  exist, a brand new file is created and initialized with a clean Master Record.
//
//  Arguments:
//      FileName    - Name of the file to be initialized.
//
//  Return value:
//      TRUE if the initialization succeeded, FALSE otherwise.
//      
{
    HANDLE hFile;
    MASTER_RECORD MasterRecord;
    DWORD BytesWritten;
    DWORD Result;

    //
    //  Create the file or open existing.
    //
    hFile = CreateFile(FileName,
        GENERIC_READ | GENERIC_WRITE,
        FILE_SHARE_READ | FILE_SHARE_WRITE,
        NULL,
        OPEN_ALWAYS,
        FILE_ATTRIBUTE_NORMAL,
        NULL);

    if (INVALID_HANDLE_VALUE == hFile) 
    {
        MSG_PRINTF(L"CreateFile failed with error 0x%08x.\n", 
            GetLastError());
        return FALSE;
    } 
    else if (ERROR_ALREADY_EXISTS == GetLastError()) 
    {
        //  This is ok, simply assume it's a valid file.
        //  Note that this does not actually test that the file
        //  is valid for this application. That error is caught later.
        CloseHandle(hFile);
        return TRUE;
    } //  The implied "else" is that the handle is a good one.


    InitRecord((RECORD_HEADER*)&MasterRecord, TRUE, 0);

    Result = WriteFile(hFile,
        &MasterRecord,
        sizeof(MASTER_RECORD),
        &BytesWritten,
        NULL);

    if (!Result) 
    {
        MSG_PRINTF(L"WriteFile failed with error 0x%08x.\n", 
            GetLastError());
    }

    CloseHandle(hFile);

    return Result;
}


int __cdecl wmain(int argc, LPCWSTR argv[])
//
//  Main function. Reads file name from command line argument, initializes the file
//  and starts the worker threads, waiting for them to return.
//
{
    HANDLE gThread[NUM_THREADS];

    DWORD IdThread;
    DWORD ResultCode;
    LPCWSTR FileName = NULL;

    if (argc != 2) {
        wprintf(L"Invalid number of arguments!\n");
        wprintf(L"Usage: %ws file_name\n", argv[0]);
        return -1;
    }

    FileName = argv[1];

    if (!InitNewFile(FileName))
    {
        wprintf(L"Unable to initialize the data file %ws.\n", FileName);
    }

    wprintf(L"Main thread creating %d worker threads for processing.\n", 
        NUM_THREADS);
    for (int i = 0; i < NUM_THREADS; i++) 
    {
        gThread[i] = CreateThread(NULL,
            0,
            (LPTHREAD_START_ROUTINE)WorkerThread,
            (PVOID)FileName,
            0,
            &IdThread);
    }

    wprintf(L"Main thread waiting for worker threads to exit...\n");

    ResultCode = WaitForMultipleObjects(
        NUM_THREADS,
        gThread,
        TRUE,
        INFINITE);

    wprintf(L"WaitForMultipleObjects returned 0x%08x, execution complete.\n",
        ResultCode);

    // Do some clean-up.
    for (int i = 0; i < NUM_THREADS; i++) 
    {
        CloseHandle(gThread[i]);
    }

    return 0;
}
```



Cet exemple est une application console Windows qui exécute plusieurs accès simultanés à un fichier, tous coordonnés par des verrous de plage d’octets à l’aide d’une base de données simple, composée de plusieurs enregistrements d’une taille fixe. Notez que la vraie simultanéité dépend du nombre de cœurs de processeurs présents sur le système hôte.

Tous les enregistrements ont les deux premiers champs en commun : un code de type et un numéro de séquence. Le code de type est l’un des deux codes suivants : le code « Master » fait référence au type d' **\_ enregistrement principal** et le code « Data » fait référence à un type d' **\_ enregistrement de données** . Il ne peut y avoir qu’un seul **\_ enregistrement principal** et zéro ou plusieurs **\_ enregistrements de données**. Pour cet exemple, les données contenues dans les enregistrements de données sont générées de manière aléatoire. Le deuxième champ, le numéro de séquence, est incrémenté chaque fois qu’un enregistrement est modifié.

Au début de l’exécution, si le fichier de données n’existe pas encore, il est créé et initialisé par la fonction **InitNewFile** . La fonction **InitNewFile** écrit un enregistrement de type Master avec une bitmap vide au début. Si le fichier existe déjà, il est ouvert ; Il est supposé avoir un enregistrement maître valide au début.

Une fois le fichier créé ou correctement ouvert, plusieurs threads de travail sont démarrés, et tous exécutent une boucle dans laquelle une opération et un enregistrement sont choisis au hasard, puis cette opération est tentée sur cet enregistrement. Étant donné que ces opérations sont aléatoires, elles ne sont pas toutes exécutées correctement, mais ne sont pas nécessairement des erreurs. Les informations d’État appropriées sont enregistrées dans la console.

Les opérations possibles sont les suivantes : la création d’un nouvel enregistrement, la modification d’un enregistrement existant ou la suppression d’un enregistrement existant. L’opération de création examine le bitmap pour trouver le premier enregistrement gratuit et alloue cet enregistrement en tant que nouvel enregistrement. L’opération de modification lit le bitmap pour voir si cet enregistrement existe réellement et, le cas échéant, modifie cet enregistrement. L’opération de suppression efface le bit de l’image bitmap correspondant à l’enregistrement, ce qui libère l’espace occupé par l’enregistrement pour une allocation future. En outre, ces opérations sont divisées en deux parties : l’accès à MasterRecord, où les métadonnées sont stockées et l’accès à l’enregistrement de données lui-même.

Étant donné qu’ils écrivent des données dans les enregistrements de données, les opérations de création d’enregistrement et de modification d’enregistrement sont les seules qui nécessitent un accès à l’enregistrement des données. Pour cette raison, la région couverte par l’enregistrement est verrouillée exclusivement avant l’opération en cours d’exécution. Les opérations de création et de suppression modifient la bitmap, afin qu’elles aient besoin de verrouiller exclusivement l’enregistrement maître. Toutefois, les opérations de modification d’enregistrement n’ont besoin que de lire la bitmap, pas d’y écrire, afin de vérifier si le fichier existe. Pour cette opération, l’enregistrement maître a uniquement besoin d’un verrou de plage d’octets partagé.

Les verrous de plage d’octets exclusifs empêchent l’accès en lecture et en écriture à tous les autres handles du fichier, et c’est la raison pour laquelle ils sont utilisés lors de l’écriture dans un enregistrement. En revanche, un verrou de plage d’octets partagé empêche l’accès en écriture à partir de tous les descripteurs, y compris le handle propriétaire du verrou, mais autorise l’accès en lecture à tous les.

Pour illustrer l’utilisation de verrous de plage d’octets avec le fichier, toutes les e/s de cet exemple, à l’exception de la nouvelle initialisation de fichier, s’effectuent via un handle de fichier asynchrone. Cela peut être observé dans la fonction **IoRecord** dans les cas **IoLock** et **IoUnlock** au sein de l’instruction switch. Les fonctions [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex) et [**UnlockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfileex) sont utilisées avec le modèle d’e/s avec chevauchement en passant une structure [**OVERLAPPED**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) à celles-ci avec le décalage pour le début de la plage verrouillée, et un événement qui est signalé après que le verrou sur cette plage a été accordé, sauf si la fonction est retournée immédiatement.

Après l’émission de la requête d’e/s asynchrone, l’opération suivante dans la fonction **IoRecord** consiste à attendre l’opération en ligne. Il s’agit souvent d’un scénario sous-optimal lorsque les performances maximales sont souhaitées et sont utilisées ici pour des raisons de simplicité. Dans les applications de production, l’utilisation de [ports de terminaison d’e/s](i-o-completion-ports.md) ou de mécanismes similaires est préférable, car elle libère les threads pour effectuer d’autres traitements pendant que l’e/s se termine.

L’exemple se termine après l’exécution de **num \_ FILEOPS** Random Operations. Chaque thread enregistre son état d’arrêt comme une condition d’erreur ou un arrêt normal. Notez que les threads ne se terminent pas tous en même temps, en fonction du nombre de cœurs de processeurs du système hôte et de la vitesse du sous-système d’e/s.

 

 



