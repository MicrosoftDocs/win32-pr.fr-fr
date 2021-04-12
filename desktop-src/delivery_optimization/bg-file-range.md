---
title: Structure BG_FILE_RANGE (Deliveryoptimization. h)
description: La structure BG_FILE_RANGE identifie une plage d’octets à télécharger à partir d’un fichier.
ms.assetid: 58993C51-E42E-4E44-9E8A-15E982B25413
keywords:
- Structure BG_FILE_RANGE
topic_type:
- apiref
api_name:
- BG_FILE_RANGE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cedabfb066a5905adb2ed8eac9996fd77c0e12be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385092"
---
# <a name="bg_file_range-structure"></a>Structure BG_FILE_RANGE

La structure **BG_FILE_RANGE** identifie une plage d’octets à télécharger à partir d’un fichier.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  UINT64 InitialOffset;
  UINT64 Length;
} BG_FILE_RANGE;
```



## <a name="members"></a>Membres

<dl> <dt>

**InitialOffset**
</dt> <dd>

Décalage de base zéro au début de la plage d’octets à télécharger à partir d’un fichier.

</dd> <dt>

**Durée**
</dt> <dd>

Longueur de la plage, en octets. Ne spécifiez pas de longueur égale à zéro octet. Pour indiquer que la plage s’étend jusqu’à la fin du fichier, spécifiez **BG_LENGTH_TO_EOF**.

</dd> </dl>

## <a name="remarks"></a>Notes

La plage doit exister dans le fichier ou générer une erreur **DO_E_INVALID_RANGE** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Server, version 1709, \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBackgroundCopyFile2::GetFileRanges**](ibackgroundcopyfile2-getfileranges-method.md)
</dt> </dl>

 

 





