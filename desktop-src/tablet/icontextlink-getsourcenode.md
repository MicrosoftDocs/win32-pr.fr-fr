---
description: Récupère l’objet IContextNode qui est la source de ce IContextLink.
ms.assetid: 2f55ae9c-9f63-4d49-9bf0-9e169b819e79
title: 'IContextLink :: GetSourceNode, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetSourceNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 609f3012608586f7e6c3279cd0dab4232f58ca3e0e31145124622e87684e06f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940409"
---
# <a name="icontextlinkgetsourcenode-method"></a>IContextLink :: GetSourceNode, méthode

Récupère l’objet [**IContextNode**](icontextnode.md) qui est la source de ce [**IContextLink**](icontextlink.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSourceNode(
  [out] IContextNode **ppSrcContextNodeId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppSrcContextNodeId* \[ à\]
</dt> <dd>

Pointeur vers l’objet [**IContextNode**](icontextnode.md) qui est la source de ce [**IContextLink**](icontextlink.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppSrcContextNodeId* lorsque vous n’avez plus besoin d’utiliser le nœud source.

 

Si l’objet [**IContextLink**](icontextlink.md) est lié entre un nœud qui contient l’écriture et un nœud qui contient Drawing, le nœud source est généralement le nœud qui contient Drawing.

Si l’objet [**IContextLink**](icontextlink.md) a un type de lien (voir [**IContextLink :: GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), le nœud source est le nœud qui englobe le nœud de destination.

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

[**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

