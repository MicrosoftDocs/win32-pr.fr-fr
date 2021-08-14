---
title: Propriété DisplayName IResultVerb (WdsSharedIDL. h)
description: Cette propriété retourne un pointeur vers le nom complet localisé pour le verbe.
ms.assetid: f1f4a30e-ecfb-4091-b9cd-312e427d0eb4
keywords:
- propriété DisplayName Windows fonctionnalités d’environnement héritées
- propriété DisplayName Legacy Windows fonctionnalités d’environnement, interface IResultVerb
- fonctionnalités d’environnement Windows héritées de l’interface IResultVerb, propriété DisplayName
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
ms.openlocfilehash: 45d7f72d0d028fa6a6ecdede7f2d88e3e3dea0a37a14cc6365dc5da2d14992af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117694717"
---
# <a name="iresultverbdisplayname-property"></a>IResultVerb ::D propriété isplayName

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

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
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





