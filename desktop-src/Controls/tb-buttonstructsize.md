---
title: Message TB_BUTTONSTRUCTSIZE (commctrl. h)
description: Spécifie la taille de la structure TBBUTTON.
ms.assetid: 4e63a075-4191-44c1-8df6-38fce51d4be5
keywords:
- TB_BUTTONSTRUCTSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_BUTTONSTRUCTSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7187c1f4cb45306fd293c7eb74ef8807f395ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033267"
---
# <a name="tb_buttonstructsize-message"></a>TO \_ BUTTONSTRUCTSIZE message

Spécifie la taille de la structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Taille, en octets, de la structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) .

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le système utilise la taille pour déterminer la version de la bibliothèque de liens dynamiques (DLL) de contrôle commun qui est utilisée.

Si une application utilise la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour créer la barre d’outils, l’application doit envoyer ce message à la barre d’outils avant d’envoyer le message [**to \_ ADDBITMAP**](tb-addbitmap.md) ou [**to \_ ADDBUTTONS**](tb-addbuttons.md) . La fonction [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) envoie automatiquement **to \_ BUTTONSTRUCTSIZE**, et la taille de la structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) est un paramètre de la fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

