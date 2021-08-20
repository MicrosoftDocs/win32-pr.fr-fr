---
description: Crée un nouveau nœud de reconnaissance personnalisé pour IInkAnalyzer.
ms.assetid: bc1dbe88-8f81-48b6-9dd3-8f00e2b6c01c
title: 'IInkAnalyzer :: CreateCustomRecognizer, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d30a829107710e1349917ced0a9068108bccd4c120faf3aa96ceed375c350449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118043952"
---
# <a name="iinkanalyzercreatecustomrecognizer-method"></a>IInkAnalyzer :: CreateCustomRecognizer, méthode

Crée un nouveau nœud de reconnaissance personnalisé pour [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateCustomRecognizer(
  [in]  const GUID         *pInkAnalysisRecognizerId,
  [out]       IContextNode **ppContextNode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pInkAnalysisRecognizerId* \[ dans\]
</dt> <dd>

Identificateur global unique (GUID) du [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) pour lequel créer un nœud.

</dd> <dt>

*ppContextNode* \[ à\]
</dt> <dd>

Pointeur vers l’objet [**IContextNode**](icontextnode.md) qui représente le nouveau nœud de reconnaissance personnalisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur ppContextNode lorsque vous n’avez plus besoin d’utiliser l’objet.

 

Cette méthode crée un nouveau [**IContextNode**](icontextnode.md) avec un type de CustomRecognizer (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)). Il ajoute ensuite le nouveau nœud de reconnaissance personnalisé à la collection de sous-nœuds du nœud racine de l’objet [**IInkAnalyzer**](iinkanalyzer.md) (consultez la méthode [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md) et [**IInkAnalyzer :: GetRootNode**](iinkanalyzer-getrootnode.md)).

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**IInkAnalyzer :: GetInkAnalysisRecognizersByPriority, méthode**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

