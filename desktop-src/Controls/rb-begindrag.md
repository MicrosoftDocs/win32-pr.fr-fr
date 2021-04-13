---
title: Message RB_BEGINDRAG (commctrl. h)
description: Place le contrôle rebar en mode glisser-déplacer. Ce message n’entraîne pas l' \_ envoi d’une notification BEGINDRAG RBN.
ms.assetid: 1e3e4928-cb84-4fd4-8056-84de1f791d1c
keywords:
- RB_BEGINDRAG les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41865baa2bf6c640595296be9c157201d0cc16d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466090"
---
# <a name="rb_begindrag-message"></a>\_Message BEGINDRAG RB

Place le contrôle rebar en mode glisser-déplacer. Ce message n’entraîne pas l’envoi d’une notification [ \_ BEGINDRAG RBN](rbn-begindrag.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la bande affecté par l’opération de glisser-déplacer.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur **DWORD** qui contient les coordonnées de début de la souris. La coordonnée horizontale est contenue dans le LOWORD et la coordonnée verticale est contenue dans le HIWORD. Si vous transmettez (**DWORD**)-1, le contrôle rebar utilise la position de la souris la dernière fois que le thread du contrôle a appelé [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message n’est pas utilisée.

## <a name="remarks"></a>Notes

Les **messages \_ RB BEGINDRAG**, [**RB \_ DRAGMOVE**](rb-dragmove.md)et [**RB \_ ENDDRAG**](rb-enddrag.md) vous permettent d’implémenter une interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) pour un contrôle rebar. Vous envoyez le **message \_ RB BEGINDRAG** en réponse à [**IDropTarget ::D ragenter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), envoyez le message **RB \_ DRAGMOVE** en réponse à [**IDropTarget ::D Ragover**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover)et au message **RB \_ ENDDRAG** en réponse à [**IDropTarget ::D ROP**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) et [**IDropTarget ::D ragleave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

