---
title: Macro MCI_TMSF_FRAME (Mciapi. h)
description: La \_ macro MCI TMSF \_ Frame récupère le composant frames à partir d’un paramètre contenant des informations de pistes compressées/minutes/secondes/images (TMSF).
ms.assetid: 1ba78d4f-4537-4955-abcc-842976b6b5b9
keywords:
- MCI_TMSF_FRAME macro Windows multimédia
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
ms.openlocfilehash: 90872f0a9391d30d7ec3af17e85203cebe433a4c24bde35e3a27db9b40ca30aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784229"
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

## <a name="remarks"></a>Remarques

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

 

 





