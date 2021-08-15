---
UID: ''
title: JournalPlaybackProc fonction de rappel
description: Lit une série de messages de souris et de clavier enregistrés précédemment.
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
ms.openlocfilehash: bee538bf2c20cc3cadb6f0bdf6f5dd6a2ae12dfe8a21baeb56b8ad62cb23ff3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437126"
---
# <a name="journalplaybackproc-function"></a>JournalPlaybackProc fonction)

## <a name="description"></a>Description

Fonction de rappel définie par l’application ou définie par la Bibliothèque utilisée avec la fonction [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
En règle générale, une application utilise cette fonction pour lire une série de messages de souris et de clavier enregistrés précédemment par la procédure de hook **JournalRecordProc** .
Tant qu’une procédure de hook **JournalPlaybackProc** est installée, l’entrée de souris et de clavier normale est désactivée.

Le type **HOOKPROC** définit un pointeur vers cette fonction de rappel.
**JournalPlaybackProc** est un espace réservé pour le nom de la fonction définie par l’application ou par la bibliothèque.

```cpp
LRESULT CALLBACK JournalPlaybackProc(
  _In_ int    code,
       WPARAM wParam,
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
| **HC_GETNEXT** 1 | La procédure de raccordement doit copier le message de la souris ou du clavier actuel dans la structure [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) vers laquelle pointe le paramètre *lParam* . |
| **HC_NOREMOVE** 3 | Une application a appelé la fonction [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) avec wRemoveMsg défini sur **PM_NOREMOVE**, ce qui indique que le message n’est pas supprimé de la file d’attente de messages après le traitement **PeekMessage** . |
| **HC_NOREMOVE** 2 | La procédure de raccordement doit préparer la copie du message suivant de la souris ou du clavier vers la structure **EVENTMSG** pointée par *lParam*. Lors de la réception du code **HC_GETNEXT** , la procédure de raccordement doit copier le message dans la structure. |
| **HC_SYSMODALOFF** 5 | Une boîte de dialogue modale du système a été détruite. La procédure de raccordement doit reprendre la réécriture des messages. |
| **HC_SYSMODALON** 4 | Une boîte de dialogue modale du système s’affiche. Jusqu’à ce que la boîte de dialogue soit détruite, la procédure de raccordement doit cesser de lire les messages. |

### <a name="wparam"></a>wParam

Type : **wParam**

Ce paramètre n'est pas utilisé.

### <a name="lparam"></a>lParam

Type : **lParam**

Pointeur vers une structure **EVENTMSG** qui représente un message en cours de traitement par la procédure de raccordement.
Ce paramètre est valide uniquement lorsque le paramètre de *code* est **HC_GETNEXT**.

## <a name="returns"></a>Retours

Type : **LRESULT**

Pour que le système attende avant de traiter le message, la valeur de retour doit correspondre à la durée, en battements d’horloge, que le système doit attendre.

(Cette valeur peut être calculée en calculant la différence entre les membres de temps dans les messages d’entrée actuels et précédents.)

Pour traiter le message immédiatement, la valeur de retour doit être égale à zéro. La valeur de retour est utilisée uniquement si le code de raccordement est **HC_GETNEXT**; Sinon, il est ignoré.

## <a name="remarks"></a>Remarques

Une procédure de hook **JournalPlaybackProc** doit copier un message d’entrée vers le paramètre *lParam* .
Le message doit avoir été enregistré précédemment à l’aide d’une procédure de hook **JournalRecordProc** , qui ne doit pas modifier le message.

Pour récupérer le même message à la fois, la procédure de raccordement peut être appelée plusieurs fois avec le paramètre de *code* défini sur **HC_GETNEXT** sans appel intermédiaire avec le *code* défini sur **HC_SKIP**.

Si le *code* est **HC_GETNEXT** et que la valeur de retour est supérieure à zéro, le système se met en veille pendant le nombre de millisecondes spécifié par la valeur de retour. Lorsque le système continue, il appelle à nouveau la procédure de raccordement avec le *code* défini sur **HC_GETNEXT** pour récupérer le même message.
La valeur de retour de ce nouvel appel à **JournalPlaybackProc** doit être égale à zéro ; dans le cas contraire, le système revient en mode veille pendant le nombre de millisecondes spécifié par la valeur de retour, appelle à nouveau **JournalPlaybackProc** , et ainsi de suite.
Le système semble ne pas répondre.

Contrairement à la plupart des autres procédures de raccordement globales, les procédures de hook **JournalRecordProc** et **JournalPlaybackProc** sont toujours appelées dans le contexte du thread qui définit le hook.

Une fois que la procédure de Hook a retourné le contrôle au système, le message continue à être traité. Si le *code* est **HC_SKIP**, la procédure de raccordement doit se préparer à retourner le prochain message d’événement enregistré lors de l’appel suivant.

Installez la procédure de hook **JournalPlaybackProc** en spécifiant le type de [WH_JOURNALPLAYBACK](about-hooks.md) et un pointeur vers la procédure de Hook dans un appel à la fonction **SetWindowsHookEx** .

Si l’utilisateur appuie sur CTRL + ECHAP ou CTRL + ALT + SUPPR pendant la lecture du journal, le système arrête la lecture, décroche la procédure de lecture du journal et envoie un message d' [WM_CANCELJOURNAL](wm-canceljournal.md) à l’application de journalisation.

Si la procédure de raccordement retourne un message dans la plage **WM_KEYFIRST** à **WM_KEYLAST**, les conditions suivantes s’appliquent :

* Le membre **param** de la structure **EVENTMSG** spécifie le code de la touche virtuelle de la touche qui a été enfoncée.
* Le membre **paramH** de la structure **EVENTMSG** spécifie le code d’analyse.
* Il n’existe aucun moyen de spécifier un nombre de répétitions.
L’événement est toujours pris pour représenter un événement clé.

## <a name="see-also"></a>Voir aussi

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[JournalRecordProc](journalrecordproc.md)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_CANCELJOURNAL](wm-canceljournal.md)

[Hooks](hooks.md)
