---
description: Crée un nouvel objet IContextNode enfant.
ms.assetid: 35d2b641-fada-418b-9374-0303c7d318e5
title: 'IContextNode :: CreateSubNode, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreateSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c7b4bc39431d6b4608586e60bdeffb7cd6c79bf95f944e436c16a683e24e634d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092310"
---
# <a name="icontextnodecreatesubnode-method"></a>IContextNode :: CreateSubNode, méthode

Crée un nouvel objet [**IContextNode**](icontextnode.md) enfant.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateSubNode(
  [in]  const GUID         *pNodeType,
  [out]       IContextNode **ppContextNodeCreated
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNodeType* \[ dans\]
</dt> <dd>

**GUID** qui représente le type de [**IContextNode**](icontextnode.md) à créer.

</dd> <dt>

*ppContextNodeCreated* \[ à\]
</dt> <dd>

Pointeur vers le nouvel [**IContextNode**](icontextnode.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppContextNodeCreated* lorsque vous n’avez plus besoin d’utiliser le nœud de contexte.

 

Le nouveau [**IContextNode**](icontextnode.md) est ajouté à la collection de nœuds enfants de ce nœud de contexte (consultez [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md)). Lorsqu’il existe des nœuds enfants existants, le nouveau **IContextNode** créé est ajouté en tant que dernier nœud enfant.

Pour obtenir la liste des types de nœuds de contexte, consultez [types de nœuds de contexte](context-node-types.md).

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

[**IContextNode ::D eleteSubNode**](icontextnode-deletesubnode.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

