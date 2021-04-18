---
UID: ''
title: ShellProc fonction de rappel
description: La fonction reçoit des notifications d’événements de Shell du système.
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 4add84011745aeb61659c39775b94fed91028d83
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/11/2020
ms.locfileid: "106509432"
---
# <a name="shellproc-function"></a>ShellProc fonction)

## <a name="description"></a>Description

Fonction de rappel définie par l’application ou définie par la Bibliothèque utilisée avec la fonction [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
La fonction reçoit des notifications d’événements de Shell du système.

Le type **HOOKPROC** définit un pointeur vers cette fonction de rappel.
**ShellProc** est un espace réservé pour le nom de la fonction définie par l’application ou par la bibliothèque.

```cpp
LRESULT CALLBACK ShellProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Paramètres

### <a name="ncode-in"></a>nCode [in]

Type : **int**

Code de raccordement.
Si *nCode* est inférieur à zéro, la procédure de raccordement doit passer le message à la fonction [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sans traitement supplémentaire et doit retourner la valeur retournée par **CallNextHookEx**.
Ce paramètre peut prendre les valeurs suivantes.

| Valeur | Signification |
|-------|---------|
| **HSHELL_ACCESSIBILITYSTATE** 11 | L’état de l’accessibilité a changé. |
| **HSHELL_ACTIVATESHELLWINDOW** 3 | L’interpréteur de commandes doit activer sa fenêtre principale. |
| **HSHELL_APPCOMMAND** 12 | L’utilisateur a terminé un événement d’entrée (par exemple, j’ai appuyé sur un bouton de commande de l’application sur la souris ou sur une touche de commande de l’application sur le clavier) et l’application n’a pas géré le [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) message généré par cette entrée. Si la procédure Shell gère le message [WM_COMMAND](/windows/desktop/menurc/wm-command) , elle ne doit pas appeler **CallNextHookEx**. Pour plus d’informations, consultez la section valeur de retour. |
| **HSHELL_GETMINRECT** 5 | Une fenêtre est réduite ou agrandie. Le système a besoin des coordonnées du rectangle réduit pour la fenêtre. |
| **HSHELL_LANGUAGE** 8 | La langue du clavier a été modifiée ou une nouvelle disposition du clavier a été chargée. |
| **HSHELL_REDRAW** 6 | Le titre d’une fenêtre dans la barre des tâches a été redessiné. |
| **HSHELL_TASKMAN** 7 | L’utilisateur a sélectionné la liste des tâches. Une application d’environnement qui fournit une liste de tâches doit retourner la **valeur true** pour empêcher Windows de démarrer sa liste de tâches. |
| **HSHELL_WINDOWACTIVATED** 4 | L’activation a été remplacée par une nouvelle fenêtre de niveau supérieur, sans propriétaire. |
| **HSHELL_WINDOWCREATED** 1 | Une fenêtre de niveau supérieur sans propriétaire a été créée. La fenêtre existe lorsque le système appelle ce hook. |
| **HSHELL_WINDOWDESTROYED** 2 | Une fenêtre de niveau supérieur, sans propriétaire, va être détruite. La fenêtre existe toujours lorsque le système appelle ce hook. |
| **HSHELL_WINDOWREPLACED** 13 | Une fenêtre de niveau supérieur est remplacée. La fenêtre existe lorsque le système appelle ce hook. |

### <a name="wparam-in"></a>wParam [in]

Type : **wParam**

Ce paramètre dépend de la valeur du paramètre *nCode* , comme indiqué dans le tableau suivant.

| nCode | wParam |
|-------|---------|
| **HSHELL_ACCESSIBILITYSTATE** | Indique quelle fonctionnalité d’accessibilité a changé d’État. Cette valeur est l’une des suivantes : **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS** ou **ACCESS_STICKYKEYS**. |
| **HSHELL_APPCOMMAND** | Indique où le message de **WM_APPCOMMAND** a été envoyé à l’origine ; par exemple, le handle d’une fenêtre. Pour plus d’informations, consultez paramètre cmd dans **WM_APPCOMMAND**. |
| **HSHELL_GETMINRECT** | Handle vers la fenêtre réduite ou agrandie. |
| **HSHELL_LANGUAGE** | Handle de la fenêtre. |
| **HSHELL_REDRAW** | Handle de la fenêtre redessinée. |
| **HSHELL_WINDOWACTIVATED** | Handle de la fenêtre activée. |
| **HSHELL_WINDOWCREATED** | Handle de la fenêtre créée. |
| **HSHELL_WINDOWDESTROYED** | Handle vers la fenêtre détruite. |
| **HSHELL_WINDOWREPLACED** | Handle de la fenêtre qui est remplacée. Windows 2000 : non pris en charge. |

### <a name="lparam-in"></a>lParam [in]

Type : **lParam**

Ce paramètre dépend de la valeur du paramètre *nCode* , comme indiqué dans le tableau suivant.

| nCode | lParam |
|-------|---------|
| **HSHELL_APPCOMMAND** | `GET_APPCOMMAND_LPARAM(lParam)` commande d’application correspondant à l’événement d’entrée. `GET_DEVICE_LPARAM(lParam)` indique ce qui a généré l’événement d’entrée ; par exemple, la souris ou le clavier. Pour plus d’informations, consultez la description du paramètre *uDevice* sous **WM_APPCOMMAND**. `GET_FLAGS_LPARAM(lParam)` dépend de la valeur de *cmd* dans **WM_APPCOMMAND**. Par exemple, il peut indiquer quelles clés virtuelles ont été conservées lors de l’envoi de l' **WM_APPCOMMAND** message. Pour plus d’informations, consultez le paramètre de description *dwCmdFlags* sous **WM_APPCOMMAND**. |
| **HSHELL_GETMINRECT** | Pointeur vers une structure [Rect](/previous-versions/dd162897(v=vs.85)) . |
| **HSHELL_LANGUAGE** | Handle d’une disposition de clavier. |
| **HSHELL_MONITORCHANGED** | Handle vers la fenêtre qui a été déplacée vers un autre moniteur. |
| **HSHELL_REDRAW** | La valeur est **true** si la fenêtre clignote, ou **false** dans le cas contraire. |
| **HSHELL_WINDOWACTIVATED** | La valeur est TRUE si la fenêtre est en mode plein écran, ou **false** dans le cas contraire. |
| **HSHELL_WINDOWREPLACED** | Handle de la nouvelle fenêtre. Windows 2000 : non pris en charge. |

## <a name="returns"></a>Retours

Type : **LRESULT**

La valeur de retour doit être égale à zéro, sauf si la valeur de nCode est **HSHELL_APPCOMMAND** et que la procédure Shell gère le message **WM_COMMAND** .
Dans ce cas, le retour doit être différent de zéro.

## <a name="remarks"></a>Notes

Installez cette procédure de hook en spécifiant le type de hook [WH_SHELL](about-hooks.md) et un pointeur vers la procédure de Hook dans un appel à la fonction **SetWindowsHookEx** .

## <a name="see-also"></a>Voir aussi

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand)

[WM_COMMAND](/windows/desktop/menurc/wm-command)

[Hooks](hooks.md)
