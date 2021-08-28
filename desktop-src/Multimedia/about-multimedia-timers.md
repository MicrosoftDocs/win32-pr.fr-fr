---
title: À propos des minuteurs multimédias
description: À propos des minuteurs multimédias
ms.assetid: 42101923-3f46-4234-bfcf-a0d06c382fa1
keywords:
- Windows multimédia, minuteries
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
ms.openlocfilehash: 99b5d899c93f0f292d7ef45e8584ae9e2b5e0e001037c456dcc4900f1c0d3f26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498209"
---
# <a name="about-multimedia-timers"></a>À propos des minuteurs multimédias

Les services de minuteur multimédia permettent aux applications de planifier des événements de minuterie avec la meilleure résolution (ou précision) possible pour la plateforme matérielle. Ces services de minuteur multimédia vous permettent de planifier des événements de minuterie à une résolution supérieure à celle des autres services du minuteur.

Ces services de minuteur sont utiles pour les applications qui exigent un minutage haute résolution. Par exemple, un séquenceur MIDI requiert un minuteur haute résolution, car il doit maintenir le rythme des événements MIDI dans une résolution de 1 milliseconde.

Les applications qui n’utilisent pas le minutage haute résolution doivent utiliser la fonction [SetTimer](/windows/win32/api/winuser/nf-winuser-settimer) à la place des services de minuteur multimédia. Les services du minuteur fournis par **SetTimer** publient les messages [ \_ du minuteur WM](../winmsg/wm-timer.md) dans une file d’attente de messages, tandis que les services du minuteur multimédia appellent une fonction de rappel. Les applications qui veulent qu’un minuteur peut utiliser la fonction [CreateWaitableTimer](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) .

 

 