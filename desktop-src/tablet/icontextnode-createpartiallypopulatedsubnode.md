---
description: Crée un objet IContextNode enfant qui contient uniquement des informations sur le type, l’identificateur et l’emplacement.
ms.assetid: 181028fb-f67c-4c90-bb09-94b68a887bd1
title: 'IContextNode :: CreatePartiallyPopulatedSubNode, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreatePartiallyPopulatedSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7947ba4665bdb101e955246fcc99352a24a4397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862722"
---
# <a name="icontextnodecreatepartiallypopulatedsubnode-method"></a>IContextNode :: CreatePartiallyPopulatedSubNode, méthode

Crée un objet [**IContextNode**](icontextnode.md) enfant qui contient uniquement des informations sur le type, l’identificateur et l’emplacement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreatePartiallyPopulatedSubNode(
  [in]  const GUID            *pNodeType,
  [in]  const GUID            *pNodeId,
  [in]        IAnalysisRegion *pNodeLocation,
  [out]       IContextNode    **pPartiallyPopulatedContextNodeCreated
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNodeType* \[ dans\]
</dt> <dd>

Type de nœud de contexte à créer.

</dd> <dt>

*pNodeId* \[ dans\]
</dt> <dd>

Identificateur du nouveau nœud.

</dd> <dt>

*pNodeLocation* \[ dans\]
</dt> <dd>

Emplacement du nouveau nœud.

</dd> <dt>

*pPartiallyPopulatedContextNodeCreated* \[ à\]
</dt> <dd>

Pointeur vers le nouveau [**IContextNode**](icontextnode.md)partiellement rempli.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *pPartiallyPopulatedContextNodeCreated* lorsque vous n’avez plus besoin d’utiliser le nœud de contexte.

 

Le nouveau [**IContextNode**](icontextnode.md) est ajouté à la collection de nœuds enfants de ce nœud de contexte (consultez [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md)). Lorsqu’il existe des nœuds enfants existants, le nouveau **IContextNode** créé est ajouté en tant que dernier nœud enfant.

Pour plus d’informations sur le type, l’identificateur et l’emplacement, consultez [**IContextNode :: GetType**](icontextnode-gettype.md), [**IContextNode :: GetId**](icontextnode-getid.md)et [**IContextNode :: GetLocation**](icontextnode-getlocation.md).

Cette méthode est utilisée pour le proxy de données comme moyen de créer un objet [**IContextNode**](icontextnode.md) dans l’arborescence de nœuds de contexte avant que toutes les informations le concernant soient disponibles. Pour plus d’informations, consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Types de nœuds de contexte](context-node-types.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

