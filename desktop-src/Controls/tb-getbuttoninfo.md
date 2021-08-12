---
title: Message TB_GETBUTTONINFO (commctrl. h)
description: Récupère des informations étendues pour un bouton dans une barre d’outils.
ms.assetid: 87430dd2-43d1-4e33-96ac-d33f89a654b6
keywords:
- TB_GETBUTTONINFO les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETBUTTONINFO
- TB_GETBUTTONINFOA
- TB_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 457b8ca82d570b9d6c55cf97392803fce9a81cbe1d5db8122fcdaa975dd99d5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669932"
---
# <a name="tb_getbuttoninfo-message"></a>TO \_ GETBUTTONINFO message

Récupère des informations étendues pour un bouton dans une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur de commande du bouton.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) qui reçoit les informations sur le bouton. Les membres **cbSize** et **dwMask** de cette structure doivent être renseignés avant l’envoi de ce message.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index de base zéro du bouton, ou-1 si une erreur se produit.

## <a name="remarks"></a>Remarques

Quand vous utilisez [**to \_ ADDBUTTONS**](tb-addbuttons.md) ou [**to \_ INSERTBUTTON**](tb-insertbutton.md) pour placer des boutons dans la barre d’outils, le texte du bouton est généralement spécifié par son index de pool de chaînes. **To \_ GETBUTTONINFO** ne récupère pas cette chaîne. Pour utiliser **to \_ GETBUTTONINFO** pour récupérer le texte du bouton, vous devez d’abord définir la chaîne de texte avec [**to \_ SETBUTTONINFO**](tb-setbuttoninfo.md). Une fois que vous avez défini le texte du bouton avec **to \_ SETBUTTONINFO**, vous ne pouvez plus utiliser l’index du pool de chaînes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **To \_ GETBUTTONINFOW** (Unicode) et **to \_ GETBUTTONINFOA** (ANSI)<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**TO \_ SETBUTTONINFO**](tb-setbuttoninfo.md)
</dt> <dt>

[**TO \_ GETBUTTONTEXT**](tb-getbuttontext.md)
</dt> </dl>

 

 





