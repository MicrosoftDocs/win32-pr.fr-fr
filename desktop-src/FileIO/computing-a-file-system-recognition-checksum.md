---
description: La structure de la structure de reconnaissance du système de fichiers \_ \_ \_ , définie en interne par Windows et utilisée par la reconnaissance du système de fichiers (FRS), contient une valeur de somme de contrôle qui doit être correctement calculée pour que le service de réplication de fichiers fonctionne correctement avec un système de fichiers non reconnu spécifié.
ms.assetid: 8f76784f-7d03-4874-ae7f-e8bdc42638c3
title: Calcul d’une somme de contrôle de reconnaissance du système de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cac3975d4e1845dd1ff4aa218526e942fda152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953182"
---
# <a name="computing-a-file-system-recognition-checksum"></a>Calcul d’une somme de contrôle de reconnaissance du système de fichiers

La structure de la structure de reconnaissance du système de fichiers, définie en interne par Windows et utilisée par la [reconnaissance du système de fichiers](file-system-recognition.md) (FRS), contient une valeur de somme de contrôle qui doit être correctement calculée pour que le service de réplication de fichiers fonctionne correctement avec un système de fichiers non reconnu spécifié. [**\_ \_ \_**](file-system-recognition-structure.md) L’exemple suivant effectue ce calcul.


```C++
typedef struct _FILE_SYSTEM_RECOGNITION_STRUCTURE {
  UCHAR  Jmp[3];
  UCHAR  FsName[8];
  UCHAR  MustBeZero[5];
  ULONG  Identifier;
  USHORT Length;
  USHORT Checksum;
} FILE_SYSTEM_RECOGNITION_STRUCTURE, *PFILE_SYSTEM_RECOGNITION_STRUCTURE;

USHORT ComputeFileSystemInformationChecksum (
    __in PFILE_SYSTEM_RECOGNITION_STRUCTURE Fsrs
    )

/*++

Routine Description:

    This routine computes the file record checksum.

Arguments:

    Fsrs - Pointer to the record.

Return Value:

    The checksum result.

--*/

{
    USHORT Checksum = 0;
    USHORT i;
    PUCHAR Buffer = (PUCHAR)Fsrs;
    USHORT StartOffset;

    //
    //  Skip the jump instruction
    //

    StartOffset = FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, FsName);
    
    for (i = StartOffset; i < Fsrs->Length; i++) {

        //
        //  Skip the checksum field itself, which is a USHORT.
        //

        if ((i == FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, Checksum)) ||
            (i == FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, Checksum)+1)) {

            continue;
        }

        Checksum = ((Checksum & 1) ? 0x8000 : 0) + (Checksum >> 1) + Buffer[i];
    }

    return Checksum;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Reconnaissance du système de fichiers](file-system-recognition.md)
</dt> <dt>

[**\_structure de \_ reconnaissance du système de fichiers \_**](file-system-recognition-structure.md)
</dt> </dl>

 

 



