---
title: Message WM_DEADCHAR (winuser. h)
description: Publié dans la fenêtre qui a le focus clavier lorsqu’un \_ message WM KEYUP est traduit par la fonction TranslateMessage.
ms.assetid: ada9a61c-dabf-447b-ae13-91803c097f0d
keywords:
- WM_DEADCHAR l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_DEADCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6053095b912360e9875fa062c2daba7cafcfd43b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464939"
---
# <a name="wm_deadchar-message"></a>\_Message WM DEADCHAR

Publié dans la fenêtre qui a le focus clavier lorsqu’un message [**WM \_ KEYUP**](wm-keyup.md) est traduit par la fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) . **WM \_ DEADCHAR** spécifie un code de caractère généré par une clé morte. Une clé morte est une clé qui génère un caractère, tel que le tréma (double point), qui est combiné avec un autre caractère pour former un caractère composite. Par exemple, le caractère Umlaut-O () est généré en tapant la touche morte pour le caractère tréma, puis en tapant la touche O.


```C++
#define WM_DEADCHAR                     0x0103
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Code de caractère généré par la touche morte.

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

## <a name="return-value"></a>Valeur retournée

Une application doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Notes

Le message **WM \_ DEADCHAR** est généralement utilisé par les applications pour fournir à l’utilisateur des commentaires sur chaque touche enfoncée. Par exemple, une application peut afficher l’accent à la position actuelle du caractère sans déplacer le signe insertion.

Étant donné qu’il n’y a pas nécessairement une correspondance un-à-un entre les touches enfoncées et les messages de caractères générés, les informations contenues dans le mot de poids fort du paramètre *lParam* ne sont généralement pas utiles aux applications. Les informations contenues dans le mot de poids fort ne s’appliquent qu’au dernier message de la [**\_ touche WM**](wm-keydown.md) qui précède la publication du message **WM \_ DEADCHAR** .

Pour les claviers à touche 101 et 102 améliorés, les touches étendues sont les touches ALT et droite de la section principale du clavier. les touches Inser, DEL, début, fin, PAGE précédente, PAGE suivante et flèche dans les clusters à gauche du pavé numérique ; et les touches de division (/) et de saisie dans le pavé numérique. D’autres claviers peuvent prendre en charge le bit de clé étendue dans le paramètre *lParam* .

## <a name="requirements"></a>Configuration requise



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

[**WM- \_ touche**](wm-keydown.md)
</dt> <dt>

[**WM \_ KEYUP**](wm-keyup.md)
</dt> <dt>

[**\_SYSDEADCHAR WM**](wm-sysdeadchar.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Entrée au clavier](keyboard-input.md)
</dt> </dl>

 

