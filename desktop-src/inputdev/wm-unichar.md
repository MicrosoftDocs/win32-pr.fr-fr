---
title: Message WM_UNICHAR (winuser. h)
description: Le \_ message WM UNICHAR peut être utilisé par une application pour envoyer une entrée à d’autres fenêtres.
ms.assetid: edbfcf14-0371-43ce-9676-eb10d964d0b7
keywords:
- WM_UNICHAR l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_UNICHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833b5cb59095f5aecc8c0172857c8761fd92449a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192135"
---
# <a name="wm_unichar-message"></a>\_Message WM UNICHAR

Le message **WM \_ UNICHAR** peut être utilisé par une application pour envoyer une entrée à d’autres fenêtres. Ce message contient le code de caractère de la touche qui a été enfoncée. (Tester si une application cible peut traiter les messages **WM \_ UNICHAR** en envoyant le message avec *wParam* défini sur **Unicode \_ nochar**.)


```C++
#define WM_UNICHAR                      0x0109
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Code de caractère de la clé.

Si *wParam* est **un \_ nochar Unicode** et que l’application traite ce message, retourne **true**. La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne la **valeur false** (valeur par défaut).

Si *wParam* n’est pas de **\_ type Unicode Nochar**, retourne **false**. Le  [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Unicode publie un [**message \_ WM**](wm-char.md) avec les mêmes paramètres et la fonction **DefWindowProc** ANSI publie un ou deux messages **WM \_ char** avec le ou les caractères ANSI correspondants.

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
| 31    | État de transition. La valeur est 1 si la touche est relâchée, ou 0 si la touche est enfoncée.                                                                                                                                                            |

Pour plus d’informations, consultez [indicateurs de message de frappe](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Une application doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Notes

Le message **WM \_ UNICHAR** est similaire à [**WM \_ char**](wm-char.md), mais il utilise le format UTF (Unicode Transformation Format)-32, alors que **WM \_ char** utilise UTF-16.

Ce message est conçu pour envoyer ou poster des caractères Unicode dans des fenêtres ANSI et peut gérer des caractères de plan supplémentaires Unicode.

Étant donné qu’il n’y a pas nécessairement une correspondance un-à-un entre les touches enfoncées et les messages de caractères générés, les informations contenues dans le mot de poids fort du paramètre *lParam* ne sont généralement pas utiles aux applications. Les informations contenues dans le mot de poids fort ne s’appliquent qu’au dernier message de la [**\_ touche WM**](wm-keydown.md) qui précède la publication du message **WM \_ UNICHAR** .

Pour les claviers à touche 101 et 102 améliorés, les touches étendues sont les touches ALT et droite de la section principale du clavier. les touches Inser, DEL, début, fin, PAGE précédente, PAGE suivante et flèche dans les clusters à gauche du pavé numérique ; et les touches de division (/) et de saisie dans le pavé numérique. D’autres claviers peuvent prendre en charge le bit de clé étendue dans le paramètre *lParam* .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**\_caractère WM**](wm-char.md)
</dt> <dt>

[**WM- \_ touche**](wm-keydown.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Entrée au clavier](keyboard-input.md)
</dt> </dl>

 

