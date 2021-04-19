---
title: Macro MCI_MAKE_TMSF (Mciapi. h)
description: La \_ macro MCI make \_ TMSF crée une valeur d’heure sous forme de pistes compressées/minutes/secondes/images (TMSF) à partir des valeurs de suivi, de minutes, de secondes et de frames données.
ms.assetid: ff2d6938-0ff7-46d5-92be-42b4b6f35524
keywords:
- MCI_MAKE_TMSF macro multimédia Windows
topic_type:
- apiref
api_name:
- MCI_MAKE_TMSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06cd6a400f742b49dc29063e8473465ad7e32dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536080"
---
# <a name="mci_make_tmsf-macro"></a>MCI \_ Make \_ TMSF macro

La macro **MCI \_ Make \_ TMSF** crée une valeur d’heure sous forme de pistes compressées/minutes/secondes/images (TMSF) à partir des valeurs de suivi, de minutes, de secondes et de frames données.

## <a name="syntax"></a>Syntaxe


```C++
DWORD MCI_MAKE_TMSF(
   BYTE tracks,
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tracks* 
</dt> <dd>

Nombre de pistes.

</dd> <dt>

*minutes* 
</dt> <dd>

Nombre de minutes.

</dd> <dt>

*secondes* 
</dt> <dd>

Nombre de secondes.

</dd> <dt>

*cadres* 
</dt> <dd>

Nombre de frames.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’heure au format compressé TMSF.

## <a name="remarks"></a>Notes

L’heure au format TMSF est exprimée sous la forme d’une valeur **DWORD** avec l’octet le moins significatif contenant les pistes, le prochain octet le moins significatif contenant les minutes, le prochain octet le moins significatif contenant les secondes et l’octet le plus significatif contenant les frames.

La macro **MCI \_ Make \_ TMSF** est définie comme suit :


```C++
#define MCI_MAKE_TMSF(t, m, s, f) ((DWORD)(((BYTE)(t) | \ 
                                  ((WORD)(m) << 8)) | \ 
                                  (((DWORD)(BYTE)(s) | \ 
                                  ((WORD)(f) << 8)) << 16))) 
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

 

 





