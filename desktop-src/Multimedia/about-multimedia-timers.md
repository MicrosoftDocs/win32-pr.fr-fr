---
title: À propos des minuteurs multimédias
description: À propos des minuteurs multimédias
ms.assetid: 42101923-3f46-4234-bfcf-a0d06c382fa1
keywords:
- Multimédia Windows, minuteurs
- multimédia, minuteries
- entrée multimédia, minuteries
- minuteries multimédias, à propos de
- minuteries, à propos de
- minuteries multimédias, planification des événements
- minuteries, événements de planification
- planification des événements de minuterie
- synchronisation haute résolution
- SetTimer fonction)
- CreateWaitableTimer fonction)
- Messages WM_TIMER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c36e5f19a92b6b47a3b1976bd85aadef88ab3ec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031177"
---
# <a name="about-multimedia-timers"></a>À propos des minuteurs multimédias

Les services de minuteur multimédia permettent aux applications de planifier des événements de minuterie avec la meilleure résolution (ou précision) possible pour la plateforme matérielle. Ces services de minuteur multimédia vous permettent de planifier des événements de minuterie à une résolution supérieure à celle des autres services du minuteur.

Ces services de minuteur sont utiles pour les applications qui exigent un minutage haute résolution. Par exemple, un séquenceur MIDI requiert un minuteur haute résolution, car il doit maintenir le rythme des événements MIDI dans une résolution de 1 milliseconde.

Les applications qui n’utilisent pas le minutage haute résolution doivent utiliser la fonction [SetTimer](/windows/win32/api/winuser/nf-winuser-settimer) à la place des services de minuteur multimédia. Les services du minuteur fournis par **SetTimer** publient les messages [ \_ du minuteur WM](../winmsg/wm-timer.md) dans une file d’attente de messages, tandis que les services du minuteur multimédia appellent une fonction de rappel. Les applications qui veulent qu’un minuteur peut utiliser la fonction [CreateWaitableTimer](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) .

 

 