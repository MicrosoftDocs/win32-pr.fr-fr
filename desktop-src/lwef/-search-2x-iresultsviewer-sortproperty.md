---
title: IResultsViewer SortProperty, propriété (WdsView. h)
description: Cette propriété définit ou retourne le IndexColumn de la propriété selon laquelle trier les résultats.
ms.assetid: 5b117f2e-52cc-43ef-9ebd-d7a800015465
keywords:
- propriété SortProperty Windows héritée fonctionnalités d’environnement
- propriété SortProperty héritée Windows fonctionnalités d’environnement, interface IResultsViewer
- fonctionnalités d’environnement Windows héritées de l’interface IResultsViewer, propriété SortProperty
topic_type:
- apiref
api_name:
- IResultsViewer.SortProperty
- IResultsViewer.get_SortProperty
- IResultsViewer.put_SortProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99ab912dde6bdc87b2e9d05496f25de497b6fdc9c8fde4e65e3d2cb89549b1e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610929"
---
# <a name="iresultsviewersortproperty-property"></a>IResultsViewer :: SortProperty, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

Cette propriété définit ou retourne le IndexColumn de la propriété selon laquelle trier les résultats.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_SortProperty(
  [in]          BSTR column
);

HRESULT get_SortProperty(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a>Valeur de la propriété

Définit la propriété IndexColumn.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                 |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                        |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| En-tête<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





