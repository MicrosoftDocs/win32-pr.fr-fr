---
description: Récupère une collection d’objets IContextLink qui représentent des relations avec d’autres objets IContextNode.
ms.assetid: 0fe56e6d-c779-4916-9c80-6f18cf6f1b09
title: 'IContextNode :: GetContextLinks, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de62550a09d0a538ddc680f6d57c35a1016fe255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514633"
---
# <a name="icontextnodegetcontextlinks-method"></a>IContextNode :: GetContextLinks, méthode

Récupère une collection d’objets [**IContextLink**](icontextlink.md) qui représentent des relations avec d’autres objets [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetContextLinks(
  [out] IContextLinks **ppContextLinks
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppContextLinks* \[ à\]
</dt> <dd>

Pointeur vers une collection d’objets [**IContextLink**](icontextlink.md) qui représente des relations avec d’autres objets [**IContextNode**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppContextLinks* lorsque vous n’avez plus besoin d’utiliser la collection de liens de contexte.

 

Pour obtenir des informations sur les relations de nœud parent ou enfant, utilisez [**IContextNode :: GetParentNode**](icontextnode-getparentnode.md) ou [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md).

Pour plus d’informations sur les genres de relations qui sont décrits par les liens, consultez [**IContextLink**](icontextlink.md) et [**ContextLinkDirection**](contextlinkdirection.md).

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

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

