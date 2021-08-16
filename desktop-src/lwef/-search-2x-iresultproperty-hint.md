---
title: Propriété de l’indicateur IResultProperty (WdsSharedIDL. h)
description: Valeur spéciale utilisée pour faciliter la récupération de données.
ms.assetid: fa888c5e-898e-4f48-b87e-2d0d078fd1fe
keywords:
- propriété Hint héritage Windows fonctionnalités d’environnement
- propriété Hint héritage Windows fonctionnalités d’environnement, interface IResultProperty
- fonctionnalités d’environnement Windows héritées de l’interface IResultProperty, propriété Hint
topic_type:
- apiref
api_name:
- IResultProperty.Hint
- IResultProperty.get_Hint
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48cd5a27a889029d7952452916c43d15ea419772d2cb46f1e86eb2fbf185d2dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754782"
---
# <a name="iresultpropertyhint-property"></a>IResultProperty :: Hint, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

Valeur spéciale utilisée pour faciliter la récupération de données.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Hint(
  [out, retval] ling *hint
);
```



## <a name="property-value"></a>Valeur de la propriété

retourne un pointeur désignant l’indicateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





