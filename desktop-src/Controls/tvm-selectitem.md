---
title: Message TVM_SELECTITEM (commctrl. h)
description: Sélectionne l’élément d’affichage d’arborescence spécifié, fait défiler l’élément dans l’affichage ou redessine l’élément dans le style utilisé pour indiquer la cible d’une opération de glisser-déplacer.
ms.assetid: 8b943958-7b93-4e54-99de-200121cf0752
keywords:
- TVM_SELECTITEM les contrôles de message Windows
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
ms.openlocfilehash: 94862b64a02cd8972e3da38a75282d99bbc1cbc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843245"
---
# <a name="tvm_selectitem-message"></a>TVM \_ SELECTITEM message

Sélectionne l’élément d’affichage d’arborescence spécifié, fait défiler l’élément dans l’affichage ou redessine l’élément dans le style utilisé pour indiquer la cible d’une opération de glisser-déplacer. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TreeView \_ Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select), [**TreeView \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)ou [**TreeView \_ SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indicateur d’action. Ce paramètre peut prendre l’une des valeurs suivantes :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <dt><strong>TVGN_CARET</strong></dt> </dl></td>
<td>Définit la sélection sur l’élément spécifié. La fenêtre parente du contrôle Tree-View reçoit les codes de notification <a href="tvn-selchanging.md">TVN_SELCHANGING</a> et <a href="tvn-selchanged.md">TVN_SELCHANGED</a> . <br/></td>
</tr>
<tr class="even">
<td><span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <dt><strong>TVGN_DROPHILITE</strong></dt> </dl></td>
<td>Redessine l’élément spécifié dans le style utilisé pour indiquer la cible d’une opération de glisser-déplacer.<br/></td>
</tr>
<tr class="odd">
<td><span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </dl></td>
<td>Garantit que l’élément spécifié est visible et, si possible, l’affiche en haut de la fenêtre du contrôle. Les contrôles d’arborescence affichent autant d’éléments que possible dans la fenêtre. Si l’élément spécifié est proche du bas de la hiérarchie d’éléments du contrôle, il peut ne pas devenir le premier élément visible, en fonction du nombre d’éléments qui tiennent dans la fenêtre.<br/></td>
</tr>
<tr class="even">
<td><span id="TVSI_NOSINGLEEXPAND"></span><span id="tvsi_nosingleexpand"></span><dl> <dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </dl></td>
<td>Lorsqu’un seul élément est sélectionné, vérifie que le TreeView ne développe pas les enfants de cet élément. Cela n’est valide que s’il est utilisé avec l’indicateur TVGN_CARET. <br/>
<blockquote>
[!Note]<br />
Pour utiliser cet indicateur, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez <a href="cookbook-overview.md">activation des styles visuels</a>.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers un élément. Si *lParam* a la **valeur null**, le contrôle est défini sur ne pas avoir d’élément sélectionné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Si l’élément spécifié est l’enfant d’un élément parent réduit, la liste des éléments enfants du parent est développée pour révéler l’élément spécifié. Dans ce cas, la fenêtre parente du contrôle reçoit les codes de notification [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) et [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) .

L’utilisation de la macro [**\_ SelectItem TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) revient à envoyer le message **TVM \_ SelectItem** avec *wParam* défini sur la \_ valeur du signe insertion TVGN. L’utilisation de la macro [**\_ SelectDropTarget TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) revient à envoyer le message **TVM \_ SELECTITEM** avec *wParam* défini sur la \_ valeur DROPHILITE TVGN. L’utilisation de [**TreeView \_ SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) revient à envoyer le message **TVM \_ SELECTITEM** avec *wParam* défini sur la \_ valeur FIRSTVISIBLE TVGN.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





