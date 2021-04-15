---
title: Utilisation de midiOutShortMsg pour envoyer des messages MIDI individuels
description: Utilisation de midiOutShortMsg pour envoyer des messages MIDI individuels
ms.assetid: 7a8f7c6c-28ac-4aa6-9073-969fc8e59f4e
keywords:
- MIDI (Musical Instrument Digital Interface), envoi de messages
- MIDI (Musical Instrument Digital Interface), envoi de messages
- envoi de messages MIDI
- Interface MIDI (Musical Instrument Digital Interface), fonction midiOutShortMsg
- MIDI (Musical Instrument Digital Interface), fonction midiOutShortMsg
- midiOutShortMsg fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905b0ce924f9aebce67f515fc0714fdc855cbe33
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463074"
---
# <a name="using-midioutshortmsg-to-send-individual-midi-messages"></a>Utilisation de midiOutShortMsg pour envoyer des messages MIDI individuels

L’exemple suivant utilise la fonction [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) pour envoyer un événement midi spécifié à un appareil de sortie MIDI donné :


```C++
UINT sendMIDIEvent(HMIDIOUT hmo, BYTE bStatus, BYTE bData1, 
    BYTE bData2) 
{ 
    union { 
        DWORD dwData; 
        BYTE bData[4]; 
    } u; 
 
    // Construct the MIDI message. 
 
    u.bData[0] = bStatus;  // MIDI status byte 
    u.bData[1] = bData1;   // first MIDI data byte 
    u.bData[2] = bData2;   // second MIDI data byte 
    u.bData[3] = 0; 
 
    // Send the message. 
    return midiOutShortMsg(hmo, u.dwData); 
} 
```



> [!Note]  
> Les pilotes de sortie MIDI ne sont pas requis pour vérifier les données avant de les envoyer vers un port de sortie. Les applications doivent s’assurer que seules les données valides sont envoyées.

 

 

 