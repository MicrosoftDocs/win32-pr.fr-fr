---
title: États de l’élément de contrôle Tree-View (CommCtrl. h)
description: Cette section répertorie les indicateurs d’état d’élément utilisés pour indiquer l’état d’un élément dans un contrôle Tree-View.
ms.assetid: 5b11d575-6dfd-47a8-b959-b19aaeeca70e
topic_type:
- apiref
api_name:
- TVIS_BOLD
- TVIS_CUT
- TVIS_DROPHILITED
- TVIS_EXPANDED
- TVIS_EXPANDEDONCE
- TVIS_EXPANDPARTIAL
- TVIS_SELECTED
- TVIS_OVERLAYMASK
- TVIS_STATEIMAGEMASK
- TVIS_USERMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4a19306855b7f38d03aa00323b26407f108bfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541070"
---
# <a name="tree-view-control-item-states"></a>États des éléments de contrôle Tree-View

Cette section répertorie les indicateurs d’état d’élément utilisés pour indiquer l’état d’un élément dans un contrôle Tree-View.



| Constante                                                                                                                                                                        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVIS_BOLD"></span><span id="tvis_bold"></span><dl> <dt>**TVIS \_ gras**</dt> </dl>                               | L’élément est en gras.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_CUT"></span><span id="tvis_cut"></span><dl> <dt>**TVIS \_ couper**</dt> </dl>                                  | L’élément est sélectionné dans le cadre d’une opération de couper-coller. <br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TVIS_DROPHILITED"></span><span id="tvis_drophilited"></span><dl> <dt>**TVIS \_ DROPHILITED**</dt> </dl>          | L’élément est sélectionné comme cible de glisser-déplacer.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_EXPANDED"></span><span id="tvis_expanded"></span><dl> <dt>**TVIS \_ développé**</dt> </dl>                   | La liste des éléments enfants de l’élément est actuellement développée ; autrement dit, les éléments enfants sont visibles. Cette valeur s’applique uniquement aux éléments parents.<br/>                                                                                                                                                                                                                                                                                                                  |
| <span id="TVIS_EXPANDEDONCE"></span><span id="tvis_expandedonce"></span><dl> <dt>**TVIS \_ EXPANDEDONCE**</dt> </dl>       | La liste des éléments enfants de l’élément a été développée au moins une fois. Les codes de notification [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) et [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) ne sont pas générés pour les éléments parents pour lesquels cet État est défini en réponse à un message de [**\_ développement TVM**](tvm-expand.md) . L’utilisation de TVE \_ Collapse et TVE \_ COLLAPSERESET avec **TVM \_ expand** entraîne la réinitialisation de cet État. Cette valeur s’applique uniquement aux éléments parents. <br/> |
| <span id="TVIS_EXPANDPARTIAL"></span><span id="tvis_expandpartial"></span><dl> <dt>**TVIS \_ EXPANDPARTIAL**</dt> </dl>    | **Version 4,70**. Élément d’arborescence partiellement développé. Dans cet État, certains, mais pas tous, des éléments enfants sont visibles et le symbole plus du parent de l’élément est affiché. <br/>                                                                                                                                                                                                                                                                              |
| <span id="TVIS_SELECTED"></span><span id="tvis_selected"></span><dl> <dt>**TVIS \_ sélectionné**</dt> </dl>                   | L'élément est sélectionné. Son apparence varie selon qu’elle a le focus. L’élément est dessiné à l’aide des couleurs système pour la sélection. <br/>                                                                                                                                                                                                                                                                                                              |
| <span id="TVIS_OVERLAYMASK"></span><span id="tvis_overlaymask"></span><dl> <dt>**TVIS \_ OVERLAYMASK**</dt> </dl>          | Masque pour les bits utilisés pour spécifier l’index d’image de superposition de l’élément.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_STATEIMAGEMASK"></span><span id="tvis_stateimagemask"></span><dl> <dt>**TVIS \_ STATEIMAGEMASK**</dt> </dl> | Masque pour les bits utilisés pour spécifier l’index d’image d’état de l’élément.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_USERMASK"></span><span id="tvis_usermask"></span><dl> <dt>**TVIS \_ USERMASK**</dt> </dl>                   | Identique à **Tvis \_ STATEIMAGEMASK**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="remarks"></a>Notes

Lorsque vous définissez ou récupérez l’index d’image de superposition ou l’index d’images d’état d’un élément, vous devez spécifier les masques suivants dans le membre **stateMask** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) :

-   **TVIS \_ OVERLAYMASK**
-   **TVIS \_ STATEIMAGEMASK**
-   **TVIS \_ USERMASK**

Ces valeurs peuvent également être utilisées pour masquer les bits d’État qui ne sont pas intéressants.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





