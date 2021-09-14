---
title: Message TVM_SELECTITEM (commctrl. h)
description: Sélectionne l’élément d’affichage d’arborescence spécifié, fait défiler l’élément dans l’affichage ou redessine l’élément dans le style utilisé pour indiquer la cible d’une opération de glisser-déplacer.
ms.assetid: 8b943958-7b93-4e54-99de-200121cf0752
keywords:
- TVM_SELECTITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_SELECTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ec7201358669fa49e6396508d371ca5e95d6fa1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115622"
---
# <a name="tvm_selectitem-message"></a>TVM \_ SELECTITEM message

Sélectionne l’élément d’affichage d’arborescence spécifié, fait défiler l’élément dans l’affichage ou redessine l’élément dans le style utilisé pour indiquer la cible d’une opération de glisser-déplacer. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TreeView \_ Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select), [**TreeView \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)ou [**TreeView \_ SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indicateur d’action. Ce paramètre peut prendre l’une des valeurs suivantes :




| Valeur | Signification | 
|-------|---------|
| <span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl><dt><strong>TVGN_CARET</strong></dt></dl> | Définit la sélection sur l’élément spécifié. La fenêtre parente du contrôle Tree-View reçoit les codes de notification <a href="tvn-selchanging.md">TVN_SELCHANGING</a> et <a href="tvn-selchanged.md">TVN_SELCHANGED</a> . <br /> | 
| <span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl><dt><strong>TVGN_DROPHILITE</strong></dt></dl> | Redessine l’élément spécifié dans le style utilisé pour indiquer la cible d’une opération de glisser-déplacer.<br /> | 
| <span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl><dt><strong>TVGN_FIRSTVISIBLE</strong></dt></dl> | Garantit que l’élément spécifié est visible et, si possible, l’affiche en haut de la fenêtre du contrôle. Les contrôles d’arborescence affichent autant d’éléments que possible dans la fenêtre. Si l’élément spécifié est proche du bas de la hiérarchie d’éléments du contrôle, il peut ne pas devenir le premier élément visible, en fonction du nombre d’éléments qui tiennent dans la fenêtre.<br /> | 
| <span id="TVSI_NOSINGLEEXPAND"></span><span id="tvsi_nosingleexpand"></span><dl><dt><strong>TVSI_NOSINGLEEXPAND</strong></dt></dl> | Lorsqu’un seul élément est sélectionné, vérifie que le TreeView ne développe pas les enfants de cet élément. Cela n’est valide que s’il est utilisé avec l’indicateur TVGN_CARET. <br /><blockquote>[!Note]<br />Pour utiliser cet indicateur, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez <a href="cookbook-overview.md">activation des styles visuels</a>.</blockquote><br /> | 




 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers un élément. Si *lParam* a la **valeur null**, le contrôle est défini sur ne pas avoir d’élément sélectionné.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Si l’élément spécifié est l’enfant d’un élément parent réduit, la liste des éléments enfants du parent est développée pour révéler l’élément spécifié. Dans ce cas, la fenêtre parente du contrôle reçoit les codes de notification [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) et [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) .

L’utilisation de la macro [**\_ SelectItem TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) revient à envoyer le message **TVM \_ SelectItem** avec *wParam* défini sur la \_ valeur du signe insertion TVGN. L’utilisation de la macro [**\_ SelectDropTarget TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) revient à envoyer le message **TVM \_ SELECTITEM** avec *wParam* défini sur la \_ valeur DROPHILITE TVGN. L’utilisation de [**TreeView \_ SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) revient à envoyer le message **TVM \_ SELECTITEM** avec *wParam* défini sur la \_ valeur FIRSTVISIBLE TVGN.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





