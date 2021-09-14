---
title: Message WM_VKEYTOITEM (winuser. h)
description: Envoyé par une zone de liste avec le \_ style WANTKEYBOARDINPUT lbs à son propriétaire en réponse à un message « WM KeyOut \_ ».
ms.assetid: 2eab922f-7298-436f-bd94-0eefae7284d5
keywords:
- WM_VKEYTOITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- WM_VKEYTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1685682d8305fff5d9d93ef59d8859e099e6ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115137"
---
# <a name="wm_vkeytoitem-message"></a>\_Message WM VKEYTOITEM

Envoyé par une zone de liste avec le style [**\_ WANTKEYBOARDINPUT lbs**](list-box-styles.md) à son propriétaire en réponse à un message « [**WM \_**](/windows/desktop/inputdev/wm-keydown) KeyOut ».


```C++
WM_VKEYTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie le code de la touche virtuelle de la touche sur laquelle l’utilisateur a appuyé. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la position actuelle du signe insertion.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers la zone de liste.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour spécifie l’action exécutée par l’application en réponse au message. Une valeur de retour de-2 indique que l’application a géré tous les aspects de la sélection de l’élément et ne nécessite aucune action supplémentaire de la zone de liste. (Consultez la section Notes.) Une valeur de retour de-1 indique que la zone de liste doit exécuter l’action par défaut en réponse à la séquence de touches. Une valeur de retour supérieure ou égale à 0 spécifie l’index d’un élément dans la zone de liste et indique que la zone de liste doit exécuter l’action par défaut pour la séquence d’entrée sur l’élément spécifié.

## <a name="remarks"></a>Notes

Une valeur de retour de-2 est valide uniquement pour les clés qui ne sont pas converties en caractères par le contrôle de zone de liste. Si le message [**WM \_ keyverse**](/windows/desktop/inputdev/wm-keydown) se traduit par un message [**WM \_ char**](/windows/desktop/inputdev/wm-char) et que l’application traite le message **WM \_ VKEYTOITEM** généré à la suite de la pression sur la touche, la zone de liste ignore la valeur de retour et effectue le traitement par défaut pour ce caractère. **WM \_ Les messages** KeyOut générés par des clés telles que VK \_ up, VK \_ , VK \_ Next et VK \_ Previous ne sont pas traduits en messages **WM \_ char** . Dans ce cas, le fait de piéger le message **WM \_ VKEYTOITEM** et de retourner-2 empêche la zone de liste d’exécuter le traitement par défaut pour cette clé.

Pour intercepter les clés qui génèrent un message de type char et effectuer un traitement spécial, l’application doit sous-classer la zone de liste, intercepter les messages [**WM \_ keyverse**](/windows/desktop/inputdev/wm-keydown) et [**WM \_ char**](/windows/desktop/inputdev/wm-char) et traiter les messages de manière appropriée dans la procédure de sous-classe.

Les remarques précédentes s’appliquent aux zones de liste régulières créées avec le style [**\_ WANTKEYBOARDINPUT**](list-box-styles.md) . Si la zone de liste est owner-drawn, l’application doit traiter le message [**WM \_ CHARTOITEM**](wm-chartoitem.md) .

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne-1.

Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en valeur **booléenne** et retourner la valeur directement. La \_ valeur DWL MSGRESULT définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_CHARTOITEM WM**](wm-chartoitem.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM- \_ touche**](/windows/desktop/inputdev/wm-keydown)
</dt> </dl>

 

