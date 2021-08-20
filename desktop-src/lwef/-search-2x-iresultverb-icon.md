---
title: IResultVerb Icon, propriété (WdsSharedIDL. h)
description: Cette propriété retourne un pointeur vers un handle de l’icône facultative associée au verbe.
ms.assetid: 19de0e36-b453-48a4-8ac0-f26432e088ae
keywords:
- propriétés d’icône Windows fonctionnalités d’environnement héritées
- propriété Icon héritage Windows fonctionnalités d’environnement, interface IResultVerb
- interface IResultVerb Windows héritée fonctionnalités d’environnement, propriété Icon
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
ms.openlocfilehash: ef3715aacb0fd2f4bb0f47424d239e3d4b9717d83471906de8d1b2637fab472a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117694727"
---
# <a name="iresultverbicon-property"></a>IResultVerb :: Icon, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

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

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





