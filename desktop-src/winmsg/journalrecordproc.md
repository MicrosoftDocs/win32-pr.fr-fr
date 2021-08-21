---
UID: ''
title: JournalRecordProc fonction de rappel
description: La fonction enregistre les messages que le système supprime de la file d’attente des messages système.
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
ms.openlocfilehash: cc5e1bdbd99b234b347d0b9c10caa7125aead9b68138472e125c8e2a11180609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437116"
---
# <a name="journalrecordproc-function"></a>JournalRecordProc fonction)

## <a name="description"></a>Description

Fonction de rappel définie par l’application ou définie par la Bibliothèque utilisée avec la fonction [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
La fonction enregistre les messages que le système supprime de la file d’attente des messages système.
Plus tard, une application peut utiliser une procédure de hook [JournalPlaybackProc](journalplaybackproc.md) pour lire les messages.

Le type **HOOKPROC** définit un pointeur vers cette fonction de rappel.
**JournalRecordProc** est un espace réservé pour le nom de la fonction définie par l’application ou par la bibliothèque.

```cpp
LRESULT CALLBACK JournalRecordProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Paramètres

### <a name="code-in"></a>Code [in]

Type : **int**

Spécifie comment traiter le message.
Si le *code* est inférieur à zéro, la procédure de raccordement doit passer le message à la fonction [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sans traitement supplémentaire et doit retourner la valeur retournée par **CallNextHookEx**.
Ce paramètre peut prendre les valeurs suivantes.

| Valeur | Signification |
|-------|---------|
| **HC_ACTION** 0 | Le paramètre *lParam* est un pointeur vers une structure [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) contenant des informations sur un message supprimé de la file d’attente système. La procédure de raccordement doit enregistrer le contenu de la structure en les copiant dans un fichier ou une mémoire tampon. |
| **HC_SYSMODALOFF** 5 | Une boîte de dialogue modale du système a été détruite. La procédure de raccordement doit reprendre l’enregistrement. |
| **HC_SYSMODALON** 4 | Une boîte de dialogue modale du système s’affiche. Jusqu’à ce que la boîte de dialogue soit détruite, la procédure de raccordement doit arrêter l’enregistrement. |

### <a name="wparam"></a>wParam

Type : **wParam**

Ce paramètre n'est pas utilisé.

### <a name="lparam-in"></a>lParam [in]

Type : **lParam**

Pointeur vers une structure **EVENTMSG** qui contient le message à enregistrer.

## <a name="returns"></a>Retours

Type : **LRESULT**

La valeur de retour est ignorée.

## <a name="remarks"></a>Remarques

Une procédure de hook **JournalRecordProc** doit copier mais ne pas modifier les messages.
Une fois que la procédure de Hook a retourné le contrôle au système, le message continue à être traité.

Installez la procédure de hook **JournalRecordProc** en spécifiant le type de [WH_JOURNALRECORD](about-hooks.md) et un pointeur vers la procédure de Hook dans un appel à la fonction **SetWindowsHookEx** .

Une procédure de hook **JournalRecordProc** n’a pas besoin de résider dans une bibliothèque de liens dynamiques.
Une procédure de hook **JournalRecordProc** peut résider dans l’application elle-même.

Contrairement à la plupart des autres procédures de raccordement globales, les procédures de hook **JournalRecordProc** et [JournalPlaybackProc](journalplaybackproc.md) sont toujours appelées dans le contexte du thread qui définit le hook.

Une application qui a installé une procédure de hook **JournalRecordProc** doit surveiller la [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) code de clé virtuelle (qui est implémenté en tant que combinaison de touches CTRL + ATTN sur la plupart des claviers).
Ce code de clé virtuelle doit être interprété par l’application comme un signal indiquant que l’utilisateur souhaite arrêter l’enregistrement du journal.
L’application doit répondre en mettant fin à la séquence d’enregistrement et en supprimant la procédure de hook **JournalRecordProc** .
La suppression est importante.
Il empêche une application de journalisation de verrouiller le système en raccrochant à l’intérieur d’une procédure de raccordement.

Ce rôle en tant que signal d’arrêt de l’enregistrement journl signifie qu’une combinaison de touches CTRL + ATTN ne peut pas être enregistrée.
Étant donné que la combinaison de touches CTRL + C n’a pas de rôle comme un signal de journalisation, elle peut être enregistrée.
Il existe deux autres combinaisons de touches qui ne peuvent pas être enregistrées : CTRL + ECHAP et CTRL + ALT + SUPPR.
Ces deux combinaisons de touches entraînent l’arrêt de toutes les activités de journalisation (enregistrement ou lecture) par le système, la suppression de tous les hooks de journalisation et la publication d’un message de [WM_CANCELJOURNAL](wm-canceljournal.md) dans l’application de journalisation.

## <a name="see-also"></a>Voir aussi

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[JournalPlaybackProc](journalplaybackproc.md)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_CANCELJOURNAL](wm-canceljournal.md)

[Hooks](hooks.md)
