---
title: Message WM_SYSDEADCHAR (winuser. h)
description: Envoyé à la fenêtre avec le focus clavier lorsqu’un \_ message WM SYSKEYDOWN est traduit par la fonction TranslateMessage.
ms.assetid: cf9a1171-a47c-4d7b-b351-31f41a893b20
keywords:
- WM_SYSDEADCHAR l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_SYSDEADCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2052f8ced24ac998a56a4365552fee4bc5e0b21e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523740"
---
# <a name="wm_sysdeadchar-message"></a>\_Message WM SYSDEADCHAR

Envoyé à la fenêtre avec le focus clavier lorsqu’un message [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) est traduit par la fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) . **WM \_ SYSDEADCHAR** spécifie le code de caractère d’une clé morte du système, c’est-à-dire une touche morte enfoncée tout en maintenant la touche Alt enfoncée.


```C++
#define WM_SYSDEADCHAR                  0x0107
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Code de caractère généré par la touche morte du système qui est, une touche morte enfoncée tout en maintenant la touche ALT enfoncée.

</dd> <dt>

*lParam* 
</dt> <dd>

Le nombre de répétitions, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de clé précédent et l’indicateur d’état de transition, comme indiqué dans le tableau suivant.



| Bits  | Signification                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Nombre de répétitions du message en cours. La valeur est le nombre de fois que la frappe est répétée de manière répétée à la suite de l’utilisateur qui maintient la touche enfoncée. Si la frappe de touche est suffisamment longue, plusieurs messages sont envoyés. Toutefois, le nombre de répétitions n’est pas cumulatif. |
| 16-23 | Code d’analyse. La valeur dépend du fabricant d’ordinateurs OEM.                                                                                                                                                                                                                          |
| 24    | Indique si la touche est une touche étendue, telle que les touches ALT et CTRL de droite qui s’affichent sur un clavier amélioré 101-ou 102-touches. La valeur est 1 s’il s’agit d’une clé étendue ; Sinon, la valeur est 0.                                                              |
| 25-28 | Réservé n’utilisez pas.                                                                                                                                                                                                                                                 |
| 29    | Code de contexte. La valeur est 1 si la touche ALT est maintenue enfoncée pendant que la touche est enfoncée ; dans le cas contraire, la valeur est 0.                                                                                                                                                     |
| 30    | État de la clé précédente. La valeur est 1 si la touche est enfoncée avant l’envoi du message ou 0 si la touche est active.                                                                                                                                                    |
| 31    | État de transition. La valeur est 1 si la touche est relâchée, ou 0 si la touche est enfoncée.                                                                                                                                                                |

Pour plus d’informations, consultez [indicateurs de message de frappe](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Une application doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Notes

Pour les claviers à touche 101 et 102 améliorés, les touches étendues sont les touches ALT et CTRL appropriées sur la section principale du clavier. les touches Inser, DEL, début, fin, PAGE précédente, PAGE suivante et flèche dans les clusters à gauche du pavé numérique ; et les touches de division (/) et de saisie dans le pavé numérique. D’autres claviers peuvent prendre en charge le bit de clé étendue dans le paramètre *lParam* .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**\_DEADCHAR WM**](wm-deadchar.md)
</dt> <dt>

[**\_SYSKEYDOWN WM**](wm-syskeydown.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Entrée au clavier](keyboard-input.md)
</dt> </dl>

 

