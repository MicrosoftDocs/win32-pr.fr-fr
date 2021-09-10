---
title: Informations de minutage
description: Informations de minutage
ms.assetid: ff9d6fb2-1387-49ce-a4de-1b2f67353628
keywords:
- MIDI (Musical Instrument Digital Interface), informations de minutage
- MIDI (Musical Instrument Digital Interface), informations de minutage
- mémoires tampons de flux, informations de minutage
- MIDIEVENT, structure
- mémoires tampons de flux, format SMPTE
- mémoires tampons de flux, heure de la note du trimestre
- mémoires tampons de flux, cycles
- Format SMPTE
- heure de la note du trimestre
- ticks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2daf5b1847456e8fb518665521e484118fead79
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364527"
---
# <a name="timing-information"></a>Informations de minutage

Les informations de minutage pour un événement MIDI sont stockées dans le membre **dwDeltaTime** de la structure [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) . L’heure est indiquée en graduations, comme défini dans la spécification *1,0 des fichiers MIDI standard* . La longueur d’un battement est définie par le format d’heure et éventuellement par le tempo associé au flux. Pour plus d’informations sur les flux, consultez [MIDI flux](midi-streams.md).

Une graduation est exprimée en microsecondes par trimestre ou en tant que battements de temps de l’information SMPTE (société de motion et ingénieurs de la télévision). Les applications qui envoient des messages MIDI individuellement ou utilisent des messages MIDI non traités utilisent l’heure de la note trimestrielle et les informations sur le tempo pour déterminer la durée d’un cycle. Les applications qui prétraitent les messages MIDI peuvent stocker le temps écoulé en tant que nombre d’unités SMPTE utilisées.

L’heure de la note du trimestre est indiquée par un zéro dans le bit de mot haute (bit 15) du mot de la Division horaire. Le reste du mot contient la note des graduations par trimestre. Un tempo associé à un flux de données MIDI est conservé en unités (microsecondes par trimestre) conformément à la spécification des *fichiers midi Standard 1,0* . Par exemple, une note d’un quart de l’heure 4/4 qui utilise une note tempo de 500 000 microsecondes par trimestre est lue au taux de 120 temps par minute.

Les formats de la Division de temps SMPTE spécifient entièrement la longueur d’un battement sans avoir besoin d’informations sur le tempo. Dans à l’aide des formats d’heure SMPTE, les séquences MIDI peuvent être synchronisées avec d’autres événements SMPTE, tels que des vidéos ou des données audio entrelacées. L’heure SMPTE est indiquée par un 1 dans le bit de poids fort (bit 15) du mot de la Division temporelle. Le reste de l’octet le plus significatif spécifie le format SMPTE utilisé comme valeurs négatives. Les formats SMPTE pris en charge et leurs valeurs correspondantes (entre parenthèses) sont 24 (-24), 25 (-25), 30 (-30) et 30 Drop (-29). L’octet de poids faible du mot de la Division horaire spécifie le nombre de graduations par cadre SMPTE.

 

 