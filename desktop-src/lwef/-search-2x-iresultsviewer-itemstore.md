---
title: IResultsViewer ItemStore, propriété (WdsView. h)
description: Cette propriété définit ou retourne le nom du magasin sur lequel filtrer les résultats.
ms.assetid: c2a60485-c8f7-4951-a75e-2e6f6dcc2e4f
keywords:
- propriété ItemStore Windows héritée fonctionnalités d’environnement
- propriété ItemStore héritée Windows fonctionnalités d’environnement, interface IResultsViewer
- fonctionnalités d’environnement Windows héritées de l’interface IResultsViewer, propriété ItemStore
topic_type:
- apiref
api_name:
- IResultsViewer.ItemStore
- IResultsViewer.get_ItemStore
- IResultsViewer.put_ItemStore
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b21db485f8bfeb52ac413a2886f5624345e9812f2a0086b143f9a10942f7aa74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753900"
---
# <a name="iresultsvieweritemstore-property"></a>IResultsViewer :: ItemStore, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

Cette propriété définit ou retourne le nom du magasin sur lequel filtrer les résultats.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_ItemStore(
  [in]          BSTR name
);

HRESULT get_ItemStore(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valeur de la propriété

Définit les noms du magasin.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                 |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                        |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| En-tête<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





