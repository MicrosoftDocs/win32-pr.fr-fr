---
description: la structure de la structure de reconnaissance du système de fichiers \_ \_ \_ , définie en interne par Windows et utilisée par la reconnaissance du système de fichiers (frs), contient une valeur de somme de contrôle qui doit être correctement calculée pour que le service de réplication de fichiers fonctionne correctement avec un système de fichiers non reconnu spécifié.
ms.assetid: 8f76784f-7d03-4874-ae7f-e8bdc42638c3
title: Calcul d’une somme de contrôle de reconnaissance du système de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce146fda589668d39f1f7ff4158384986fb719f2bbbee6ce0584ad9f1e540b08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329179"
---
# <a name="computing-a-file-system-recognition-checksum"></a>Calcul d’une somme de contrôle de reconnaissance du système de fichiers

la structure de la structure de reconnaissance du système de fichiers, définie en interne par Windows et utilisée par la [reconnaissance du système de fichiers](file-system-recognition.md) (frs), contient une valeur de somme de contrôle qui doit être correctement calculée pour que le service de réplication de fichiers fonctionne correctement avec un système de fichiers non reconnu spécifié. [**\_ \_ \_**](file-system-recognition-structure.md) L’exemple suivant effectue ce calcul.


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

 

 



