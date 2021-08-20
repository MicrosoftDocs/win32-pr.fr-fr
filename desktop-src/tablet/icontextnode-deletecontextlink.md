---
description: Supprime un objet IContextLink de la collection de liens de l’objet IContextNode.
ms.assetid: c4a69a74-30d6-4099-a02a-13c8a2e52bc7
title: IContextNode ::D méthode eleteContextLink (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 39a36ed8a74accdc7da3eed4c98a96d9ee6abbaa4f52b5c71c367250321d28b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118044840"
---
# <a name="icontextnodedeletecontextlink-method"></a>IContextNode ::D méthode eleteContextLink

Supprime un objet [**IContextLink**](icontextlink.md) de la collection de liens de l’objet [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeleteContextLink(
  [in] IContextLink *pContextLinkToDelete
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pContextLinkToDelete* \[ dans\]
</dt> <dd>

Objet [**IContextLink**](icontextlink.md) à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Un lien de contexte a un nœud source et un nœud de destination (voir [**IContextLink :: GetSourceNode**](icontextlink-getsourcenode.md) et [**IContextLink :: GetDestinationNode**](icontextlink-getdestinationnode.md)). Cette méthode supprime le [**IContextLink**](icontextlink.md) de la collection de liens de contexte des nœuds source et de destination (voir [**IContextNode :: GetContextLinks**](icontextnode-getcontextlinks.md)).

## <a name="requirements"></a>Conditions requises



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

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




