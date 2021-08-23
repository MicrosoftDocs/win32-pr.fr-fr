---
description: Récupère l’objet IContextNode qui est la destination de ce IContextLink.
ms.assetid: 7e185e69-821b-409b-bc58-d89a4aefeb23
title: 'IContextLink :: GetDestinationNode, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetDestinationNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1a11d9021d4299a1823fee57ed9a80237b4896459b0396a8ba4b140bd377bb80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967452"
---
# <a name="icontextlinkgetdestinationnode-method"></a>IContextLink :: GetDestinationNode, méthode

Récupère l’objet [**IContextNode**](icontextnode.md) qui est la destination de ce [**IContextLink**](icontextlink.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDestinationNode(
  [out] IContextNode **ppDstContextNodeId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppDstContextNodeId* \[ à\]
</dt> <dd>

Pointeur vers l’objet [**IContextNode**](icontextnode.md) qui est la destination de ce [**IContextLink**](icontextlink.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppDstContextNodeId* lorsque vous n’avez plus besoin d’utiliser le nœud de destination.

 

Si l’objet [**IContextLink**](icontextlink.md) est lié entre un nœud qui contient l’écriture et un nœud qui contient Drawing, le nœud de destination est généralement le nœud qui contient l’écriture.

Si l’objet [**IContextLink**](icontextlink.md) a un type de lien (voir [**IContextLink :: GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), le nœud de destination est l’objet [**IContextNode**](icontextnode.md) qui est entouré.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

