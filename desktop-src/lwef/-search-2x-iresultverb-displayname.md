---
title: Propriété DisplayName IResultVerb (WdsSharedIDL. h)
description: Cette propriété retourne un pointeur vers le nom complet localisé pour le verbe.
ms.assetid: f1f4a30e-ecfb-4091-b9cd-312e427d0eb4
keywords:
- Propriété DisplayName fonctionnalités d’environnement Windows héritées
- Propriété DisplayName fonctionnalités d’environnement Windows héritées, interface IResultVerb
- Interface IResultVerb fonctionnalités d’environnement Windows héritées, propriété DisplayName
topic_type:
- apiref
api_name:
- IResultVerb.DisplayName
- IResultVerb.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721831274fc87ee65c8ee1655fdb7b38f80e1114
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032713"
---
# <a name="iresultverbdisplayname-property"></a>IResultVerb ::D propriété isplayName

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

Cette propriété retourne un pointeur vers le nom complet localisé pour le verbe.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *Verb
);
```



## <a name="property-value"></a>Valeur de la propriété

Cette propriété retourne un pointeur vers le nom complet localisé pour le verbe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





