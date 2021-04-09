---
title: Macro MCI_HMS_HOUR (Mciapi. h)
description: La \_ macro MCI HMS \_ Hour récupère le composant heures à partir d’un paramètre contenant des informations sur les heures/minutes/secondes (HMS) compressées.
ms.assetid: 55968b2b-2bfe-48ac-a50f-5c8741d11e33
keywords:
- MCI_HMS_HOUR macro multimédia Windows
topic_type:
- apiref
api_name:
- MCI_HMS_HOUR
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ecab8b5de7712a9c1a5ebd5c0a4401b264d7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033239"
---
# <a name="mci_hms_hour-macro"></a>HMS de la \_ \_ macro d’heure MCI

La macro **MCI \_ HMS \_ Hour** récupère le composant heures à partir d’un paramètre contenant des informations sur les heures/minutes/secondes (HMS) compressées.

## <a name="syntax"></a>Syntaxe


```C++
BYTE MCI_HMS_HOUR(
   DWORD dwHMS
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwHMS* 
</dt> <dd>

Heure au format HMS.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le composant « heures » des informations de HMS spécifiées.

## <a name="remarks"></a>Notes

L’heure au format HMS est exprimée sous la forme d’une valeur **DWORD** avec l’octet le moins significatif contenant les heures, le prochain octet le moins significatif contenant les minutes et le prochain octet le moins significatif contenant les secondes. L’octet le plus significatif n’est pas utilisé.

La macro **MCI \_ HMS \_ Hour** est définie comme suit :


```C++
#define MCI_HMS_HOUR(hms) ((BYTE)(hms)) 
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

 

 





