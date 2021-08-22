---
title: Propriété de type de données IResultProperty (WdsSharedIDL. h)
description: Type de données des propriétés.
ms.assetid: 2bf83256-0d69-48f2-aa7d-d34dcba17050
keywords:
- propriété DataType héritée Windows fonctionnalités d’environnement
- propriété DataType héritée Windows fonctionnalités d’environnement, interface IResultProperty
- interface IResultProperty Windows héritée fonctionnalités d’environnement, propriété DataType
topic_type:
- apiref
api_name:
- IResultProperty.DataType
- IResultProperty.get_DataType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f669fdbb01459e99edb0ccc9ba75fed1cbd60ebfe789fdb4393d217239cdc1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755258"
---
# <a name="iresultpropertydatatype-property"></a>IResultProperty ::D propriété ataType

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

Type de données des propriétés.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_DataType(
  [out, retval] VARTYPE *vt
);
```



## <a name="property-value"></a>Valeur de la propriété

retourne un pointeur vers le type de données des propriétés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





