---
description: Déplace les données de trait de ce IContextNode vers le IContextNode spécifié.
ms.assetid: 583f2de9-d32e-4177-83d1-4abbd0f9f960
title: 'IContextNode :: ReparentStrokeByIdToNode, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ReparentStrokeByIdToNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a915425900bccb15145546658d51d50dcaee14880f8f219bd1908efaa17bd3c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008409"
---
# <a name="icontextnodereparentstrokebyidtonode-method"></a>IContextNode :: ReparentStrokeByIdToNode, méthode

Déplace les données de trait de ce [**IContextNode**](icontextnode.md) vers le **IContextNode** spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ReparentStrokeByIdToNode(
  [in] LONG         lStrokeId,
  [in] IContextNode *pContextNodeDestination
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lStrokeId* \[ dans\]
</dt> <dd>

Identificateur du trait à déplacer.

</dd> <dt>

*pContextNodeDestination* \[ dans\]
</dt> <dd>

Objet [**IContextNode**](icontextnode.md) vers lequel déplacer les données de trait.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

L’objet [**IContextNode**](icontextnode.md) spécifié doit être l’un des types suivants des constantes de [type de nœud de contexte](context-node-types.md) : **InkWord**, **InkDrawing**, **InkBullet** ou **UnclassifiedInk**. Si vous tentez de déplacer un trait vers tout autre type d’objet **IContextNode** , la valeur de retour **E \_ INVALIDARG** est retournée.

Cette méthode peut être appelée à partir de n’importe quel objet [**IContextNode**](icontextnode.md) , y compris les objets **IContextNode** terminaux non-Ink. Le trait spécifié doit être référencé par l’un des descendants de cet objet **IContextNode** ou **E \_ INVALIDARG** est retourné.

Si ce [**IContextNode**](icontextnode.md) ou **IContextNode** dans *pContextNodeDestination* est confirmé, **E \_ INVALIDARG** est retourné (voir [**IContextNode :: IsConfirmed**](icontextnode-isconfirmed.md)).

L’analyseur d’encre ne supprime pas les nœuds de contexte vides de l’arborescence des résultats en réponse à cette méthode.

-   Un nœud terminal d’encre qui ne fait pas référence à des données de trait est un nœud vide.
-   Un nœud conteneur qui ne fait pas référence à un nœud enfant est un nœud vide.

Un nœud vide génère des erreurs s’il se trouve dans l’arborescence pendant une opération d’analyse de l’encre. Pour supprimer un nœud de l’arborescence de l’analyseur d’encre, appelez la méthode [**IContextNode ::D eletesubnode**](icontextnode-deletesubnode.md) du nœud parent (voir [**IContextNode :: GetParentNode**](icontextnode-getparentnode.md)).

## <a name="requirements"></a>Configuration requise



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

[**IContextNode::SetStrokes**](icontextnode-setstrokes.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




