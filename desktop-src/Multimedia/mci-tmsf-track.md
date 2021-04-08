---
title: Macro MCI_TMSF_TRACK (Mciapi. h)
description: La \_ macro MCI TMSF \_ Track récupère le composant Tracks à partir d’un paramètre contenant des informations de pistes compressées/minutes/secondes/images (TMSF).
ms.assetid: 3455442c-5c66-47c7-b06b-1a2de0e2dfed
keywords:
- MCI_TMSF_TRACK macro multimédia Windows
topic_type:
- apiref
api_name:
- MCI_TMSF_TRACK
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8512169d0e5b3d6892dd1bf615a220143e6d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843697"
---
# <a name="mci_tmsf_track-macro"></a>\_Macro MCI TMSF \_ Track

La macro **MCI \_ TMSF \_ Track** récupère le composant Tracks à partir d’un paramètre contenant des informations de pistes compressées/minutes/secondes/images (TMSF).

## <a name="syntax"></a>Syntaxe


```C++
BYTE MCI_TMSF_TRACK(
   DWORD dwTMSF
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwTMSF* 
</dt> <dd>

Heure au format TMSF.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le composant Tracks des informations de TMSF spécifiées.

## <a name="remarks"></a>Notes

L’heure au format TMSF est exprimée sous la forme d’une valeur **DWORD** avec l’octet le moins significatif contenant les pistes, le prochain octet le moins significatif contenant les minutes, le prochain octet le moins significatif contenant les secondes et l’octet le plus significatif contenant les frames.

La macro **MCI \_ TMSF \_ Track** est définie comme suit :


```C++
#define MCI_TMSF_TRACK(tmsf) ((BYTE)(tmsf)) 
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

 

 





