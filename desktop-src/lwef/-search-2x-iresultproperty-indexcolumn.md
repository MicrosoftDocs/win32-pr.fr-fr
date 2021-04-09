---
title: IResultProperty IndexColumn, propriété (WdsSharedIDL. h)
description: Nom de la colonne des propriétés dans l’index.
ms.assetid: a043be43-49ef-46e0-bfb6-01104288e9ef
keywords:
- Propriétés IndexColumn héritées fonctionnalités de l’environnement Windows
- Propriété IndexColumn fonctionnalités de l’environnement Windows héritées, interface IResultProperty
- Interface IResultProperty fonctionnalités d’environnement Windows héritées, propriété IndexColumn
topic_type:
- apiref
api_name:
- IResultProperty.IndexColumn
- IResultProperty.get_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a4749f9ba1200f1af8ba202056e48f0123e8402
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843377"
---
# <a name="iresultpropertyindexcolumn-property"></a>IResultProperty :: IndexColumn, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

Nom de la colonne des propriétés dans l’index.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a>Valeur de la propriété

retourne un pointeur vers le nom de colonne dans l’index.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





