---
UID: ''
title: MouseProc fonction de rappel
description: Le système appelle cette fonction lorsqu’une application appelle une fonction de message et qu’il y a un message de souris à traiter.
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
ms.openlocfilehash: abdd74b5fed93e2c2ddbc8d037a657b779a62a05
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/11/2020
ms.locfileid: "106512302"
---
# <a name="mouseproc-function"></a>MouseProc fonction)

## <a name="description"></a>Description

Fonction de rappel définie par l’application ou définie par la Bibliothèque utilisée avec la fonction [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
Le système appelle cette fonction chaque fois qu’une application appelle la fonction [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) et qu’un message de souris est traité.

Le type **HOOKPROC** définit un pointeur vers cette fonction de rappel.
**MouseProc** est un espace réservé pour le nom de la fonction définie par l’application ou par la bibliothèque.

```cpp
LRESULT CALLBACK MouseProc(
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
| **HC_NOREMOVE** 3 | Les paramètres *wParam* et *lParam* contiennent des informations sur un message de souris, et le message de la souris n’a pas été supprimé de la file d’attente de messages. (Une application appelée fonction **PeekMessage** , en spécifiant l’indicateur **PM_NOREMOVE** .) |

### <a name="wparam-in"></a>wParam [in]

Type : **wParam**

Identificateur du message de la souris.

### <a name="lparam-in"></a>lParam [in]

Type : **lParam**

Pointeur vers une structure [MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct) .

## <a name="returns"></a>Retours

Type : **LRESULT**

Si *nCode* est inférieur à zéro, la procédure de raccordement doit retourner la valeur retournée par **CallNextHookEx**.

Si *nCode* est supérieur ou égal à zéro et que la procédure de hook n’a pas traité le message, il est vivement recommandé d’appeler **CallNextHookEx** et de retourner la valeur qu’il retourne ; dans le cas contraire, les autres applications qui ont installé [WH_MOUSE](about-hooks.md) hooks ne recevront pas de notifications de raccordement et pourront se comporter de manière incorrecte.
Si la procédure de Hook a traité le message, elle peut retourner une valeur différente de zéro pour empêcher le système de transmettre le message à la procédure de fenêtre cible.

## <a name="remarks"></a>Notes

Une application installe la procédure de raccordement en spécifiant le type de hook WH_MOUSE et un pointeur vers la procédure de Hook dans un appel à la fonction **SetWindowsHookEx** .

La procédure de raccordement ne doit pas installer de [WH_JOURNALPLAYBACK](about-hooks.md) fonction de rappel.

Ce hook peut être appelé dans le contexte du thread qui l’a installé.
L’appel est effectué en envoyant un message au thread qui a installé le hook.
Par conséquent, le thread qui a installé le hook doit avoir une boucle de message.

## <a name="see-also"></a>Voir aussi

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Hooks](hooks.md)

[À propos des hooks](about-hooks.md)
