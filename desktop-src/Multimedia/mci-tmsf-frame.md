---
title: Macro MCI_TMSF_FRAME (Mciapi. h)
description: La \_ macro MCI TMSF \_ Frame récupère le composant frames à partir d’un paramètre contenant des informations de pistes compressées/minutes/secondes/images (TMSF).
ms.assetid: 1ba78d4f-4537-4955-abcc-842976b6b5b9
keywords:
- MCI_TMSF_FRAME macro multimédia Windows
topic_type:
- apiref
api_name:
- MCI_TMSF_FRAME
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c5a6620137aea397c3f1bc04ff7fe821666d837
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740253"
---
# <a name="mci_tmsf_frame-macro"></a>\_Macro de \_ cadre TMSF MCI

La macro **MCI \_ TMSF \_ Frame** récupère le composant frames à partir d’un paramètre contenant des informations de pistes compressées/minutes/secondes/images (TMSF).

## <a name="syntax"></a>Syntaxe


```C++
BYTE MCI_TMSF_FRAME(
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

Retourne le composant frames des informations de TMSF spécifiées.

## <a name="remarks"></a>Notes

L’heure au format TMSF est exprimée sous la forme d’une valeur **DWORD** avec l’octet le moins significatif contenant les pistes, le prochain octet le moins significatif contenant les minutes, le prochain octet le moins significatif contenant les secondes et l’octet le plus significatif contenant les frames.

La macro **MCI \_ TMSF \_ Frame** est définie comme suit :


```C++
#define MCI_TMSF_FRAME(tmsf) ((BYTE)((tmsf) >> 24)) 
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

 

 





