---
title: Instructions de création pour les fichiers MIDI
description: Instructions de création pour les fichiers MIDI
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- Instructions de création de fichiers MIDI (Musical Instrument Digital Interface)
- MIDI (Musical Instrument Digital Interface), instructions de création de fichiers
- création de fichiers MIDI, instructions de création de fichiers
- attributions de correctifs MIDI standard
- attributions de clés MIDI standard
- Interface MIDI (Musical Instrument Digital Interface), attributions de correctifs standard
- MIDI (Musical Instrument Digital Interface), attributions de correctifs standard
- MIDI (Musical Instrument Digital Interface), attributions de touches standard
- MIDI (Musical Instrument Digital Interface), attributions de touches standard
- création de fichiers MIDI, attributions de correctifs standard
- création de fichiers MIDI, attributions de clés standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe148c2fe1bb562aad994608a8c87c35e84bccb7d63ba1bc3ee3e5dd3bbc56a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065639"
---
# <a name="authoring-guidelines-for-midi-files"></a>Instructions de création pour les fichiers MIDI

Suivez ces instructions pour créer des fichiers MIDI indépendants de l’appareil pour Windows :

-   Utilisez les [affectations de correctifs MIDI standard](standard-midi-patch-assignments.md) et les [attributions de clés MIDI standard](standard-midi-key-assignments.md).
-   Toujours envoyer un message de modification de programme à un canal pour sélectionner un correctif avant d’envoyer d’autres messages à ce canal. Pour les deux canaux à percussion (10 et 16), sélectionnez le numéro de programme 0.
-   Suivez toujours un message MIDI de modification de programme avec un message de contrôleur de volume principal MIDI (numéro de contrôleur 7) pour définir le volume relatif du correctif.
-   Utilisez la valeur 80 (0x50) pour le contrôleur de volume principal pour les niveaux d’écoute normale. Pour des niveaux plus silencieux ou plus forts, vous pouvez utiliser des valeurs inférieures ou supérieures.
-   Utilisez uniquement les messages MIDI suivants : Remarque avec la vélocité, la note de désactivation, le changement de programme, la courbure du tangage, le volume principal (contrôleur 7) et la pédale d’amortisseur (contrôleur 64). Des synthétiseurs internes sont requis pour répondre à ces messages et la plupart des instruments de musique MIDI y répondent également.

 

 




