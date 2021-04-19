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
ms.openlocfilehash: ac5676635bec961129078ed8689169d1a81cd87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538855"
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

## <a name="remarks"></a>Notes

Un lien de contexte a un nœud source et un nœud de destination (voir [**IContextLink :: GetSourceNode**](icontextlink-getsourcenode.md) et [**IContextLink :: GetDestinationNode**](icontextlink-getdestinationnode.md)). Cette méthode supprime le [**IContextLink**](icontextlink.md) de la collection de liens de contexte des nœuds source et de destination (voir [**IContextNode :: GetContextLinks**](icontextnode-getcontextlinks.md)).

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

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




