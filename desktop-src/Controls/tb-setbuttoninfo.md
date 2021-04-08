---
title: Message TB_SETBUTTONINFO (commctrl. h)
description: Définit les informations d’un bouton existant dans une barre d’outils.
ms.assetid: ac9b88b9-d0d0-4669-a342-708924d97c8b
keywords:
- TB_SETBUTTONINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETBUTTONINFO
- TB_SETBUTTONINFOA
- TB_SETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70612a90f245a25dde5a487917d7c3b669424ea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844262"
---
# <a name="tb_setbuttoninfo-message"></a>TO \_ SETBUTTONINFO message

Définit les informations d’un bouton existant dans une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur du bouton.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) qui contient les informations sur le nouveau bouton. Les membres **cbSize** et **dwMask** de cette structure doivent être renseignés avant l’envoi de ce message.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Notes

Le texte est généralement affecté à des boutons lorsqu’ils sont ajoutés à une barre d’outils en spécifiant l’index d’une chaîne dans le pool de chaînes de la barre d’outils. Si vous utilisez un **\_ SETBUTTONINFO to** pour assigner un nouveau texte à un bouton, il remplace définitivement le texte du pool de chaînes. Vous pouvez modifier le texte en appelant à nouveau **to \_ SETBUTTONINFO** , mais vous ne pouvez pas réassigner la chaîne à partir du pool de chaînes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **To \_ SETBUTTONINFOW** (Unicode) et **to \_ SETBUTTONINFOA** (ANSI)<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**TO \_ ADDBUTTONS**](tb-addbuttons.md)
</dt> <dt>

[**TO \_ GETBUTTONINFO**](tb-getbuttoninfo.md)
</dt> <dt>

[**TO \_ GETBUTTONTEXT**](tb-getbuttontext.md)
</dt> <dt>

[**TO \_ GETSTRING**](tb-getstring.md)
</dt> <dt>

[**TO \_ INSERTBUTTON**](tb-insertbutton.md)
</dt> </dl>

 

 





