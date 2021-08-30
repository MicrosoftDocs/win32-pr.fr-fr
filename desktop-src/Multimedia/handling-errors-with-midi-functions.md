---
title: Gestion des erreurs avec les fonctions MIDI
description: Gestion des erreurs avec les fonctions MIDI
ms.assetid: 7ea5db5e-34d7-4506-8157-c24adf5bcdda
keywords:
- MIDI (Musical Instrument Digital Interface), Erreurs
- MIDI (Musical Instrument Digital Interface), Erreurs
- Services MIDI, Erreurs
- Erreurs MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5831763157f34728c3ed3a94a2be14e227921a710fd17a3cd55d1a24bd00b07f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785079"
---
# <a name="handling-errors-with-midi-functions"></a>Gestion des erreurs avec les fonctions MIDI

Les fonctions audio MIDI retournent un code d’erreur différent de zéro. Pour les erreurs associées à MIDI, les fonctions [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) et [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) récupèrent les descriptions textuelles des codes d’erreur. L’application doit toujours examiner la valeur d’erreur elle-même pour déterminer comment procéder, mais elle peut utiliser les descriptions d’erreur dans les boîtes de dialogue pour informer les utilisateurs des conditions d’erreur.

Les seules fonctions MIDI qui ne retournent pas de codes d’erreur sont les fonctions [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) et [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) . Ces fonctions retournent une valeur de zéro si aucun appareil n’est présent dans un système ou si des erreurs sont rencontrées par la fonction.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Services MIDI](midi-services.md)
</dt> </dl>

 

 