---
title: IResultsViewer PreviewStyle, propriété (WdsView. h)
description: Contrôle le mode d’affichage du volet de visualisation.
ms.assetid: 750664ea-506a-4219-ade5-1c7f1ffbd0d7
keywords:
- propriété PreviewStyle Windows héritée fonctionnalités d’environnement
- propriété PreviewStyle héritée Windows fonctionnalités d’environnement, interface IResultsViewer
- fonctionnalités d’environnement Windows héritées de l’interface IResultsViewer, propriété PreviewStyle
topic_type:
- apiref
api_name:
- IResultsViewer.PreviewStyle
- IResultsViewer.get_PreviewStyle
- IResultsViewer.put_PreviewStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b412c92ca82263481b83ce739d44f21c2d15d99e9e6e7c74502480e0d8fad1b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753781"
---
# <a name="iresultsviewerpreviewstyle-property"></a>IResultsViewer ::P propriété reviewStyle

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

Contrôle le mode d’affichage du volet de visualisation.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_PreviewStyle(
  [in]          PreviewDisplayStyle style
);

HRESULT get_PreviewStyle(
  [out, retval] PreviewDisplayStyle *style
);
```



## <a name="property-value"></a>Valeur de la propriété

Définit la propriété de style actuelle pour le volet de visualisation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                 |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                        |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| En-tête<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





