---
UID: ''
title: LowLevelMouseProc fonction de rappel
description: Le système appelle cette fonction chaque fois qu’un nouvel événement d’entrée de la souris est sur le point d’être publié dans une file d’attente d’entrée de thread.
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
ms.openlocfilehash: df6f246e5824099d01ab2a42f887464c7177cfa5
ms.sourcegitcommit: 36610cefb8577d0cf9aa2286c8000d8f31cc4ec2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2020
ms.locfileid: "104032043"
---
# <a name="lowlevelmouseproc-function"></a>LowLevelMouseProc fonction)

## <a name="description"></a>Description

Fonction de rappel définie par l’application ou définie par la Bibliothèque utilisée avec la fonction [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
Le système appelle cette fonction chaque fois qu’un nouvel événement d’entrée de la souris est sur le point d’être publié dans une file d’attente d’entrée de thread.

Le type **HOOKPROC** définit un pointeur vers cette fonction de rappel.
**LowLevelMouseProc** est un espace réservé pour le nom de la fonction définie par l’application ou par la bibliothèque.

```cpp
LRESULT CALLBACK LowLevelMouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Paramètres

### <a name="ncode-in"></a>nCode [in]

Type : **int**

Code que la procédure de raccordement utilise pour déterminer comment traiter le message.
Si *nCode* est inférieur à zéro, la procédure de raccordement doit passer le message à la fonction [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sans traitement supplémentaire et doit retourner la valeur retournée par **CallNextHookEx**.
Ce paramètre peut prendre les valeurs suivantes.

| Valeur | Signification |
|-------|---------|
| **HC_ACTION** 0 | Les paramètres *wParam* et *lParam* contiennent des informations sur un message de souris. |

### <a name="wparam-in"></a>wParam [in]

Type : **wParam**

Identificateur du message de la souris.
Ce paramètre peut être l’un des messages suivants : [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) ou [WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).

### <a name="lparam-in"></a>lParam [in]

Type : **lParam**

Pointeur vers une structure [MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct) .

## <a name="returns"></a>Retours

Type : **LRESULT**

Si *nCode* est inférieur à zéro, la procédure de raccordement doit retourner la valeur retournée par **CallNextHookEx**.

Si *nCode* est supérieur ou égal à zéro et que la procédure de hook n’a pas traité le message, il est vivement recommandé d’appeler **CallNextHookEx** et de retourner la valeur qu’il retourne ; dans le cas contraire, les autres applications qui ont installé [WH_MOUSE_LL](about-hooks.md) hooks ne recevront pas de notifications de raccordement et pourront se comporter de manière incorrecte.
Si la procédure de Hook a traité le message, elle peut retourner une valeur différente de zéro pour empêcher le système de transmettre le message au reste de la chaîne de raccordement ou à la procédure de fenêtre cible.

## <a name="remarks"></a>Notes

Une application installe la procédure de raccordement en spécifiant le type de hook **WH_MOUSE_LL** et un pointeur vers la procédure de Hook dans un appel à la fonction **SetWindowsHookEx** .

Ce hook est appelé dans le contexte du thread qui l’a installé.
L’appel est effectué en envoyant un message au thread qui a installé le hook.
Par conséquent, le thread qui a installé le hook doit avoir une boucle de message.

L’entrée de la souris peut provenir du pilote de souris local ou d’appels à la fonction [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) .
Si l’entrée provient d’un appel à **mouse_event**, l’entrée était « injectée ».
Toutefois, le hook **WH_MOUSE_LL** n’est pas injecté dans un autre processus.
Au lieu de cela, le contexte revient au processus qui a installé le hook et il est appelé dans son contexte d’origine.
Ensuite, le contexte revient à l’application qui a généré l’événement.

La procédure de raccordement doit traiter un message en moins de temps que l’entrée de données spécifiée dans la valeur **LowLevelHooksTimeout** de la clé de Registre suivante : **HKEY_CURRENT_USER\Control Panel\Desktop**.

Cette valeur est exprimée en millisecondes.
Si la procédure de raccordement expire, le système transmet le message au Hook suivant.
Toutefois, sur Windows 7 et versions ultérieures, le hook est supprimé en mode silencieux sans être appelé.
L’application n’a aucun moyen de savoir si le hook est supprimé.

**Remarque :**  Les raccordements de débogage ne peuvent pas suivre ce type de crochets de souris de bas niveau.
Si l’application doit utiliser des raccordements de bas niveau, elle doit exécuter les raccordements sur un thread dédié qui transmet le travail à un thread de travail, puis retourne immédiatement.
Dans la plupart des cas où l’application doit utiliser des raccordements de bas niveau, elle doit surveiller l’entrée brute à la place.
Cela est dû au fait que l’entrée brute peut surveiller de façon asynchrone les messages de souris et de clavier ciblés pour d’autres threads plus efficacement que les raccordements de bas niveau.
Pour plus d’informations sur les entrées brutes, consultez [entrée brute](/windows/desktop/inputdev/raw-input).

## <a name="see-also"></a>Voir aussi

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event)

[KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown)

[WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup)

[WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove)

[WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel)

[WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown)

[WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup)

[Hooks](hooks.md)

[À propos des hooks](about-hooks.md)
