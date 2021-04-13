---
title: IResultVerb Icon, propriété (WdsSharedIDL. h)
description: Cette propriété retourne un pointeur vers un handle de l’icône facultative associée au verbe.
ms.assetid: 19de0e36-b453-48a4-8ac0-f26432e088ae
keywords:
- Propriété Icon fonctionnalités de l’environnement Windows hérité
- Propriété Icon fonctionnalités de l’environnement Windows héritées, interface IResultVerb
- Interface IResultVerb fonctionnalités de l’environnement Windows héritées, propriété Icon
topic_type:
- apiref
api_name:
- IResultVerb.Icon
- IResultVerb.get_Icon
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2babd2a9e45f1d038d5f7ce567eeaaf37e1f29f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465942"
---
# <a name="iresultverbicon-property"></a>IResultVerb :: Icon, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

Cette propriété retourne un pointeur vers un handle de l’icône facultative associée au verbe.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Icon(
  [out, retval] SHANDLE_PTR *hicon
);
```



## <a name="property-value"></a>Valeur de la propriété

HICON est un pointeur vers le handle de l’icône facultative assocuated avec le verbe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





