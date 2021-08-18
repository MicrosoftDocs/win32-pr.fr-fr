---
description: Supprime un objet IContextNode de cette collection.
ms.assetid: ddda506d-4e39-486d-ac7d-211dc7869a73
title: 'IContextNodes :: RemoveContextNode, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.RemoveContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8fa1fd222e671dfd87f15862108ea66df3b99e530d453cf4614b7572d31b275c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092300"
---
# <a name="icontextnodesremovecontextnode-method"></a>IContextNodes :: RemoveContextNode, méthode

Supprime un objet [**IContextNode**](icontextnode.md) de cette collection.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RemoveContextNode(
  [in] IContextNode *pContextNode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pContextNode* \[ dans\]
</dt> <dd>

Objet [**IContextNode**](icontextnode.md) à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




