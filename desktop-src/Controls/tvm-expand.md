---
title: Message TVM_EXPAND (commctrl. h)
description: La TVM \_ expand message développe ou réduit la liste des éléments enfants associés à l’élément parent spécifié, le cas échéant. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro Expand TreeView.
ms.assetid: d6c2e5b2-ce36-4c2b-b527-91c6de56e305
keywords:
- TVM_EXPAND les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_EXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025527dc86e832cf24a86cf9c973d1e2e5103fa23e597bc14cb35e00dba276a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104419"
---
# <a name="tvm_expand-message"></a>TVM- \_ développer le message

La **TVM \_ expand** message développe ou réduit la liste des éléments enfants associés à l’élément parent spécifié, le cas échéant. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ expand TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indicateur d’action. Ce paramètre peut être une ou plusieurs des valeurs suivantes :



| Valeur                                                                                                                                                                     | Signification                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVE_COLLAPSE"></span><span id="tve_collapse"></span><dl> <dt>**TVE \_ réduire**</dt> </dl>                | Réduit la liste. <br/>                                                                                                                                                                                                                                                       |
| <span id="TVE_COLLAPSERESET"></span><span id="tve_collapsereset"></span><dl> <dt>**TVE \_ COLLAPSERESET**</dt> </dl> | Réduit la liste et supprime les éléments enfants. L’indicateur d’état [**Tvis \_ EXPANDEDONCE**](tree-view-control-item-states.md) est réinitialisé. Cet indicateur doit être utilisé avec l' \_ indicateur de réduction TVE.<br/>                                                                 |
| <span id="TVE_EXPAND"></span><span id="tve_expand"></span><dl> <dt>**TVE \_ développer**</dt> </dl>                      | Développe la liste.<br/>                                                                                                                                                                                                                                                          |
| <span id="TVE_EXPANDPARTIAL"></span><span id="tve_expandpartial"></span><dl> <dt>**TVE \_ EXPANDPARTIAL**</dt> </dl> | [Version 4,70](common-control-versions.md). Développe partiellement la liste. Dans cet État, les éléments enfants sont visibles et le signe plus (+) de l’élément parent, indiquant qu’il peut être développé, est affiché. Cet indicateur doit être utilisé en association avec l' \_ indicateur de développement TVE.<br/> |
| <span id="TVE_TOGGLE"></span><span id="tve_toggle"></span><dl> <dt>**TVE \_ bascule**</dt> </dl>                      | Réduit la liste si elle est développée ou développée si elle est réduite.<br/>                                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers l’élément parent à développer ou réduire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro si l’opération a réussi, ou zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

Le développement d’un nœud déjà développé est considéré comme une opération réussie et [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) retourne une valeur différente de zéro. La réduction d’un nœud retourne la valeur zéro si le nœud est déjà réduit ; Sinon, elle retourne une valeur différente de zéro. Toute tentative de développement ou de réduction d’un nœud qui n’a pas d’enfants est considérée comme un échec et **SendMessage** retourne la valeur zéro.

Lorsqu’un élément est développé pour la première fois par un message de **\_ développement TVM** , l’action génère des codes de notification [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) et [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) et l' [**indicateur d’État Tvis EXPANDEDONCE de \_**](tree-view-control-item-states.md) l’élément est défini. Tant que cet indicateur d’état reste défini, les messages de l' **\_ extension TVM** suivante ne génèrent pas de \_ notifications TVN ITEMEXPANDING ou TVN \_ ITEMEXPANDED. Pour réinitialiser l’indicateur d’état **Tvis \_ EXPANDEDONCE** , vous devez envoyer un message de **\_ développement TVM** avec les \_ indicateurs TVE Collapse et TVE \_ COLLAPSERESET définis. Toute tentative de définition explicite de **\_ EXPANDEDONCE Tvis** entraîne un comportement imprévisible.

L’opération de développement peut échouer si le propriétaire du contrôle TreeView refuse l’opération en réponse à une [notification \_ ITEMEXPANDING TVN](tvn-itemexpanding.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

