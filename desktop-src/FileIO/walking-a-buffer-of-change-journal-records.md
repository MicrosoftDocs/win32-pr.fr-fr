---
description: Comment retourner les enregistrements du journal des modifications qui répondent aux critères spécifiés.
ms.assetid: 8946adb5-da47-4711-8800-86f323081c4c
title: Parcours d’un tampon d’enregistrements de journal de modification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9384316e38c23951849006efc259268a7bdf33df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541213"
---
# <a name="walking-a-buffer-of-change-journal-records"></a><span data-ttu-id="b2c6d-103">Parcours d’un tampon d’enregistrements de journal de modification</span><span class="sxs-lookup"><span data-stu-id="b2c6d-103">Walking a Buffer of Change Journal Records</span></span>

<span data-ttu-id="b2c6d-104">Les codes de contrôle qui renvoient les enregistrements de journal de modification du numéro de séquence de mise à jour (USN), le [**\_ \_ \_ journal USN de lecture FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) et les [**\_ \_ \_ données USN d’énumération FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data), retournent des données similaires dans le tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="b2c6d-104">The control codes that return update sequence number (USN) change journal records, [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) and [**FSCTL\_ENUM\_USN\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data), return similar data in the output buffer.</span></span> <span data-ttu-id="b2c6d-105">Tous deux retournent un USN suivi de zéro, un ou plusieurs enregistrements de journal de modification, chacun dans une structure d’enregistrement [**USN \_ \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) ou [**USN \_ \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) .</span><span class="sxs-lookup"><span data-stu-id="b2c6d-105">Both return a USN followed by zero or more change journal records, each in a [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structure.</span></span>

<span data-ttu-id="b2c6d-106">Le volume cible des opérations USN doit être ReFS ou NTFS 3,0 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b2c6d-106">The target volume for USN operations must be ReFS or NTFS 3.0 or later.</span></span> <span data-ttu-id="b2c6d-107">Pour obtenir la version NTFS d’un volume, ouvrez une invite de commandes avec des droits d’accès administrateur et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b2c6d-107">To obtain the NTFS version of a volume, open a command prompt with Administrator access rights and execute the following command:</span></span>

<span data-ttu-id="b2c6d-108">**FSUtil.exe FSInfo NTFSInfo** *X \* \* * :**</span><span class="sxs-lookup"><span data-stu-id="b2c6d-108">**FSUtil.exe FSInfo NTFSInfo** *X\*\*\*:*\*</span></span>

<span data-ttu-id="b2c6d-109">où *X* est la lettre de lecteur du volume.</span><span class="sxs-lookup"><span data-stu-id="b2c6d-109">where *X* is the drive letter of the volume.</span></span>

<span data-ttu-id="b2c6d-110">La liste suivante identifie les façons d’accéder aux enregistrements de journal des modifications :</span><span class="sxs-lookup"><span data-stu-id="b2c6d-110">The following list identifies ways to get change journal records:</span></span>

-   <span data-ttu-id="b2c6d-111">Utilisez [**FSCTL \_ enum \_ USN \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) pour obtenir une liste (énumération) de tous les enregistrements de journal des modifications entre deux USN.</span><span class="sxs-lookup"><span data-stu-id="b2c6d-111">Use [**FSCTL\_ENUM\_USN\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) to get a listing (enumeration) of all change journal records between two USNs.</span></span>
-   <span data-ttu-id="b2c6d-112">Utilisez [**FSCTL \_ \_ \_ journal USN de lecture**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) pour être plus sélectif, par exemple en sélectionnant des raisons spécifiques de modifications ou en retournant lorsqu’un fichier est fermé.</span><span class="sxs-lookup"><span data-stu-id="b2c6d-112">Use [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) to be more selective, such as selecting specific reasons for changes or returning when a file is closed.</span></span>

> [!Note]  
> <span data-ttu-id="b2c6d-113">Ces deux opérations retournent uniquement le sous-ensemble d’enregistrements de journal de modification qui répondent aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="b2c6d-113">Both of these operations return only the subset of change journal records that meet the specified criteria.</span></span>

 

<span data-ttu-id="b2c6d-114">L’USN retourné comme premier élément de la mémoire tampon de sortie est l’USN du numéro d’enregistrement suivant à récupérer.</span><span class="sxs-lookup"><span data-stu-id="b2c6d-114">The USN returned as the first item in the output buffer is the USN of the next record number to be retrieved.</span></span> <span data-ttu-id="b2c6d-115">Utilisez cette valeur pour poursuivre la lecture des enregistrements à partir de la limite de fin.</span><span class="sxs-lookup"><span data-stu-id="b2c6d-115">Use this value to continue reading records from the end boundary forward.</span></span>

<span data-ttu-id="b2c6d-116">Le membre de **nom** de fichier de l’enregistrement [**USN \_ \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) ou de l' [**\_ enregistrement USN \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) contient le nom du fichier auquel s’applique l’enregistrement en question.</span><span class="sxs-lookup"><span data-stu-id="b2c6d-116">The **FileName** member of [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) contains the name of the file to which the record in question applies.</span></span> <span data-ttu-id="b2c6d-117">Le nom de fichier varie en fonction de la longueur, de sorte que l' **\_ enregistrement USN \_ v2** et l' **\_ enregistrement USN \_ v3** sont des structures de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="b2c6d-117">The file name varies in length, so **USN\_RECORD\_V2** and **USN\_RECORD\_V3** are variable length structures.</span></span> <span data-ttu-id="b2c6d-118">Son premier membre, **RecordLength**, est la longueur de la structure (y compris le nom de fichier), en octets.</span><span class="sxs-lookup"><span data-stu-id="b2c6d-118">Their first member, **RecordLength**, is the length of the structure (including the file name), in bytes.</span></span>

<span data-ttu-id="b2c6d-119">Lorsque vous travaillez avec le membre de **nom** de fichier de l' [**\_ enregistrement USN \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) et les structures d' [**\_ enregistrement USN \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) , ne supposez pas que le nom de fichier contient un \\ délimiteur de fin « 0 ».</span><span class="sxs-lookup"><span data-stu-id="b2c6d-119">When you work with the **FileName** member of [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structures, do not assume that the file name contains a trailing '\\0' delimiter.</span></span> <span data-ttu-id="b2c6d-120">Pour déterminer la longueur du nom de fichier, utilisez le membre **FileNameLength** .</span><span class="sxs-lookup"><span data-stu-id="b2c6d-120">To determine the length of the file name, use the **FileNameLength** member.</span></span>

<span data-ttu-id="b2c6d-121">L’exemple suivant appelle [**FSCTL \_ \_ \_ journal USN de lecture**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) et parcourt la mémoire tampon des enregistrements de journal des modifications que l’opération retourne.</span><span class="sxs-lookup"><span data-stu-id="b2c6d-121">The following example calls [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) and walks the buffer of change journal records that the operation returns.</span></span>


```C++
#include <Windows.h>
#include <WinIoCtl.h>
#include <stdio.h>

#define BUF_LEN 4096

void main()
{
   HANDLE hVol;
   CHAR Buffer[BUF_LEN];

   USN_JOURNAL_DATA JournalData;
   READ_USN_JOURNAL_DATA ReadData = {0, 0xFFFFFFFF, FALSE, 0, 0};
   PUSN_RECORD UsnRecord;  

   DWORD dwBytes;
   DWORD dwRetBytes;
   int I;

   hVol = CreateFile( TEXT("\\\\.\\c:"), 
               GENERIC_READ | GENERIC_WRITE, 
               FILE_SHARE_READ | FILE_SHARE_WRITE,
               NULL,
               OPEN_EXISTING,
               0,
               NULL);

   if( hVol == INVALID_HANDLE_VALUE )
   {
      printf("CreateFile failed (%d)\n", GetLastError());
      return;
   }

   if( !DeviceIoControl( hVol, 
          FSCTL_QUERY_USN_JOURNAL, 
          NULL,
          0,
          &JournalData,
          sizeof(JournalData),
          &dwBytes,
          NULL) )
   {
      printf( "Query journal failed (%d)\n", GetLastError());
      return;
   }

   ReadData.UsnJournalID = JournalData.UsnJournalID;

   printf( "Journal ID: %I64x\n", JournalData.UsnJournalID );
   printf( "FirstUsn: %I64x\n\n", JournalData.FirstUsn );

   for(I=0; I<=10; I++)
   {
      memset( Buffer, 0, BUF_LEN );

      if( !DeviceIoControl( hVol, 
            FSCTL_READ_USN_JOURNAL, 
            &ReadData,
            sizeof(ReadData),
            &Buffer,
            BUF_LEN,
            &dwBytes,
            NULL) )
      {
         printf( "Read journal failed (%d)\n", GetLastError());
         return;
      }

      dwRetBytes = dwBytes - sizeof(USN);

      // Find the first record
      UsnRecord = (PUSN_RECORD)(((PUCHAR)Buffer) + sizeof(USN));  

      printf( "****************************************\n");

      // This loop could go on for a long time, given the current buffer size.
      while( dwRetBytes > 0 )
      {
         printf( "USN: %I64x\n", UsnRecord->Usn );
         printf("File name: %.*S\n", 
                  UsnRecord->FileNameLength/2, 
                  UsnRecord->FileName );
         printf( "Reason: %x\n", UsnRecord->Reason );
         printf( "\n" );

         dwRetBytes -= UsnRecord->RecordLength;

         // Find the next record
         UsnRecord = (PUSN_RECORD)(((PCHAR)UsnRecord) + 
                  UsnRecord->RecordLength); 
      }
      // Update starting USN for next call
      ReadData.StartUsn = *(USN *)&Buffer; 
   }

   CloseHandle(hVol);

}
```



<span data-ttu-id="b2c6d-122">La taille en octets des enregistrements spécifiés par une structure d’enregistrement [**USN \_ \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) ou d' [**\_ enregistrement USN \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) est au plus `((MaxComponentLength - 1) * Width) + Size` où *MaxComponentLength* est la longueur maximale, en caractères, du nom du fichier d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b2c6d-122">The size in bytes of any record specified by a [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structure is at most `((MaxComponentLength - 1) * Width) + Size` where *MaxComponentLength* is the maximum length in characters of the record file name.</span></span> <span data-ttu-id="b2c6d-123">La largeur correspond à la taille d’un caractère large, et la *taille correspond à* la taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="b2c6d-123">The width is the size of a wide character, and the *Size* is the size of the structure.</span></span>

<span data-ttu-id="b2c6d-124">Pour obtenir la longueur maximale, appelez la fonction [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) et examinez la valeur désignée par le paramètre *lpMaximumComponentLength* .</span><span class="sxs-lookup"><span data-stu-id="b2c6d-124">To obtain the maximum length, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the value pointed to by the *lpMaximumComponentLength* parameter.</span></span> <span data-ttu-id="b2c6d-125">Soustraire un de *MaxComponentLength* pour tenir compte du fait que la définition de l’enregistrement [**USN \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) et de l' [**\_ enregistrement USN \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) comprend un caractère du nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="b2c6d-125">Subtract one from *MaxComponentLength* to account for the fact that the definition of [**USN\_RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) includes one character of the file name.</span></span>

<span data-ttu-id="b2c6d-126">Dans le langage de programmation C, la plus grande taille d’enregistrement possible est la suivante :</span><span class="sxs-lookup"><span data-stu-id="b2c6d-126">In the C programming language, the largest possible record size is the following:</span></span>

`(MaxComponentLength - 1) * sizeof(WCHAR) + sizeof(USN_RECORD)`

 

 
