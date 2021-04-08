---
description: Contient les informations de reconnaissance du système de fichiers sur disque stockées dans le secteur de démarrage des volumes (secteur du disque logique zéro).
ms.assetid: d9c19e01-ff82-4bbc-9eb6-aac9dc5c34ac
title: STRUCTURE FILE_SYSTEM_RECOGNITION_STRUCTURE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_SYSTEM_RECOGNITION_STRUCTURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: c542b2b9ee1cd1696c7c95797c7df20aa02180cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034273"
---
# <a name="file_system_recognition_structure-structure"></a>Structure de la structure de reconnaissance du système de fichiers \_ \_ \_

Contient les informations de reconnaissance du système de fichiers sur disque stockées dans le secteur de démarrage du volume (secteur du disque logique zéro).

Il s’agit d’une structure de données définie en interne qui n’est pas disponible dans un en-tête public et est fournie ici pour les développeurs de système de fichiers qui souhaitent tirer parti de la reconnaissance du système de fichiers. Pour plus d’informations, consultez [reconnaissance du système de fichiers](file-system-recognition.md).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _FILE_SYSTEM_RECOGNITION_STRUCTURE {
  UCHAR  Jmp[3];
  UCHAR  FsName[8];
  UCHAR  MustBeZero[5];
  ULONG  Identifier;
  USHORT Length;
  USHORT Checksum;
} FILE_SYSTEM_RECOGNITION_STRUCTURE;
```



## <a name="members"></a>Membres

<dl> <dt>

**JMP**
</dt> <dd>

Instruction JMP. Ce membre de données n’est pas inclus dans la valeur contenue dans le membre de la **somme de contrôle** .

</dd> <dt>

**FsName**
</dt> <dd>

Nom du système de fichiers. Il s’agit d’une séquence de 8 caractères ASCII qui représente le nom explicite non localisable du système de fichiers avec lequel le volume est mis en forme.

Cette chaîne se trouve au même emplacement que le nom du système de fichiers OEM sur un disque avec une structure de bloc de paramètres BIOS normale (BPB).

</dd> <dt>

**MustBeZero**
</dt> <dd>

Espace réservé qui contient des zéros.

Ce membre de données chevauche ce qui est normalement les membres de données suivants dans un BPB :

-   **BytesPerSector**
-   **SectorsPerCluster**
-   **ReservedSectorCount**

Étant donné que ces membres de données ont la valeur zéro, cela doit être suffisant pour obliger les OSs antérieurs à conclure qu’il ne s’agit pas d’un BPB valide et donc de reconnaître le volume.

</dd> <dt>

**Identificateur**
</dt> <dd>

Identificateur de la structure Doit contenir la valeur 0x53525346 organisée dans un ordre d’octet Little endian.

À ce stade de la structure, les données sont alignées sur 16 octets.

</dd> <dt>

**Durée**
</dt> <dd>

Nombre d’octets dans cette structure, du début à la fin, y compris le membre de données **JMP** .

</dd> <dt>

**EEPROM**
</dt> <dd>

Somme de contrôle de deux octets calculée sur les octets à partir du membre de données **FsName** et se terminant au dernier octet de cette structure, à l’exclusion des membres de données **JMP** et **checksum** .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Calcul d’une somme de contrôle de reconnaissance du système de fichiers](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[Reconnaissance du système de fichiers](file-system-recognition.md)
</dt> <dt>

[**\_ \_ informations sur la reconnaissance du système de fichiers \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-file_system_recognition_information)
</dt> <dt>

[**\_reconnaissance du \_ système de fichiers de requête FSCTL \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

