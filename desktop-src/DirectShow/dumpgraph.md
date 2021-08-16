---
description: La fonction DumpGraph envoie les informations relatives à un graphique de filtre à l’emplacement de sortie de débogage. Ignoré dans les builds de vente au détail.
ms.assetid: c78f86bb-44d0-4904-b7f8-e756bda0151d
title: DumpGraph, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DumpGraph
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ac09cc3381ab1b5f85f523d1c822768b3e2f87b6bcf08f1877680349072c216
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820958"
---
# <a name="dumpgraph-function"></a>DumpGraph fonction)

La `DumpGraph` fonction envoie des informations sur un graphique de filtre à l’emplacement de sortie de débogage. Ignoré dans les builds de vente au détail.

## <a name="syntax"></a>Syntaxe


```C++
void DumpGraph(
   IFilterGraph *pGraph,
   DWORD        dwLevel
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pGraph* 
</dt> <dd>

Pointeur vers l’interface [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) sur le gestionnaire de graphique de filtre.

</dd> <dt>

*dwLevel* 
</dt> <dd>

Niveau de journalisation. La fonction génère un \_ message de trace du journal avec le niveau de journalisation spécifié.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de sortie de débogage](debug-output-functions.md)
</dt> </dl>

 

 




