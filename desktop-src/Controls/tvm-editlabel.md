---
title: Message TVM_EDITLABEL (commctrl. h)
description: Commence la modification sur place du texte de l’élément spécifié, en remplaçant le texte de l’élément par un contrôle d’édition sur une seule ligne qui contient le texte.
ms.assetid: ae844cbf-fa43-4f91-90cc-688f44bf77a5
keywords:
- TVM_EDITLABEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_EDITLABEL
- TVM_EDITLABELA
- TVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3608c3f959c45571d9bc085518b763cf505180ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941942"
---
# <a name="tvm_editlabel-message"></a>TVM \_ EDITLABEL message

Commence la modification sur place du texte de l’élément spécifié, en remplaçant le texte de l’élément par un contrôle d’édition sur une seule ligne qui contient le texte. Ce message sélectionne et concentre implicitement l’élément spécifié. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ EditLabel TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Handle de l’élément à modifier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle du contrôle d’édition utilisé pour modifier le texte de l’élément en cas de réussite, ou **null** dans le cas contraire.

## <a name="remarks"></a>Notes

Ce message envoie un code de notification [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) au parent du contrôle Tree-View.

Lorsque l’utilisateur termine ou annule la modification, le contrôle d’édition est détruit et le descripteur n’est plus valide. Vous pouvez sous-définir le contrôle d’édition, mais ne le détruisez pas.

Le contrôle doit avoir le focus avant d’envoyer ce message au contrôle. Le focus peut être défini à l’aide de la fonction [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVM \_ EDITLABELW** (Unicode) et **TVM \_ EDITLABELA** (ANSI)<br/>               |



 

