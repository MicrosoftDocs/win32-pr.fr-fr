---
description: Représente un attribut de nom de fichier. Un fichier a un attribut de nom de fichier pour chaque répertoire dans lequel il est entré.
ms.assetid: 54458eee-b786-446c-80bd-213c13bdeb4a
title: Structure FILE_NAME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_NAME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9b09b9c58228c9028a5ac9d26d834bdc21a5c02201338767af84dc713bc3aa60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076143"
---
# <a name="file_name-structure"></a>Structure de nom de fichier \_

\[Cette structure est valide uniquement pour la version 3 des volumes NTFS ; elles peuvent être modifiées dans les versions ultérieures.\]

Représente un attribut de nom de fichier. Un fichier a un attribut de nom de fichier pour chaque répertoire dans lequel il est entré.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _FILE_NAME {
  FILE_REFERENCE ParentDirectory;
  UCHAR          Reserved[0x38];
  UCHAR          FileNameLength;
  UCHAR          Flags;
  WCHAR          FileName[1];
} FILE_NAME, *PFILE_NAME;
```



## <a name="members"></a>Membres

<dl> <dt>

**ParentDirectory**
</dt> <dd>

Référence de fichier au répertoire qui indexe ce nom. Consultez [**\_ \_ référence de segment MFT**](mft-segment-reference.md).

</dd> <dt>

**Reserved**
</dt> <dd>

Réservé.

</dd> <dt>

**FileNameLength**
</dt> <dd>

Longueur du nom de fichier, en caractères Unicode.

</dd> <dt>

**Indicateurs**
</dt> <dd>

Indicateurs de nom de fichier.

<dl> <dt>

<span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**Fichier \_ NOM \_ NTFS** (0x01)
</dt> <dt>

<span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**Fichier \_ NOM \_ dos** (0x02)
</dt> </dl> </dd> <dt>

**FileName**
</dt> <dd>

Premier caractère du nom de fichier.

</dd> </dl>

## <a name="remarks"></a>Remarques

Notez qu’il n’y a aucun fichier d’en-tête associé pour cette structure.

Cette définition de structure est valide uniquement pour la version majeure de la version 3 et la version mineure 0 ou 1, comme indiqué par [**FSCTL \_ obtenir les \_ \_ \_ données du volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Table de fichiers maîtres](master-file-table.md)
</dt> </dl>

 

 
