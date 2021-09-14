---
description: Modifie le type de confirmation, qui contrôle ce que l’objet IInkAnalyzer peut modifier à propos du IContextNode.
ms.assetid: a506f27e-3909-453e-a2f3-10d4c04d78a4
title: 'IContextNode :: Confirm, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Confirm
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3703bb735c0707c412b7c1e41c43819904d83ce8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127220204"
---
# <a name="icontextnodeconfirm-method"></a>IContextNode :: Confirm, méthode

Modifie le type de confirmation, qui contrôle ce que l’objet [**IInkAnalyzer**](iinkanalyzer.md) peut modifier à propos du [**IContextNode**](icontextnode.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Confirm(
  [in] ConfirmationType confirmedType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*confirmedType* \[ dans\]
</dt> <dd>

[**ConfirmationType**](confirmationtype.md) appliqué au nœud.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Utilisez cette méthode pour permettre à l’utilisateur final de confirmer que le [**IInkAnalyzer**](iinkanalyzer.md) a correctement analysé les traits. Après l’appel de **IContextNode :: Confirm** , le **IInkAnalyzer** ne modifie pas les objets [**IContextNode**](icontextnode.md) pour ces traits lors de l’analyse ultérieure.

Utilisez **IContextNode :: Confirm** lorsque l’utilisateur a confirmé les résultats de l’analyse et ne veut pas que le [**IInkAnalyzer**](iinkanalyzer.md) change un [**IContextNode**](icontextnode.md) lors de l’analyse ultérieure. Par exemple, si l’utilisateur écrit le mot « vers », puis que l’application appelle la [**méthode IInkAnalyzer :: Analyze**](iinkanalyzer-analyze.md), l’analyseur d’encre génère un nœud InkWord avec la valeur « to ». Si l’utilisateur ajoute ensuite « me » après « to » comme un seul mot et que l’application appelle de nouveau la **méthode IInkAnalyzer :: Analyze** , l’analyseur d’encre peut supprimer le nœud InkWord précédent et créer un nouveau nœud InkWord avec la valeur « tome ». Toutefois, si, après le premier appel à la **méthode IInkAnalyzer :: Analyze**, l’application appelle **IContextNode :: Confirm** sur le nœud InkWord pour « to » avec la valeur [**ConfirmationType**](confirmationtype.md) **NodeTypeAndProperties**, avant que l’utilisateur n’ajoute le « me », quand l’application appelle la **méthode IInkAnalyzer :: Analyze**, l’analyseur d’encre ne supprime pas ou ne modifie pas le nœud « to ». À la place, l’analyseur d’encre peut reconnaître deux nœuds InkWord pour « to » et « me ».

[**IContextNode**](icontextnode.md) peut uniquement confirmer les objets de type InkWord et InkDrawing (consultez [types de nœuds de contexte](context-node-types.md)). **IContextNode :: Confirm** retourne **E \_ INVALIDARG** lorsque le nœud n’est pas un nœud terminal.

Les méthodes [**IInkAnalyzer :: RemoveStroke**](iinkanalyzer-removestroke.md) et [**IInkAnalyzer :: RemoveStrokes**](iinkanalyzer-removestrokes.md) déconfirment les nœuds à partir desquels ils suppriment les données de trait.

[**IContextNode :: SetStrokes**](icontextnode-setstrokes.md), [**IInkAnalyzer :: SetStrokesType**](iinkanalyzer-setstrokestype.md)et [**IInkAnalyzer :: SetStrokeType**](iinkanalyzer-setstroketype.md) retournent le biais du **Core \_ E \_ INVALIDOPERATION** si l’objet [**IContextNode**](icontextnode.md) est déjà confirmé.

[**IContextNode :: ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md) retourne une erreur si le nœud source ou de destination est confirmé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




