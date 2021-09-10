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
ms.openlocfilehash: 7c5a6620137aea397c3f1bc04ff7fe821666d837
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363972"
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



## <a name="requirements"></a>Spécifications



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

 

 





