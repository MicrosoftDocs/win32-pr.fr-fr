---
description: Représente une relation entre deux objets IContextNode.
ms.assetid: ee81d9d7-eba9-4b11-84d0-5a6ca0df7d92
title: Interface IContextLink (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df1e0d8717ba29532486277aced19f17adb1d79c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524069"
---
# <a name="icontextlink-interface"></a>Interface IContextLink

Représente une relation entre deux objets [**IContextNode**](icontextnode.md) .

## <a name="members"></a>Membres

L’interface **IContextLink** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IContextLink** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IContextLink** possède ces méthodes.



| Méthode                                                                  | Description                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md) | Récupère le type de relation représenté par ce **IContextLink** .<br/>                                         |
| [**GetDestinationNode**](icontextlink-getdestinationnode.md)           | Récupère l’objet [**IContextNode**](icontextnode.md) qui est la destination de ce **IContextLink**.<br/> |
| [**GetSourceNode**](icontextlink-getsourcenode.md)                     | Récupère l’objet [**IContextNode**](icontextnode.md) qui est la source de ce **IContextLink**.<br/>      |



 

## <a name="remarks"></a>Remarques

Voici un exemple de relation représentée par un objet **IContextLink** :

-   Lorsqu’un nœud AnalysisHint est utilisé dans l’analyse de l’encre, l’opération d’analyse de l’encre crée un objet **IContextLink** de type AnalysisHint entre le nœud de l’indicateur d’analyse et le nœud qui contient l’écriture dans la zone de l’indicateur. Le nœud source est le nœud d’indicateur d’analyse et le nœud de destination est le nœud qui contient l’écriture.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Types de nœuds de contexte](context-node-types.md)
</dt> </dl>

 

