---
title: IResultsViewer SortProperty, propriété (WdsView. h)
description: Cette propriété définit ou retourne le IndexColumn de la propriété selon laquelle trier les résultats.
ms.assetid: 5b117f2e-52cc-43ef-9ebd-d7a800015465
keywords:
- Propriétés SortProperty héritées fonctionnalités de l’environnement Windows
- Propriété SortProperty fonctionnalités de l’environnement Windows héritées, interface IResultsViewer
- Interface IResultsViewer fonctionnalités d’environnement Windows héritées, propriété SortProperty
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
ms.openlocfilehash: 2cb75b98f1f0a726ef0d61b5c476df1485ba7189
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843505"
---
# <a name="iresultsviewersortproperty-property"></a>IResultsViewer :: SortProperty, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

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
| Serveur minimal pris en charge<br/> | Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                        |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| En-tête<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





