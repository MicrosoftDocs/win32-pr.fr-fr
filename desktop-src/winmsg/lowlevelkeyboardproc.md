---
UID: ''
title: LowLevelKeyboardProc fonction de rappel
description: Le système appelle cette fonction chaque fois qu’un nouvel événement d’entrée au clavier est sur le point d’être publié dans une file d’attente d’entrée de thread.
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
ms.openlocfilehash: 5a9a2a0cb5ccf60fe5cfc9f495b621669ba1d85ca04eeb7ecd345cdc60d48bc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548569"
---
# <a name="lowlevelkeyboardproc-function"></a>LowLevelKeyboardProc fonction)

## <a name="description"></a>Description

Fonction de rappel définie par l’application ou définie par la Bibliothèque utilisée avec la fonction [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
Le système appelle cette fonction chaque fois qu’un nouvel événement d’entrée au clavier est sur le point d’être publié dans une file d’attente d’entrée de thread.

**Remarque :**  Lorsque cette fonction de rappel est appelée en réponse à une modification de l’état d’une clé, la fonction de rappel est appelée avant que l’état asynchrone de la clé ne soit mis à jour.
Par conséquent, l’état asynchrone de la clé ne peut pas être déterminé en appelant [GetAsyncKeyState](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) à partir de la fonction de rappel.

Le type **HOOKPROC** définit un pointeur vers cette fonction de rappel.
**LowLevelKeyboardProc** est un espace réservé pour le nom de la fonction définie par l’application ou par la bibliothèque.

```cpp
LRESULT CALLBACK LowLevelKeyboardProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Paramètres

### <a name="code-in"></a>Code [in]

Type : **int**

Code que la procédure de raccordement utilise pour déterminer comment traiter le message.
Si *nCode* est inférieur à zéro, la procédure de raccordement doit passer le message à la fonction [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sans traitement supplémentaire et doit retourner la valeur retournée par **CallNextHookEx**.
Ce paramètre peut prendre les valeurs suivantes.

| Valeur | Signification |
|-------|---------|
| **HC_ACTION** 0 | Les paramètres *wParam* et *lParam* contiennent des informations sur un message de clavier. |

### <a name="wparam-in"></a>wParam [in]

Type : **wParam**

Identificateur du message du clavier.
Ce paramètre peut être l’un des messages suivants : [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown), [WM_KEYUP](/windows/desktop/inputdev/wm-keyup), [WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown)ou [WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup).

### <a name="lparam-in"></a>lParam [in]

Type : **lParam**

Pointeur vers une structure [KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct) .

## <a name="returns"></a>Retours

Type : **LRESULT**

Si *nCode* est inférieur à zéro, la procédure de raccordement doit retourner la valeur retournée par **CallNextHookEx**.

Si *nCode* est supérieur ou égal à zéro et que la procédure de hook n’a pas traité le message, il est vivement recommandé d’appeler **CallNextHookEx** et de retourner la valeur qu’il retourne ; dans le cas contraire, les autres applications qui ont installé [WH_KEYBOARD_LL](about-hooks.md) hooks ne recevront pas de notifications de raccordement et pourront se comporter de manière incorrecte.
Si la procédure de Hook a traité le message, elle peut retourner une valeur différente de zéro pour empêcher le système de transmettre le message au reste de la chaîne de raccordement ou à la procédure de fenêtre cible.

## <a name="remarks"></a>Remarques

Une application installe la procédure de raccordement en spécifiant le type de hook **WH_KEYBOARD_LL** et un pointeur vers la procédure de Hook dans un appel à la fonction **SetWindowsHookEx** .

Ce hook est appelé dans le contexte du thread qui l’a installé.
L’appel est effectué en envoyant un message au thread qui a installé le hook.
Par conséquent, le thread qui a installé le hook doit avoir une boucle de message.

L’entrée au clavier peut provenir du pilote de clavier local ou d’appels à la fonction [keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event) .
Si l’entrée provient d’un appel à **keybd_event**, l’entrée était « injectée ».
Toutefois, le hook WH_KEYBOARD_LL n’est pas injecté dans un autre processus.
Au lieu de cela, le contexte revient au processus qui a installé le hook et il est appelé dans son contexte d’origine.
Ensuite, le contexte revient à l’application qui a généré l’événement.

La procédure de raccordement doit traiter un message en moins de temps que l’entrée de données spécifiée dans la valeur **LowLevelHooksTimeout** de la clé de Registre suivante : **HKEY_CURRENT_USER\Control Panel\Desktop**.

Cette valeur est exprimée en millisecondes.
Si la procédure de raccordement expire, le système transmet le message au Hook suivant.
toutefois, sur Windows 7 et versions ultérieures, le hook est supprimé en mode silencieux sans être appelé.
L’application n’a aucun moyen de savoir si le hook est supprimé.

Remarque : les raccordements de débogage ne peuvent pas suivre ce type de hook de clavier de bas niveau.
Si l’application doit utiliser des raccordements de bas niveau, elle doit exécuter les raccordements sur un thread dédié qui transmet le travail à un thread de travail, puis retourne immédiatement.
Dans la plupart des cas où l’application doit utiliser des raccordements de bas niveau, elle doit surveiller l’entrée brute à la place.
Cela est dû au fait que l’entrée brute peut surveiller de façon asynchrone les messages de souris et de clavier ciblés pour d’autres threads plus efficacement que les raccordements de bas niveau.
Pour plus d’informations sur les entrées brutes, consultez [entrée brute](/windows/desktop/inputdev/raw-input).

## <a name="see-also"></a>Voir aussi

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)

[WM_KEYUP](/windows/desktop/inputdev/wm-keyup)

[WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown)

[WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup)

[Hooks](hooks.md)

[À propos des hooks](about-hooks.md)
