---
title: Message WM_SYSCOMMAND (winuser. h)
description: Une fenêtre reçoit ce message lorsque l’utilisateur choisit une commande dans le menu fenêtre (anciennement appelé système ou menu contrôle) ou lorsque l’utilisateur choisit le bouton Agrandir, le bouton réduire, le bouton restaurer ou le bouton Fermer.
ms.assetid: 82c7cc95-82d5-4f0f-8c78-ab325561b04e
keywords:
- WM_SYSCOMMAND des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_SYSCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 5458a9acfa6c166764b47a2d49a5ddcc181e38ee
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482175"
---
# <a name="wm_syscommand-message"></a>\_Message WM SYSCOMMAND

Une fenêtre reçoit ce message lorsque l’utilisateur choisit une commande dans le menu **fenêtre** (anciennement appelé système ou menu contrôle) ou lorsque l’utilisateur choisit le bouton Agrandir, le bouton réduire, le bouton restaurer ou le bouton Fermer.


```C++
#define WM_SYSCOMMAND                   0x0112
```

## <a name="example"></a>Exemple

```cpp
 case WM_SYSCOMMAND:
        if (wParam == SC_CLOSE)
        {
            EndDialog (hDlg, TRUE);
            return(TRUE);
        }
        break;

```
exemple de [Windows exemples classiques](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) sur GitHub.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Type de commande système demandée. Ce paramètre peut prendre les valeurs suivantes.




| Valeur | Signification | 
|-------|---------|
| <span id="SC_CLOSE"></span><span id="sc_close"></span><dl><dt><strong>SC_CLOSE</strong></dt><dt>0xF060</dt></dl> | Ferme la fenêtre.<br /> | 
| <span id="SC_CONTEXTHELP"></span><span id="sc_contexthelp"></span><dl><dt><strong>SC_CONTEXTHELP</strong></dt><dt>0xF180</dt></dl> | Remplace le curseur par un point d’interrogation par un pointeur. Si l’utilisateur clique ensuite sur un contrôle dans la boîte de dialogue, le contrôle reçoit un message de <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> .<br /> | 
| <span id="SC_DEFAULT"></span><span id="sc_default"></span><dl><dt><strong>SC_DEFAULT</strong></dt><dt>0xF160</dt></dl> | Sélectionne l’élément par défaut ; l’utilisateur a double-cliqué dans le menu fenêtre.<br /> | 
| <span id="SC_HOTKEY"></span><span id="sc_hotkey"></span><dl><dt><strong>SC_HOTKEY</strong></dt><dt>0xF150</dt></dl> | Active la fenêtre associée à la touche d’accès rapide spécifiée par l’application. Le paramètre <em>lParam</em> identifie la fenêtre à activer.<br /> | 
| <span id="SC_HSCROLL"></span><span id="sc_hscroll"></span><dl><dt><strong>SC_HSCROLL</strong></dt><dt>0xF080</dt></dl> | Fait défiler horizontalement.<br /> | 
| <span id="SCF_ISSECURE"></span><span id="scf_issecure"></span><dl><dt><strong>SCF_ISSECURE</strong></dt><dt>0x00000001</dt></dl> | Indique si l’économiseur d’écran est sécurisé. <br /> | 
| <span id="SC_KEYMENU"></span><span id="sc_keymenu"></span><dl><dt><strong>SC_KEYMENU</strong></dt><dt>0xF100</dt></dl> | Récupère le menu fenêtre à la suite d’une séquence de touches. Pour plus d'informations, consultez la section Notes.<br /> | 
| <span id="SC_MAXIMIZE"></span><span id="sc_maximize"></span><dl><dt><strong>SC_MAXIMIZE</strong></dt><dt>0xF030</dt></dl> | Agrandit la fenêtre.<br /> | 
| <span id="SC_MINIMIZE"></span><span id="sc_minimize"></span><dl><dt><strong>SC_MINIMIZE</strong></dt><dt>0xF020</dt></dl> | Réduit la fenêtre.<br /> | 
| <span id="SC_MONITORPOWER"></span><span id="sc_monitorpower"></span><dl><dt><strong>SC_MONITORPOWER</strong></dt><dt>0xF170</dt></dl> | Définit l’état de l’affichage. Cette commande prend en charge les appareils qui ont des fonctionnalités d’économie d’énergie, comme un ordinateur personnel alimenté par batterie. <br /> Le paramètre <em>lParam</em> peut avoir les valeurs suivantes :<br /><ul><li>-1 (l’affichage est sous tension)</li><li>1 (l’affichage est faible puissance)</li><li>2 (l’affichage est en cours d’arrêt)</li></ul> | 
| <span id="SC_MOUSEMENU"></span><span id="sc_mousemenu"></span><dl><dt><strong>SC_MOUSEMENU</strong></dt><dt>0xF090</dt></dl> | Récupère le menu fenêtre à la suite d’un clic de souris.<br /> | 
| <span id="SC_MOVE"></span><span id="sc_move"></span><dl><dt><strong>SC_MOVE</strong></dt><dt>0xF010</dt></dl> | Déplace la fenêtre.<br /> | 
| <span id="SC_NEXTWINDOW"></span><span id="sc_nextwindow"></span><dl><dt><strong>SC_NEXTWINDOW</strong></dt><dt>0xF040</dt></dl> | Passe à la fenêtre suivante.<br /> | 
| <span id="SC_PREVWINDOW"></span><span id="sc_prevwindow"></span><dl><dt><strong>SC_PREVWINDOW</strong></dt><dt>0xF050</dt></dl> | Passe à la fenêtre précédente.<br /> | 
| <span id="SC_RESTORE"></span><span id="sc_restore"></span><dl><dt><strong>SC_RESTORE</strong></dt><dt>0xF120</dt></dl> | Rétablit la position et la taille normales de la fenêtre.<br /> | 
| <span id="SC_SCREENSAVE"></span><span id="sc_screensave"></span><dl><dt><strong>SC_SCREENSAVE</strong></dt><dt>0xF140</dt></dl> | Exécute l’application d’écran de veille spécifiée dans la section [boot] du fichier System.ini.<br /> | 
| <span id="SC_SIZE"></span><span id="sc_size"></span><dl><dt><strong>SC_SIZE</strong></dt><dt>0xF000</dt></dl> | Dimensionne la fenêtre.<br /> | 
| <span id="SC_TASKLIST"></span><span id="sc_tasklist"></span><dl><dt><strong>SC_TASKLIST</strong></dt><dt>0xF130</dt></dl> | Active le menu <strong>Démarrer</strong> .<br /> | 
| <span id="SC_VSCROLL"></span><span id="sc_vscroll"></span><dl><dt><strong>SC_VSCROLL</strong></dt><dt>0xF070</dt></dl> | Fait défiler verticalement.<br /> | 




 

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible spécifie la position horizontale du curseur, en coordonnées d’écran, si une commande de menu fenêtre est sélectionnée avec la souris. Dans le cas contraire, ce paramètre n’est pas utilisé.

