---
title: Message WM_SYSCHAR (winuser. h)
description: Publié dans la fenêtre qui a le focus clavier lorsqu’un \_ message WM SYSKEYDOWN est traduit par la fonction TranslateMessage.
ms.assetid: 55987105-3c53-42e5-8fab-a3c9f2ca7273
keywords:
- WM_SYSCHAR des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_SYSCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b42d88d5ae1346032da2c663dd8c9189c030d5bb7d538ab7ef84403d42fba76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472087"
---
# <a name="wm_syschar-message"></a>\_Message WM SYSCHAR

Publié dans la fenêtre qui a le focus clavier lorsqu’un message [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) est traduit par la fonction [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) . Elle spécifie le code de caractère d’une touche de caractère système, c’est-à-dire une touche de caractère qui est enfoncée pendant que la touche ALT est enfoncée.


```C++
#define WM_SYSCHAR                      0x0106
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Code de caractère de la touche de menu de la fenêtre.

</dd> <dt>

*lParam* 
</dt> <dd>

Le nombre de répétitions, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de clé précédent et l’indicateur d’état de transition, comme indiqué dans le tableau suivant.



| Bits                                                                             | Signification                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 15</dt> </dl>  | Nombre de répétitions du message en cours. La valeur est le nombre de fois que la frappe a été répétée automatiquement à la suite de l’utilisateur qui maintient la touche enfoncée. Si la frappe de touche est suffisamment longue, plusieurs messages sont envoyés. Toutefois, le nombre de répétitions n’est pas cumulatif.<br/> |
| <dl> <dt>16 23</dt> </dl> | Code d’analyse. La valeur dépend du fabricant d’ordinateurs OEM (Original Equipment Manufacturer).<br/>                                                                                                                                                                                          |
| <dl> <dt>24</dt> </dl>    | Indique si la touche est une touche étendue, telle que les touches ALT et CTRL de droite qui s’affichent sur un clavier amélioré 101-ou 102-touches. La valeur est 1 s’il s’agit d’une clé étendue ; Sinon, la valeur est 0.<br/>                                                                |
| <dl> <dt>25 28</dt> </dl> | Réservé n’utilisez pas.<br/>                                                                                                                                                                                                                                                   |
| <dl> <dt>29</dt> </dl>    | Code de contexte. La valeur est 1 si la touche ALT est maintenue enfoncée pendant que la touche est enfoncée ; dans le cas contraire, la valeur est 0.<br/>                                                                                                                                                       |
| <dl> <dt>30</dt> </dl>    | État de la clé précédente. La valeur est 1 si la touche est enfoncée avant l’envoi du message ou 0 si la touche est active.<br/>                                                                                                                                                      |
| <dl> <dt>31</dt> </dl>    | État de transition. La valeur est 1 si la touche est relâchée, ou 0 si la touche est enfoncée.<br/>                                                                                                                                                              |

Pour plus d’informations, consultez [indicateurs de message de frappe](../inputdev/about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une application doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Remarques

Lorsque le code de contexte est égal à zéro, le message peut être passé à la fonction [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) , qui le gère comme s’il s’agissait d’un message de clé standard au lieu d’un message de touche de caractère système. Cela permet d’utiliser les touches d’accès rapide avec la fenêtre active, même si la fenêtre active n’a pas le focus clavier.

Pour les claviers à touche 101 et 102 améliorés, les touches étendues sont les touches ALT et CTRL appropriées sur la section principale du clavier. les touches Inser, DEL, début, fin, PAGE précédente, PAGE suivante et flèche dans les clusters à gauche du pavé numérique ; touche Impr. SCRN. touche Attn ; touche VERR. num ; et les touches de division (/) et de saisie dans le pavé numérique. D’autres claviers peuvent prendre en charge le bit de clé étendue dans le paramètre.

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

[**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**\_SYSKEYDOWN WM**](/windows/desktop/inputdev/wm-syskeydown)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Raccourcis clavier](keyboard-accelerators.md)
</dt> </dl>

