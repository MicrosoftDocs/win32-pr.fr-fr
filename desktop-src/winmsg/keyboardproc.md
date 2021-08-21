---
UID: ''
title: KeyboardProc fonction de rappel
description: Le système appelle cette fonction pour obtenir une fonction de message et un message clavier à traiter.
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
ms.openlocfilehash: ed2f3943667d09f42a7bc843adac69eaa4043454d93b409b193513b8ab43fd63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437154"
---
# <a name="keyboardproc-function"></a>KeyboardProc fonction)

## <a name="description"></a>Description

Fonction de rappel définie par l’application ou définie par la Bibliothèque utilisée avec la fonction [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
Le système appelle cette fonction chaque fois qu’une application appelle la fonction [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) et qu’un message de clavier ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) ou [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) doit être traité.

Le type **HOOKPROC** définit un pointeur vers cette fonction de rappel.
**KeyboardProc** est un espace réservé pour le nom de la fonction définie par l’application ou par la bibliothèque.

```cpp
LRESULT CALLBACK KeyboardProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Paramètres

### <a name="code-in"></a>Code [in]

Type : **int**

Code que la procédure de raccordement utilise pour déterminer comment traiter le message.
Si le *code* est inférieur à zéro, la procédure de raccordement doit passer le message à la fonction [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sans traitement supplémentaire et doit retourner la valeur retournée par **CallNextHookEx**.
Ce paramètre peut prendre les valeurs suivantes.

| Valeur | Signification |
|-------|---------|
| **HC_ACTION** 0 | Les paramètres *wParam* et *lParam* contiennent des informations sur un message de séquence de touches. |
| **HC_NOREMOVE** 3 | Les paramètres *wParam* et *lParam* contiennent des informations sur un message de frappe de touche et le message de frappe n’a pas été supprimé de la file d’attente de messages. (Une application appelée fonction **PeekMessage** , en spécifiant l’indicateur **PM_NOREMOVE** .) |

### <a name="wparam-in"></a>wParam [in]

Type : **wParam**

Code de la clé [virtuelle](/windows/desktop/inputdev/virtual-key-codes) de la clé qui a généré le message de frappe.

### <a name="lparam-in"></a>lParam [in]

Type : **lParam**

Le nombre de répétitions, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de clé précédent et l’indicateur d’état de transition.
Pour plus d’informations sur le paramètre *lParam* , consultez [indicateurs de message de frappe](/windows/desktop/inputdev/about-keyboard-input).
Le tableau suivant décrit les bits de cette valeur.

| Bits | Description |
|-------|---------|
| 0-15 | Nombre de répétitions. La valeur est le nombre de fois où la frappe est répétée à la suite de la touche de l’utilisateur. |
| 16-23 | Code d’analyse. La valeur dépend du fabricant d’ordinateurs OEM. |
| 24 | Indique si la touche est une touche étendue, telle qu’une touche de fonction ou une touche du pavé numérique. La valeur est 1 si la clé est une clé étendue ; Sinon, la valeur est 0. |
| 25-28 | Réservé. |
| 29 | Code de contexte. La valeur est 1 si la touche ALT est enfoncée ; Sinon, la valeur est 0. |
| 30 | État de la clé précédente. La valeur est 1 si la touche est enfoncée avant l’envoi du message ; la valeur est 0 si la touche est enfoncée. |
| 31 | État de transition. La valeur est 0 si la touche est enfoncée et 1 si elle est libérée. |

## <a name="returns"></a>Retours

Type : **LRESULT**

Si le *code* est inférieur à zéro, la procédure de raccordement doit retourner la valeur retournée par **CallNextHookEx**.

Si le *code* est supérieur ou égal à zéro et que la procédure de hook n’a pas traité le message, il est fortement recommandé d’appeler **CallNextHookEx** et de retourner la valeur qu’il retourne ; dans le cas contraire, les autres applications qui ont installé [WH_KEYBOARD](about-hooks.md) hooks ne recevront pas de notifications de raccordement et pourront se comporter de manière incorrecte.
Si la procédure de Hook a traité le message, elle peut retourner une valeur différente de zéro pour empêcher le système de transmettre le message au reste de la chaîne de raccordement ou à la procédure de fenêtre cible.

## <a name="remarks"></a>Remarques

Une application installe la procédure de raccordement en spécifiant le type de hook **WH_KEYBOARD** et un pointeur vers la procédure de Hook dans un appel à la fonction **SetWindowsHookEx** .

Ce hook peut être appelé dans le contexte du thread qui l’a installé.
L’appel est effectué en envoyant un message au thread qui a installé le hook.
Par conséquent, le thread qui a installé le hook doit avoir une boucle de message.

## <a name="see-also"></a>Voir aussi

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_KEYUP](/windows/desktop/inputdev/wm-keyup)

[WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)

[Hooks](hooks.md)
