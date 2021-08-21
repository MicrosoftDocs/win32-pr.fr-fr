---
title: IResultsViewer HeaderStyle, propriété (WdsView. h)
description: Style de l’en-tête affiché dans la vue.
ms.assetid: 092a2ff2-eb88-4347-a81c-6a8005971ca9
keywords:
- propriété HeaderStyle héritée Windows fonctionnalités d’environnement
- propriété HeaderStyle héritée Windows fonctionnalités d’environnement, interface IResultsViewer
- fonctionnalités d’environnement Windows héritées de l’interface IResultsViewer, propriété HeaderStyle
topic_type:
- apiref
api_name:
- IResultsViewer.HeaderStyle
- IResultsViewer.get_HeaderStyle
- IResultsViewer.put_HeaderStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7c60687c3d306c3f9c3fcbb551f2d746723c7223b1964d42386464729b4069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753890"
---
# <a name="iresultsviewerheaderstyle-property"></a>IResultsViewer :: HeaderStyle, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

Style de l’en-tête affiché dans la vue.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_HeaderStyle(
  [in]          HeaderDisplayStyle style
);

HRESULT get_HeaderStyle(
  [out, retval] HeaderDisplayStyle *style
);
```



## <a name="property-value"></a>Valeur de la propriété

Définit le style de l’en-tête affiché.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                 |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                        |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| En-tête<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





