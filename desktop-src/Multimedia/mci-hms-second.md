---
title: Macro MCI_HMS_SECOND (Mciapi. h)
description: La \_ macro MCI HMS \_ second récupère le composant seconds à partir d’un paramètre contenant des informations sur les heures/minutes/secondes (HMS) compressées.
ms.assetid: b6895bec-524f-4345-ae65-e75168855df2
keywords:
- MCI_HMS_SECOND macro Windows multimédia
topic_type:
- apiref
api_name:
- MCI_HMS_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b869141d6480ba0d986450ce950097ba240009
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416836"
---
# <a name="mci_hms_second-macro"></a>HMS de la \_ \_ deuxième macro MCI

La macro **MCI \_ HMS \_ second** récupère le composant seconds à partir d’un paramètre contenant des informations sur les heures/minutes/secondes (HMS) compressées.

## <a name="syntax"></a>Syntaxe


```C++
BYTE MCI_HMS_SECOND(
   DWORD dwHMS
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwHMS* 
</dt> <dd>

Heure au format HMS.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne le composant « secondes » des informations de HMS spécifiées.

## <a name="remarks"></a>Notes

L’heure au format HMS est exprimée sous la forme d’une valeur **DWORD** avec l’octet le moins significatif contenant les heures, le prochain octet le moins significatif contenant les minutes et le prochain octet le moins significatif contenant les secondes. L’octet le plus significatif n’est pas utilisé.

La macro **MCI \_ HMS \_ second** est définie comme suit :


```C++
#define MCI_HMS_SECOND(hms) ((BYTE)((hms) >> 16)) 
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

 

 





