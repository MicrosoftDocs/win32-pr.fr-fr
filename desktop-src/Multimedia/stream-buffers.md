---
title: Mémoires tampons de flux
description: Mémoires tampons de flux
ms.assetid: d73209a3-4b9d-4405-9e62-8ecfb94c0bd5
keywords:
- Windows multimédia, mémoires tampons de flux
- multimédia, mémoires tampons de flux
- audio multimédia, mémoires tampons de flux
- audio, mémoires tampons de flux
- MIDI (Musical Instrument Digital Interface), mémoires tampons de flux
- MIDI (Musical Instrument Digital Interface), mémoires tampons de flux
- mémoires tampons de flux, à propos de
- MIDIHDR, structure
- MIDIEVENT, structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a01862a8a8e6b7846cbe445737bd13422cf0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229937"
---
# <a name="stream-buffers"></a>Mémoires tampons de flux

Les applications peuvent utiliser des mémoires tampons de flux pour envoyer des flux d’événements MIDI à un appareil. Chaque mémoire tampon de flux est un bloc de mémoire vers lequel pointe une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) . Ce bloc de mémoire contient des données pour un ou plusieurs événements MIDI, chacun d’eux étant défini par une structure [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) . Une application contrôle la mémoire tampon en appelant les fonctions de manipulation de flux, telles que [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen), [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)et [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose).

-   [Format de mémoire tampon de flux](stream-buffer-format.md)
-   [Informations de minutage](timing-information.md)
-   [Types d’événements MIDI](midi-event-types.md)
-   [Flux MIDI](midi-streams.md)

 

 