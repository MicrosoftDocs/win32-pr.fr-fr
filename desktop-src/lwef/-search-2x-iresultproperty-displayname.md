---
title: Propriété DisplayName IResultProperty (WdsSharedIDL. h)
description: Nom complet localisé de la propriété.
ms.assetid: 8f9e118a-9e92-4919-afe1-735c61af38f7
keywords:
- Propriété DisplayName fonctionnalités d’environnement Windows héritées
- Propriété DisplayName fonctionnalités d’environnement Windows héritées, interface IResultProperty
- Interface IResultProperty fonctionnalités d’environnement Windows héritées, propriété DisplayName
topic_type:
- apiref
api_name:
- IResultProperty.DisplayName
- IResultProperty.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f36aa934d2ddf31d841478cef1cb9a33b0531224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104554"
---
# <a name="iresultpropertydisplayname-property"></a>IResultProperty ::D propriété isplayName

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

Nom complet localisé de la propriété.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valeur de la propriété

retourne un pointeur vers le nom complet localisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





