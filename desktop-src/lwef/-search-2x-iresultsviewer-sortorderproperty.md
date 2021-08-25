---
title: IResultsViewer SortOrderProperty, propriété (WdsView.h)
description: Cette propriété définit ou retourne l’ordre des colonnes de tri des résultats.
ms.assetid: ea05f4df-4caf-404f-8890-a109ca88555c
keywords:
- propriété SortOrderProperty Windows héritée fonctionnalités d’environnement
- propriété SortOrderProperty héritée Windows fonctionnalités d’environnement, interface IResultsViewer
- fonctionnalités d’environnement Windows héritées de l’interface IResultsViewer, propriété SortOrderProperty
topic_type:
- apiref
api_name:
- IResultsViewer.SortOrderProperty
- IResultsViewer.get_SortOrderProperty
- IResultsViewer.put_SortOrderProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01680ac46592887cf4f321b771ff0e46039c775c4e9e9d8ed1edbc893ab45977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829169"
---
# <a name="iresultsviewersortorderproperty-property"></a>IResultsViewer :: SortOrderProperty, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

Cette propriété définit ou retourne l’ordre des colonnes de tri des résultats.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_SortOrderProperty(
  [in]          ColumnSortOrder order
);

HRESULT get_SortOrderProperty(
  [out, retval] ColumnSortOrder *order
);
```



## <a name="property-value"></a>Valeur de la propriété

Définit la propriété [**ColumnSortOrder**](/windows/win32/api/mmcobj/ne-mmcobj-_columnsortorder) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                 |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                        |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| En-tête<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





