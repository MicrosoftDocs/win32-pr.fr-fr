---
description: Réorganise un objet IContextNode enfant spécifié à l’index spécifié.
ms.assetid: 1cee73af-8d5b-4d5d-bc67-a3ac6f4b2462
title: 'IContextNode :: MoveSubNodeToPosition, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.MoveSubNodeToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 398a56cf2c30c93a72e061dfe968de24276888f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235091"
---
# <a name="icontextnodemovesubnodetoposition-method"></a>IContextNode :: MoveSubNodeToPosition, méthode

Réorganise un objet [**IContextNode**](icontextnode.md) enfant spécifié à l’index spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT MoveSubNodeToPosition(
  [in] IContextNode *pSubnodeToMove,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSubnodeToMove* \[ dans\]
</dt> <dd>

Objet [**IContextNode**](icontextnode.md) à déplacer.

</dd> <dt>

*ulNewIndex* \[ dans\]
</dt> <dd>

Index de la nouvelle position du sous-nœud.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Retourne **E \_ INVALIDARG** si *pSubnodeToMove* n’est pas un nœud enfant de ce [**IContextNode**](icontextnode.md).

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

[**IContextNode::CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




