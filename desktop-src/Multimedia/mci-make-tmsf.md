---
title: Macro MCI_MAKE_TMSF (Mciapi. h)
description: La \_ macro MCI make \_ TMSF crée une valeur d’heure sous forme de pistes compressées/minutes/secondes/images (TMSF) à partir des valeurs de suivi, de minutes, de secondes et de frames données.
ms.assetid: ff2d6938-0ff7-46d5-92be-42b4b6f35524
keywords:
- MCI_MAKE_TMSF macro Windows multimédia
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
ms.openlocfilehash: ec038e0eb1e46c46162c9a2139f03881689db5fe1ee5993a8e135e5d92d67984
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138402"
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

## <a name="remarks"></a>Remarques

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

 

 





