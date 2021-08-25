---
description: Comment retourner les enregistrements du journal des modifications qui répondent aux critères spécifiés.
ms.assetid: 8946adb5-da47-4711-8800-86f323081c4c
title: Parcours d’un tampon d’enregistrements de journal de modification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9242d671cedfb5c9ef2b5fa836e29c455d09a9e1287b1ed035712f49c6c7d627
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830149"
---
# <a name="walking-a-buffer-of-change-journal-records"></a>Parcours d’un tampon d’enregistrements de journal de modification

Les codes de contrôle qui renvoient les enregistrements de journal de modification du numéro de séquence de mise à jour (USN), le [**\_ \_ \_ journal USN de lecture FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) et les [**\_ \_ \_ données USN d’énumération FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data), retournent des données similaires dans le tampon de sortie. Tous deux retournent un USN suivi de zéro, un ou plusieurs enregistrements de journal de modification, chacun dans une structure d’enregistrement [**USN \_ \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) ou [**USN \_ \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) .

Le volume cible des opérations USN doit être ReFS ou NTFS 3,0 ou une version ultérieure. Pour obtenir la version NTFS d’un volume, ouvrez une invite de commandes avec des droits d’accès administrateur et exécutez la commande suivante :

**FSUtil.exe FSInfo NTFSInfo** *X * * * :**

où *X* est la lettre de lecteur du volume.

La liste suivante identifie les façons d’accéder aux enregistrements de journal des modifications :

-   Utilisez [**FSCTL \_ enum \_ USN \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) pour obtenir une liste (énumération) de tous les enregistrements de journal des modifications entre deux USN.
-   Utilisez [**FSCTL \_ \_ \_ journal USN de lecture**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) pour être plus sélectif, par exemple en sélectionnant des raisons spécifiques de modifications ou en retournant lorsqu’un fichier est fermé.

> [!Note]  
> Ces deux opérations retournent uniquement le sous-ensemble d’enregistrements de journal de modification qui répondent aux critères spécifiés.

 

L’USN retourné comme premier élément de la mémoire tampon de sortie est l’USN du numéro d’enregistrement suivant à récupérer. Utilisez cette valeur pour poursuivre la lecture des enregistrements à partir de la limite de fin.

Le membre de **nom** de fichier de l’enregistrement [**USN \_ \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) ou de l' [**\_ enregistrement USN \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) contient le nom du fichier auquel s’applique l’enregistrement en question. Le nom de fichier varie en fonction de la longueur, de sorte que l' **\_ enregistrement USN \_ v2** et l' **\_ enregistrement USN \_ v3** sont des structures de longueur variable. Son premier membre, **RecordLength**, est la longueur de la structure (y compris le nom de fichier), en octets.

Lorsque vous travaillez avec le membre de **nom** de fichier de l' [**\_ enregistrement USN \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) et les structures d' [**\_ enregistrement USN \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) , ne supposez pas que le nom de fichier contient un \\ délimiteur de fin « 0 ». Pour déterminer la longueur du nom de fichier, utilisez le membre **FileNameLength** .

L’exemple suivant appelle [**FSCTL \_ \_ \_ journal USN de lecture**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) et parcourt la mémoire tampon des enregistrements de journal des modifications que l’opération retourne.


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



La taille en octets des enregistrements spécifiés par une structure d’enregistrement [**USN \_ \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) ou d' [**\_ enregistrement USN \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) est au plus `((MaxComponentLength - 1) * Width) + Size` où *MaxComponentLength* est la longueur maximale, en caractères, du nom du fichier d’enregistrement. La largeur correspond à la taille d’un caractère large, et la *taille correspond à* la taille de la structure.

Pour obtenir la longueur maximale, appelez la fonction [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) et examinez la valeur désignée par le paramètre *lpMaximumComponentLength* . Soustraire un de *MaxComponentLength* pour tenir compte du fait que la définition de l’enregistrement [**USN \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) et de l' [**\_ enregistrement USN \_ v3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) comprend un caractère du nom de fichier.

Dans le langage de programmation C, la plus grande taille d’enregistrement possible est la suivante :

`(MaxComponentLength - 1) * sizeof(WCHAR) + sizeof(USN_RECORD)`

 

 
