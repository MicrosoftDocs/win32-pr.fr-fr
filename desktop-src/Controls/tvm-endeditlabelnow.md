---
title: Message TVM_ENDEDITLABELNOW (commctrl. h)
description: Termine la modification de l’étiquette d’un élément d’affichage d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro EndEditLabelNow TreeView.
ms.assetid: 68de2020-9311-4958-859a-de55f5e41fcf
keywords:
- TVM_ENDEDITLABELNOW les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_ENDEDITLABELNOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f059be20560adeb8cbcb0c63a2555283f6b7051
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115734"
---
# <a name="tvm_endeditlabelnow-message"></a>TVM \_ ENDEDITLABELNOW message

Termine la modification de l’étiquette d’un élément d’affichage d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ EndEditLabelNow TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Variable qui indique si la modification est annulée sans être enregistrée dans l’étiquette. Si ce paramètre a la **valeur true**, le système annule la modification sans enregistrer les modifications. Dans le cas contraire, le système enregistre les modifications apportées à l’étiquette.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Ce message entraîne l’envoi du code de notification [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) à la fenêtre parente du contrôle Tree-View.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





