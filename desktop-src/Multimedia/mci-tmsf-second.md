---
title: Macro MCI_TMSF_SECOND (Mciapi. h)
description: La \_ macro MCI TMSF \_ second récupère le composant seconds à partir d’un paramètre contenant les informations de pistes compressées/minutes/secondes/images (TMSF).
ms.assetid: 0f431545-bde0-4898-9a9d-993847aedf50
keywords:
- MCI_TMSF_SECOND macro Windows multimédia
topic_type:
- apiref
api_name:
- MCI_TMSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92dc8f7771df35e9ddc712d263e805ba1e844ca42cde607d7204dc6dc7b350d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784198"
---
# <a name="mci_tmsf_second-macro"></a>TMSF de la \_ \_ deuxième macro MCI

La macro **MCI \_ TMSF \_ second** récupère le composant seconds à partir d’un paramètre contenant les informations de pistes compressées/minutes/secondes/images (TMSF).

## <a name="syntax"></a>Syntaxe


```C++
BYTE MCI_TMSF_SECOND(
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

Retourne le composant « secondes » des informations de TMSF spécifiées.

## <a name="remarks"></a>Remarques

L’heure au format TMSF est exprimée sous la forme d’une valeur **DWORD** avec l’octet le moins significatif contenant les pistes, le prochain octet le moins significatif contenant les minutes, le prochain octet le moins significatif contenant les secondes et l’octet le plus significatif contenant les frames.

La macro **MCI \_ TMSF \_ second** est définie comme suit :


```C++
#define MCI_TMSF_SECOND(tmsf) ((BYTE)((tmsf) >> 16)) 
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

 

 





