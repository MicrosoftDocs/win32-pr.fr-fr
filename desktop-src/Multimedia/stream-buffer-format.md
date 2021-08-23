---
title: Format de mémoire tampon de flux
description: Format de mémoire tampon de flux
ms.assetid: 4b24c12e-b43f-492e-a000-af4f59d5e16f
keywords:
- MIDI (Musical Instrument Digital Interface), mémoires tampons de flux
- MIDI (Musical Instrument Digital Interface), mémoires tampons de flux
- mémoires tampons de flux, format
- MIDIHDR, structure
- MIDIEVENT, structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072c2541ab6b731686fc63c59b11b0dfff529ef9cab347d41fbddf13e9b60b04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688499"
---
# <a name="stream-buffer-format"></a>Format de mémoire tampon de flux

Le membre **lpData** de la structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) pointe vers une mémoire tampon de flux, et le membre **dwBufferLength** spécifie la taille réelle de cette mémoire tampon. Le membre **dwBytesRecorded** de **MIDIHDR** spécifie le nombre d’octets dans la mémoire tampon qui sont réellement utilisés par les événements MIDI ; Cette valeur doit être inférieure ou égale à la valeur spécifiée par **dwBufferLength**.

Chacun des événements MIDI dans la mémoire tampon de flux est spécifié par une structure [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) , qui contient l’heure de l’événement, un identificateur de flux, un code d’événement et, le cas échéant, les paramètres de l’événement. Chacune de ces structures **MIDIEVENT** doit commencer sur une limite de mot double. Si nécessaire, les octets de remplissage doivent être ajoutés à la fin de la structure pour s’assurer que le suivant démarre sur une limite de mot double.

 

 