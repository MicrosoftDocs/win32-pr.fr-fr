---
title: IPropertyFilter LogicOperator, propriété (WdsSharedIDL. h)
description: Opérateur logique à utiliser lors de l’application d’un filtre.
ms.assetid: 9461c7a3-1c70-41bf-a4fe-8dacd4d2ba49
keywords:
- propriété LogicOperator Windows héritée fonctionnalités d’environnement
- propriété LogicOperator héritée Windows fonctionnalités d’environnement, interface IPropertyFilter
- fonctionnalités d’environnement Windows héritées de l’interface IPropertyFilter, propriété LogicOperator
topic_type:
- apiref
api_name:
- IPropertyFilter.LogicOperator
- IPropertyFilter.get_LogicOperator
- IPropertyFilter.put_LogicOperator
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fb4638edbb839581ad20ab6c860afc918b0ddd08e5fe6a36fc92f0dd4cea4a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963829"
---
# <a name="ipropertyfilterlogicoperator-property"></a>IPropertyFilter :: LogicOperator, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

Opérateur logique à utiliser lors de l’application d’un filtre.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_LogicOperator(
  [in]          FilterLogicOperator op
);

HRESULT get_LogicOperator(
  [out, retval] FilterLogicOperator *op
);
```



## <a name="property-value"></a>Valeur de la propriété

Définit le type d’opérateur logique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





