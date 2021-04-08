---
description: Contient l’attribut d’informations standard. Cet attribut est présent dans chaque enregistrement de fichier de base et doit être résident.
ms.assetid: 8e668309-2722-4115-923d-bf0aa78d24f1
title: Structure STANDARD_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STANDARD_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4927553ac593475f8659932468227362ae19fe59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033573"
---
# <a name="standard_information-structure"></a>\_Structure d’informations standard

\[Cette structure est valide uniquement pour la version 3 des volumes NTFS ; elles peuvent être modifiées dans les versions ultérieures.\]

Contient l’attribut d’informations standard. Cet attribut est présent dans chaque enregistrement de fichier de base et doit être résident.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _STANDARD_INFORMATION {
  UCHAR Reserved[0x30];
  ULONG OwnerId;
  ULONG SecurityId;
} STANDARD_INFORMATION, *PSTANDARD_INFORMATION;
```



## <a name="members"></a>Membres

<dl> <dt>

**Reserved**
</dt> <dd>

Réservé.

</dd> <dt>

**OwnerId**
</dt> <dd>

Identificateur du propriétaire du fichier, à partir de l’index de sécurité.

</dd> <dt>

**SecurityId**
</dt> <dd>

Identificateur de sécurité du fichier.

</dd> </dl>

## <a name="remarks"></a>Notes

Notez qu’il n’y a aucun fichier d’en-tête associé pour cette structure.

Cette définition de structure est valide uniquement pour la version majeure de la version 3 et la version mineure 0 ou 1, comme indiqué par [**FSCTL \_ obtenir les \_ \_ \_ données du volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Table de fichiers maîtres](master-file-table.md)
</dt> </dl>

 

 
