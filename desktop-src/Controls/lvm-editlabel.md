---
title: Message LVM_EDITLABEL (commctrl. h)
description: Commence la modification sur place du texte de l’élément d’affichage de liste spécifié. Le message sélectionne et concentre implicitement l’élément spécifié. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView EditLabel.
ms.assetid: b63f13f1-6e66-4770-af84-30bcdb241727
keywords:
- LVM_EDITLABEL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_EDITLABEL
- LVM_EDITLABELA
- LVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9be1896c39e06c25bf06e033d74a17107b3e194a43b1c574e1dcb7f9a456413
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411843"
---
# <a name="lvm_editlabel-message"></a>\_Message EDITLABEL LVM

Commence la modification sur place du texte de l’élément d’affichage de liste spécifié. Le message sélectionne et concentre implicitement l’élément spécifié. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’élément de vue de liste. Pour annuler la modification, affectez la valeur-1 à l’index.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle du contrôle d’édition utilisé pour modifier le texte de l’élément en cas de réussite, ou **null** dans le cas contraire.

## <a name="remarks"></a>Remarques

Lorsque l’utilisateur termine ou annule la modification, le contrôle d’édition est détruit et le descripteur n’est plus valide. Vous pouvez sous-définir le contrôle d’édition, mais vous ne devez pas le détruire.

Le contrôle doit avoir le focus avant d’envoyer ce message au contrôle. Le focus peut être défini à l’aide de la fonction [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .

Si *wParam* est-1, un code de notification [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) est envoyé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVM \_ EDITLABELW** (Unicode) et **LVM \_ EDITLABELA** (ANSI)<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_CANCELMODE WM**](/windows/desktop/winmsg/wm-cancelmode)
</dt> </dl>

 

