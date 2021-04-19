---
title: Propriété DisplayName IResultType (WdsSharedIDL. h)
description: Nom complet localisé du type
ms.assetid: 21695ba3-aa6d-419b-961a-0643caa5ea1f
keywords:
- Propriété DisplayName fonctionnalités d’environnement Windows héritées
- Propriété DisplayName fonctionnalités d’environnement Windows héritées, interface IResultType
- Interface IResultType fonctionnalités d’environnement Windows héritées, propriété DisplayName
topic_type:
- apiref
api_name:
- IResultType.DisplayName
- IResultType.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94080a2b5c6121bbaa9b611a7d55c2d5aaeed5e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510746"
---
# <a name="iresulttypedisplayname-property"></a>IResultType ::D propriété isplayName

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

Nom complet localisé du type :

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valeur de la propriété

retourne l’adresse du nom complet localisé pour le type.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





