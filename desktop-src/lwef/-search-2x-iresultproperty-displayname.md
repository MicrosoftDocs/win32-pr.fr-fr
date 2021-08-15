---
title: Propriété DisplayName IResultProperty (WdsSharedIDL. h)
description: Nom complet localisé de la propriété.
ms.assetid: 8f9e118a-9e92-4919-afe1-735c61af38f7
keywords:
- propriété DisplayName Windows fonctionnalités d’environnement héritées
- propriété DisplayName Legacy Windows fonctionnalités d’environnement, interface IResultProperty
- fonctionnalités d’environnement Windows héritées de l’interface IResultProperty, propriété DisplayName
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
ms.openlocfilehash: c0e15eedcafffbae25b2671b02aaac8fd1e64b625edfea3e040ed2c6067ca953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755161"
---
# <a name="iresultpropertydisplayname-property"></a>IResultProperty ::D propriété isplayName

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

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
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





