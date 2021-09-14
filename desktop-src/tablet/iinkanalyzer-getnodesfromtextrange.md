---
description: Récupère une collection d’objets IContextNode qui sont pertinents pour la plage de texte spécifiée pour les nœuds de contexte spécifiés.
ms.assetid: 39a5dd52-7007-4395-8668-261eca78a090
title: 'IInkAnalyzer :: GetNodesFromTextRange, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetNodesFromTextRange
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ada60a64bb4e7d8b4604b18982630dabd7e44256
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293315"
---
# <a name="iinkanalyzergetnodesfromtextrange-method"></a>IInkAnalyzer :: GetNodesFromTextRange, méthode

Récupère une collection d’objets [**IContextNode**](icontextnode.md) qui sont pertinents pour la plage de texte spécifiée pour les nœuds de contexte spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNodesFromTextRange(
  [in, out] LONG          *plStart,
  [in, out] LONG          *plLength,
  [out]     IContextNodes **ppContextNodes,
  [in]      IContextNodes *pNodesToSearch = defaultvalue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*plStart* \[ in, out\]
</dt> <dd>

Référence au début de la plage de texte dans la partie *pNodesToSearch* de la chaîne reconnue.

</dd> <dt>

*plLength* \[ in, out\]
</dt> <dd>

Référence à la longueur de la plage de texte dans la partie *pNodesToSearch* de la chaîne reconnue.

</dd> <dt>

*ppContextNodes* \[ à\]
</dt> <dd>

Pointeur vers les objets [**IContextNode**](icontextnode.md) qui sont pertinents pour la plage de texte spécifiée pour les nœuds de contexte spécifiés.

</dd> <dt>

*pNodesToSearch* \[ dans\]
</dt> <dd>

Objets [**IContextNode**](icontextnode.md) auxquels limiter la recherche.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

La plage de texte spécifiée doit être relative à la partie *pNodesToSearch* de la chaîne reconnue du [**IInkAnalyzer**](iinkanalyzer.md), plutôt qu’à la chaîne reconnue du **IInkAnalyzer** entier.

Cette méthode modifie les valeurs des paramètres *plStart* et *plLength* en développant la plage de texte aux limites de mot les plus proches.

Par exemple, si la chaîne reconnue est « je suis tardif » et que vous appelez cette méthode à l’aide des valeurs de paramètre de 6 pour *plStart* et 1 pour *plLength*, qui correspond à la lettre « a » dans « Late », cette méthode retourne une collection contenant un [**IContextNode**](icontextnode.md)unique, InkWord ou TextWord qui correspond au mot « Late ». Pour cet exemple, cette méthode modifie également la valeur de *plStart* à 5 et la valeur de *plLength* à 4, ce qui correspond au mot « Late ».

> [!Note]  
> Le paramètre *plStart* est relatif à la chaîne reconnue du paramètre *pNodesToSearch* .

 

## <a name="requirements"></a>Spécifications



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

 

 