Le mot de poids fort spécifie la position verticale du curseur, en coordonnées d’écran, si une commande de menu fenêtre est sélectionnée avec la souris. Ce paramètre a la valeur 1 si la commande est choisie à l’aide d’un accélérateur système, ou zéro si vous utilisez un mnémonique.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Une application doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Remarques

Pour obtenir les coordonnées de position en coordonnées d’écran, utilisez le code suivant :


```
xPos = GET_X_LPARAM(lParam);    // horizontal position 
yPos = GET_Y_LPARAM(lParam);    // vertical position
```



La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) exécute la demande du menu fenêtre pour les actions prédéfinies spécifiées dans le tableau précédent.

Dans les messages **WM \_ SYSCOMMAND** , les quatre bits de poids faible du paramètre *wParam* sont utilisés en interne par le système. Pour obtenir le résultat correct lors du test de la valeur de *wParam*, une application doit combiner la valeur 0xFFF0 avec la valeur *wParam* à l’aide de l’opérateur de bits and.

Les éléments de menu d’un menu fenêtre peuvent être modifiés à l’aide des fonctions [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)et [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) . Les applications qui modifient le menu fenêtre doivent traiter les messages **WM \_ SYSCOMMAND** .

Une application peut exécuter n’importe quelle commande système à tout moment en transmettant un message **WM \_ SYSCOMMAND** à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Tous les messages **WM \_ SYSCOMMAND** non gérés par l’application doivent être passés à **DefWindowProc**. Toutes les valeurs de commande ajoutées par une application doivent être traitées par l’application et ne peuvent pas être passées à **DefWindowProc**.

Si la protection par mot de passe est activée par la stratégie, l’économiseur d’écran est démarré indépendamment de ce qu’une application utilise avec la notification **SC \_ SCREENSAVE** même si ne parvient pas à la passer à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Les touches d’accès rapide définies pour choisir des éléments dans le menu fenêtre sont traduites en messages **WM \_ SYSCOMMAND** ; toutes les autres séquences de touches d’accélérateur sont traduites en messages de [**\_ commande WM**](wm-command.md) .

Si le *wParam* est **le \_ keymenu SC**, *lParam* contient le code de caractère de la clé utilisée avec la touche Alt pour afficher le menu contextuel. Par exemple, si vous appuyez sur ALT + F pour afficher la fenêtre contextuelle du fichier, un **\_ SYSCOMMAND WM** avec *wParam* égal à **SC \_ keymenu** et *lParam* est égal à’F'.

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

[**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Obtient \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**Obtient \_ le \_ lParam Y**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
</dt> <dt>

[**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
</dt> <dt>

[**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
</dt> <dt>

[**WM, \_ commande**](wm-command.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Raccourcis clavier](keyboard-accelerators.md)
</dt> </dl>

