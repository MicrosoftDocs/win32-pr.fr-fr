---
description: Supprime un IContextNode enfant.
ms.assetid: ed1d7b35-f6ba-4eff-888d-5cc492f02832
title: IContextNode ::D méthode eleteSubNode (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 0ebad42f02ccfad0db2d119832f3495819ac18ce321d72ede3aa8d7545b999be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057879"
---
# <a name="icontextnodedeletesubnode-method"></a>IContextNode ::D méthode eleteSubNode

Supprime un [**IContextNode**](icontextnode.md)enfant.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeleteSubNode(
  [in] IContextNode *pContextNodeToDelete
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pContextNodeToDelete* \[ dans\]
</dt> <dd>

[**IContextNode**](icontextnode.md) à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

E \_ INVALIDARG est retourné si le paramètre *pContextNodeToDelete* n’est pas un enfant de cet objet [**IContextNode**](icontextnode.md) .

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

[**IContextNode::CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




