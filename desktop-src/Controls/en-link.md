---
title: Code de notification EN_LINK (RichEdit. h)
description: Un contrôle RichEdit envoie \_ des codes de notification en lien lorsqu’il reçoit divers messages, par exemple lorsque l’utilisateur clique sur la souris ou lorsque le pointeur de la souris se trouve sur le texte qui a l' \_ effet de lien CFE.
ms.assetid: 67f02908-957e-4d91-8a70-70399ce9cf2e
keywords:
- EN_LINK les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- EN_LINK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3398f79a94982a8b7c843747f38f16431cad6a061388367037d259cfe862d468
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047659"
---
# <a name="en_link-notification-code"></a>\_Code de notification en lien

Un contrôle RichEdit envoie \_ des codes de notification en lien lorsqu’il reçoit divers messages, par exemple lorsque l’utilisateur clique sur la souris ou lorsque le pointeur de la souris se trouve sur le texte qui a l’effet de **\_ lien CFE** . Un contrôle RichEdit sans fenêtre envoie cette notification à l’aide de la méthode [**ITextHost :: TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) . La fenêtre parente du contrôle reçoit ce code de notification via un message [**WM \_ Notify**](wm-notify.md) .


```C++
EN_LINK

    penLink = (ENLINK *) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

ID de fenêtre récupéré en appelant la fonction [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) avec la \_ valeur d’ID GWL.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur désignant une structure d' [**enlien**](/windows/desktop/api/Richedit/ns-richedit-enlink) . La structure contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , des informations sur le code de notification et une structure [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) qui indique la plage de caractères qui ont l’effet de **\_ lien CFE** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne zéro pour permettre au contrôle de poursuivre sa gestion normale du message.

Retourne une valeur différente de zéro pour empêcher le contrôle de gérer le message.

**Windows 8**: return **\_ -fr LINK \_ effectuent \_ par défaut** le contrôle rich edit pour exécuter l’action par défaut.

## <a name="remarks"></a>Remarques

Pour recevoir des codes de notification en **\_ lien** lorsque le lien a le focus, spécifiez l’indicateur de [**\_ lien ENM**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .

Si le lien n’a pas le focus, pour recevoir les codes de notification en **\_ lien** , spécifiez l’indicateur **\_ NOFOCUSLINKNOTIFY ses** dans le masque envoyé avec le message [**em \_ SETEDITSTYLE**](em-seteditstyle.md) .

Un contrôle RichEdit envoie des codes de notification en **\_ lien** lorsqu’il reçoit les messages suivants lorsque le pointeur de la souris se trouve sur le texte qui a l’effet de **\_ lien CFE** :

-   [**\_LBUTTONDBLCLK WM**](/windows/desktop/inputdev/wm-lbuttondblclk)
-   [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown)
-   [**\_LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup)
-   [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)
-   [**\_RBUTTONDBLCLK WM**](/windows/desktop/inputdev/wm-rbuttondblclk)
-   [**\_RBUTTONDOWN WM**](/windows/desktop/inputdev/wm-rbuttondown)
-   [**\_RBUTTONUP WM**](/windows/desktop/inputdev/wm-rbuttonup)
-   [**\_SETCURSOR WM**](/windows/desktop/menurc/wm-setcursor)

L’effet de **\_ lien CFE** identifie généralement une plage de texte qui contient une URL. Les applications peuvent gérer le \_ Code de notification en lien en modifiant le pointeur de la souris lorsqu’il se trouve sur l’URL, ou en démarrant un navigateur pour afficher l’emplacement identifié par l’URL.

Si vous envoyez le message [**em \_ AUTOURLDETECT**](em-autourldetect.md) pour activer la détection automatique des URL, le contrôle Rich Edit définit automatiquement l’effet de **\_ lien CFE** pour le texte modifié qu’il identifie en tant qu’URL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> <dt>

[**\_AUTOURLDETECT em**](em-autourldetect.md)
</dt> <dt>

[**Créer un lien**](/windows/desktop/api/Richedit/ns-richedit-enlink)
</dt> <dt>

[**ITextRange2 :: SetURL**](/windows/desktop/api/Tom/nf-tom-itextrange2-seturl)
</dt> <dt>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> </dl>

 

