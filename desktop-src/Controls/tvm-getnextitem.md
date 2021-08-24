---
title: Message TVM_GETNEXTITEM (commctrl. h)
description: Récupère l’élément d’arborescence qui porte la relation spécifiée à un élément spécifié. Vous pouvez envoyer ce message de manière explicite, à l’aide de la \_ macro GetNextItem TreeView.
ms.assetid: 505c713c-7728-4119-bc0e-482fe7e73193
keywords:
- TVM_GETNEXTITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_GETNEXTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84dbbd39ca347bcf1084ddfaa46c997cc5c4e5dd4d52250136a230dd834ac836
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698679"
---
# <a name="tvm_getnextitem-message"></a>TVM \_ GETNEXTITEM message

Récupère l’élément d’arborescence qui porte la relation spécifiée à un élément spécifié. Vous pouvez envoyer ce message de manière explicite, à l’aide de la macro [**\_ GetNextItem TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextitem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indicateur spécifiant l’élément à récupérer. Ce paramètre peut prendre l’une des valeurs suivantes :



| Valeur                                                                                                                                                                              | Signification                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <dt>**\_signe insertion TVGN**</dt> </dl>                               | Récupère l’élément actuellement sélectionné. Vous pouvez utiliser la macro [**TreeView \_ GetSelection**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection) pour envoyer ce message.<br/>                                                                                                                                                                          |
| <span id="TVGN_CHILD"></span><span id="tvgn_child"></span><dl> <dt>**\_enfant TVGN**</dt> </dl>                               | Récupère le premier élément enfant de l’élément spécifié par le paramètre *hitem* . Vous pouvez utiliser la [**macro \_ GetChild TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild) pour envoyer ce message.<br/>                                                                                                                                          |
| <span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <dt>**TVGN \_ DROPHILITE**</dt> </dl>                | Récupère l’élément qui est la cible d’une opération de glisser-déplacer. Vous pouvez utiliser la [**macro \_ GetDropHilight TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight) pour envoyer ce message.<br/>                                                                                                                                         |
| <span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <dt>**TVGN \_ FIRSTVISIBLE**</dt> </dl>          | Récupère le premier élément qui est visible dans la fenêtre d’arborescence. Vous pouvez utiliser la [**macro \_ GetFirstVisible TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) pour envoyer ce message.<br/>                                                                                                                                         |
| <span id="TVGN_LASTVISIBLE"></span><span id="tvgn_lastvisible"></span><dl> <dt>**TVGN \_ LASTVISIBLE**</dt> </dl>             | [Version 4,71](common-control-versions.md). Récupère le dernier élément développé dans l’arborescence. Cela ne récupère pas le dernier élément visible dans la fenêtre d’arborescence. Vous pouvez utiliser la [**macro \_ GetLastVisible TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible) pour envoyer ce message.<br/>                                            |
| <span id="TVGN_NEXT"></span><span id="tvgn_next"></span><dl> <dt>**TVGN \_ suivant**</dt> </dl>                                  | Récupère l’élément frère suivant. Vous pouvez utiliser la [**macro \_ GetNextSibling TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling) pour envoyer ce message.<br/>                                                                                                                                                                            |
| <span id="TVGN_NEXTSELECTED"></span><span id="tvgn_nextselected"></span><dl> <dt>**TVGN \_ NEXTSELECTED**</dt> </dl>          | **Windows Vista et versions ultérieures.** Récupère l'élément sélectionné suivant. Vous pouvez utiliser la [**macro \_ GetNextSelected TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextselected) pour envoyer ce message.<br/>                                                                                                                                            |
| <span id="TVGN_NEXTVISIBLE"></span><span id="tvgn_nextvisible"></span><dl> <dt>**TVGN \_ NEXTVISIBLE**</dt> </dl>             | Récupère l’élément visible suivant qui suit l’élément spécifié. L’élément spécifié doit être visible. Utilisez le message [**TVM \_ GETITEMRECT**](tvm-getitemrect.md) pour déterminer si un élément est visible. Vous pouvez utiliser la [**macro \_ GetNextVisible TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible) pour envoyer ce message.<br/>   |
| <span id="TVGN_PARENT"></span><span id="tvgn_parent"></span><dl> <dt>**TVGN \_ parent**</dt> </dl>                            | Récupère le parent de l’élément spécifié. Vous pouvez utiliser la macro [**TreeView \_ GetParent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent) pour envoyer ce message.<br/>                                                                                                                                                                           |
| <span id="TVGN_PREVIOUS"></span><span id="tvgn_previous"></span><dl> <dt>**TVGN \_ précédent**</dt> </dl>                      | Récupère l’élément frère précédent. Vous pouvez utiliser la [**macro \_ GetPrevSibling TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling) pour envoyer ce message.<br/>                                                                                                                                                                        |
| <span id="TVGN_PREVIOUSVISIBLE"></span><span id="tvgn_previousvisible"></span><dl> <dt>**TVGN \_ PREVIOUSVISIBLE**</dt> </dl> | Récupère le premier élément visible qui précède l’élément spécifié. L’élément spécifié doit être visible. Utilisez le message [**TVM \_ GETITEMRECT**](tvm-getitemrect.md) pour déterminer si un élément est visible. Vous pouvez utiliser la [**macro \_ GetPrevVisible TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible) pour envoyer ce message.<br/> |
| <span id="TVGN_ROOT"></span><span id="tvgn_root"></span><dl> <dt>**\_racine TVGN**</dt> </dl>                                  | Récupère le premier ou le dernier élément du contrôle Tree-View. Vous pouvez utiliser la [**macro \_ GetRoot TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot) pour envoyer ce message. <br/>                                                                                                                                                       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers un élément.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle de l’élément en cas de réussite. Dans la plupart des cas, le message retourne une valeur **null** pour indiquer une erreur. Pour plus d'informations, consultez la section Notes.

## <a name="remarks"></a>Remarques

Ce message retourne la **valeur null** si l’élément récupéré est le nœud racine de l’arborescence. Par exemple, si vous utilisez ce message avec l' \_ indicateur parent TVGN sur un enfant de premier niveau du nœud racine de la vue d’arborescence, le message retourne la **valeur null**.

Vous pouvez également utiliser l’une des macros associées suivantes :



|                                                               |
|---------------------------------------------------------------|
| [**\_GetChild TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild)               |
| [**\_GetDropHilight TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight)   |
| [**\_GetFirstVisible TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) |
| [**\_GetLastVisible TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible)   |
| [**\_GetNextSibling TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling)   |
| [**\_GetNextVisible TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible)   |
| [**TreeView \_ GetParent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent)             |
| [**\_GetPrevSibling TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling)   |
| [**\_GetPrevVisible TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible)   |
| [**\_GetRoot TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot)                 |
| [**\_GetSelection TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection)       |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





