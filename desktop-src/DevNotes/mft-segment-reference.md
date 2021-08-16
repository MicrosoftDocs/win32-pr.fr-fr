---
description: Représente une adresse dans la table de fichiers maîtres (MFT). L’adresse est marquée avec un numéro de séquence réutilisé circulairement qui est défini au moment où la référence de segment MFT était valide.
ms.assetid: 59d83b95-83fb-4630-8ce4-f58441c748ab
title: Structure MFT_SEGMENT_REFERENCE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFT_SEGMENT_REFERENCE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0ef3ad4e727465b5ceb24c1ecc785f62b747da8113b8853bffc3431604089066
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827085"
---
# <a name="mft_segment_reference-structure"></a>Structure de référence du \_ segment MFT \_

\[Cette structure est valide uniquement pour la version 3 des volumes NTFS ; elles peuvent être modifiées dans les versions ultérieures.\]

Représente une adresse dans la table de fichiers maîtres (MFT). L’adresse est marquée avec un numéro de séquence réutilisé circulairement qui est défini au moment où la référence de segment MFT était valide.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _MFT_SEGMENT_REFERENCE {
  ULONG  SegmentNumberLowPart;
  USHORT SegmentNumberHighPart;
  USHORT SequenceNumber;
} MFT_SEGMENT_REFERENCE, *PMFT_SEGMENT_REFERENCE;
```



## <a name="members"></a>Membres

<dl> <dt>

**SegmentNumberLowPart**
</dt> <dd>

Partie inférieure du numéro de segment.

</dd> <dt>

**SegmentNumberHighPart**
</dt> <dd>

Partie haute du numéro de segment.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Numéro de séquence différent de zéro. La valeur 0 est réservée.

</dd> </dl>

## <a name="remarks"></a>Remarques

Notez qu’il n’y a aucun fichier d’en-tête associé pour cette structure.

Cette définition de structure est valide uniquement pour la version majeure de la version 3 et la version mineure 0 ou 1, comme indiqué par [**FSCTL \_ obtenir les \_ \_ \_ données du volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

Le type de données de **\_ référence de fichier** est défini comme suit.

``` syntax
typedef MFT_SEGMENT_REFERENCE FILE_REFERENCE, *PFILE_REFERENCE;
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Table de fichiers maîtres](master-file-table.md)
</dt> </dl>

 

 
