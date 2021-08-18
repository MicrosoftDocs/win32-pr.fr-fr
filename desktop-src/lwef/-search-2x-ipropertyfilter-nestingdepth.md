---
title: IPropertyFilter NestingDepth, propriété (WdsSharedIDL. h)
description: Filtre la profondeur dans un ensemble imbriqué de parenthèses.
ms.assetid: a52992b3-d232-46a5-907c-8df6bd5ad6fc
keywords:
- propriété NestingDepth Windows héritée fonctionnalités d’environnement
- propriété NestingDepth héritée Windows fonctionnalités d’environnement, interface IPropertyFilter
- fonctionnalités d’environnement Windows héritées de l’interface IPropertyFilter, propriété NestingDepth
topic_type:
- apiref
api_name:
- IPropertyFilter.NestingDepth
- IPropertyFilter.get_NestingDepth
- IPropertyFilter.put_NestingDepth
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2499d7a3d5505f4cb428cbc8831ec0ea4e0a71843693f5a8ba1250995071df32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481207"
---
# <a name="ipropertyfilternestingdepth-property"></a>IPropertyFilter :: NestingDepth, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

Filtre la profondeur dans un ensemble imbriqué de parenthèses.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_NestingDepth(
  [in]          long depth
);

HRESULT get_NestingDepth(
  [out, retval] long *depth
);
```



## <a name="property-value"></a>Valeur de la propriété

Définit le nombre indiquant la profondeur des parenthèses imbriquées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





