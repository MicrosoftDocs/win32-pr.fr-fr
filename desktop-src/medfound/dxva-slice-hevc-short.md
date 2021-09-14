---
description: Spécifie les données de contrôle de la tranche.
ms.assetid: ae3399e9-b78c-473d-8ed5-e570dfb676aa
title: Structure DXVA_Slice_HEVC_Short (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Slice_HEVC_Short
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 0d0f88e1534ef3d901023ebdee8ce9c36a8c2cc9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122165"
---
# <a name="dxva_slice_hevc_short-structure"></a>\_ \_ \_ Structure abrégée HEVC de la tranche DXVA

Spécifie les données de contrôle de la tranche.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DXVA_Slice_HEVC_Short {
  UINT   BSNALunitDataLocation;
  UINT   SliceBytesInBuffer;
  USHORT wBadSliceChopping;
} DXVA_Slice_HEVC_Short, *LPDXVA_Slice_HEVC_Short;
```



## <a name="members"></a>Membres

<dl> <dt>

**BSNALunitDataLocation**
</dt> <dd>

Spécifie l’emplacement de l’unité NAL.

</dd> <dt>

**SliceBytesInBuffer**
</dt> <dd>

Nombre d’octets dans la mémoire tampon de données de flux binaire associés à cette structure de données de contrôle de la tranche.

</dd> <dt>

**wBadSliceChopping**
</dt> <dd>

Si l’analyse de flux binaire hors hôte est utilisée, cette valeur indique le découpage de la tranche incorrecte et contient l’une des valeurs suivantes :



| Condition requise | Valeur |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valeur | Description                                                                                                                                                                                                                                             |
| 0     | Tous les bits de la tranche sont situés dans le tampon de données de flux binaire correspondant.                                                                                                                                                                      |
| 1     | La mémoire tampon de données de flux binaire contient le début de la tranche, mais pas la tranche entière, car la mémoire tampon est pleine.                                                                                                                                        |
| 2     | La mémoire tampon de données de flux binaire contient la fin de la tranche. Elle ne contient pas le début de la tranche, car le début de la tranche a été localisé dans la mémoire tampon de données de flux binaire précédente.                                                                  |
| 3     | La mémoire tampon de données de flux binaire ne contient pas le début de la tranche, car le début de la tranche a été localisé dans la mémoire tampon de données de flux binaire précédente et ne contient pas la fin de la tranche, car la mémoire tampon de données de flux de données actuelle est également pleine. |



 

</dd> </dl>

## <a name="remarks"></a>Notes

**DXVA \_ Slice \_ HEVC \_ short** contient des données de contrôle de tranche qui sont transmises à l’accélérateur matériel à partir du décodeur logiciel hôte.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures de Media Foundation](media-foundation-structures.md)
</dt> </dl>

 

 




