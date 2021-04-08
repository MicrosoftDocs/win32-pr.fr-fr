---
title: Macro MCI_MAKE_HMS (Mciapi. h)
description: La \_ macro MCI make \_ HMS crée une valeur d’heure sous forme d’heures/minutes/secondes (HMS) à partir des valeurs d’heures, de minutes et de secondes fournies.
ms.assetid: 470e89eb-36e1-4b05-babd-4c986adc88dd
keywords:
- MCI_MAKE_HMS macro multimédia Windows
topic_type:
- apiref
api_name:
- MCI_MAKE_HMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f37c95df89ed6a799575e964ae274e01e329ef1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743141"
---
# <a name="mci_make_hms-macro"></a>MCI \_ Make \_ HMS macro

La macro **MCI \_ Make \_ HMS** crée une valeur d’heure sous forme d’heures/minutes/secondes (HMS) à partir des valeurs d’heures, de minutes et de secondes fournies.

## <a name="syntax"></a>Syntaxe


```C++
DWORD MCI_MAKE_HMS(
   BYTE hours,
   BYTE minutes,
   BYTE seconds
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hours* 
</dt> <dd>

Nombre d'heures.

</dd> <dt>

*minutes* 
</dt> <dd>

Nombre de minutes.

</dd> <dt>

*secondes* 
</dt> <dd>

Nombre de secondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’heure au format compressé HMS.

## <a name="remarks"></a>Notes

L’heure au format HMS est exprimée sous la forme d’une valeur **DWORD** avec l’octet le moins significatif contenant les heures, le prochain octet le moins significatif contenant les minutes et le prochain octet le moins significatif contenant les secondes. L’octet le plus significatif n’est pas utilisé.

La macro **MCI \_ Make \_ HMS** est définie comme suit :


```C++
#define MCI_MAKE_HMS(h, m, s) ((DWORD)(((BYTE)(h) | \ 
                              ((WORD)(m) << 8)) | \ 
                              (((DWORD)(BYTE)(s)) << 16))) 
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Macros MCI](mci-macros.md)
</dt> </dl>

 

 





