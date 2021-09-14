---
description: Ajoute un nouveau IContextLink à la collection de liens de contexte de l’objet IContextNode.
ms.assetid: b7b9da10-3015-4976-bc4e-1a7f69b7c85b
title: 'IContextNode :: AddContextLink, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eccfcc8be51ff951c1bcd6de55bd3a0f89cdc201
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127220209"
---
# <a name="icontextnodeaddcontextlink-method"></a>IContextNode :: AddContextLink, méthode

Ajoute un nouveau [**IContextLink**](icontextlink.md) à la collection de liens de contexte de l’objet [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddContextLink(
  [in]  IContextNode         *pDestinationNode,
  [in]  ContextLinkDirection linkDirection,
  [out] IContextLink         **ppContextLinkToAdd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDestinationNode* \[ dans\]
</dt> <dd>

[**IContextNode**](icontextnode.md) de destination pour le nouveau [**IContextLink**](icontextlink.md).

</dd> <dt>

*linkDirection* \[ dans\]
</dt> <dd>

Direction de l’objet [**IContextLink**](icontextlink.md) à créer.

</dd> <dt>

*ppContextLinkToAdd* \[ à\]
</dt> <dd>

Pointeur vers le nouvel objet [**IContextLink**](icontextlink.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppContextLinkToAdd* lorsque vous n’avez plus besoin d’utiliser le nœud de contexte.

 

Cet objet [**IContextNode**](icontextnode.md) est le nœud source (consultez [**IContextLink :: GetSourceNode**](icontextlink-getsourcenode.md)) pour le nouvel objet [**IContextLink**](icontextlink.md) .

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

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[**IContextNode ::D eleteContextLink**](icontextnode-deletecontextlink.md)
</dt> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

