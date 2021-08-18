---
description: Recherche la plage de texte dans la chaîne reconnue qui correspond à une collection d’objets IContextNode.
ms.assetid: 2c5bc4a1-08de-4872-b552-6d22924ce2a8
title: 'IInkAnalyzer :: GetTextRangeFromNodes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetTextRangeFromNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 147877ef8871f7b07e2aa501a107c1e40bd75e80009e5bee97dca03346bb853a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092129"
---
# <a name="iinkanalyzergettextrangefromnodes-method"></a>IInkAnalyzer :: GetTextRangeFromNodes, méthode

Recherche la plage de texte dans la chaîne reconnue qui correspond à une collection d’objets [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTextRangeFromNodes(
  [out] LONG          *plStart,
  [out] LONG          *plLength,
  [in]  IContextNodes *pNodesToSearch
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*plStart* \[ à\]
</dt> <dd>

Entier signé 32 bits qui indique le début de la plage de texte. Ce paramètre est passé sans être initialisé.

</dd> <dt>

*plLength* \[ à\]
</dt> <dd>

Entier signé 32 bits qui indique la longueur de la plage de texte. Ce paramètre est passé sans être initialisé.

</dd> <dt>

*pNodesToSearch* \[ dans\]
</dt> <dd>

Collection d’objets [**IContextNode**](icontextnode.md) pour lesquels rechercher la plage de texte.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Si *pNodesToSearch* contient des objets [**IContextNode**](icontextnode.md) qui ne sont pas adjacents, cette méthode retourne la plus petite plage de texte qui couvre tous les objets **IContextNode** .

Cette méthode lève une exception E \_ INVALIDARG quand *pNodesToSearch* contient un [**IContextNode**](icontextnode.md) qui n’est pas associé au [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> </dl>

 

 




