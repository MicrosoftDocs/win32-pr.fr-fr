---
description: Spécifie le type de confirmation qui peut se produire sur un objet IContextNode.
ms.assetid: 5c906548-dbf5-4448-b248-070bd43b054e
title: Énumération ConfirmationType (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfirmationType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 2c43971c6ccf44513c11e46d4bc5db86d973d7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514380"
---
# <a name="confirmationtype-enumeration"></a>Énumération ConfirmationType

Spécifie le type de confirmation qui peut se produire sur un objet [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef enum ConfirmationType { 
  ConfirmationType_None                   = 0,
  ConfirmationType_NodeTypeAndProperties  = 1,
  ConfirmationType_TopBoundary            = 4
} ConfirmationType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**ConfirmationType \_ aucun**
</dt> <dd>

Aucune confirmation n’est appliquée. Le [**IInkAnalyzer**](iinkanalyzer.md) est libre de modifier un nœud de contexte ou l’un de ses descendants si nécessaire.

</dd> <dt>

<span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**ConfirmationType \_ NodeTypeAndProperties**
</dt> <dd>

Le [**IInkAnalyzer**](iinkanalyzer.md) ne peut pas modifier le type ou les propriétés du nœud de contexte spécifié.

</dd> <dt>

<span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**ConfirmationType- \_ boundic**
</dt> <dd>

Le [**IInkAnalyzer**](iinkanalyzer.md) n’effectue pas d’opérations, y compris l’ajout d’encre ou la fusion avec d’autres [**ContextNodes**](icontextnodes.md), qui entraînent le déplacement de la limite supérieure au-delà de la limite supérieure actuelle. Par exemple :

-   Une application analyse un jeu d’encre et un ParagraphNode est identifié.
-   L’application confirme la limite de la limite de ce paragraphe.
-   L’utilisateur de l’application écrit une nouvelle encre au-dessus du paragraphe actuel. Lorsque l’analyse est à nouveau appelée, la nouvelle encre n’est pas incorporée dans le nœud de paragraphe confirmé.
-   Étant donné que seule la limite supérieure est confirmée, le ContextNode peut continuer à croître dans d’autres directions. La suppression des traits peut entraîner le déplacement de la limite supérieure. La traduction du ContextNode peut entraîner la modification de l’emplacement, mais n’autorisera pas la fusion de l’encre supplémentaire dans le nouvel emplacement.

Ce ConfirmationType s’applique uniquement aux nœuds de paragraphe.

</dd> </dl>

## <a name="remarks"></a>Notes

Vous pouvez utiliser la valeur **NodeTypeAndProperties** uniquement pour les nœuds Word et Ink Drawing (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)). Dans le cas contraire, un **E \_ INVALIDARG** est retourné à partir de [**IContextNode :: Confirm**](icontextnode-confirm.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextNode :: Confirm**](icontextnode-confirm.md)
</dt> <dt>

[**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)
</dt> </dl>

 

 




