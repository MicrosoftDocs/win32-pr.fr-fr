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
ms.openlocfilehash: a9689fe30b9c4f598cfc9bea892ff3d4fe15d3a9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106510471"
---
# <a name="handling-errors-with-midi-functions"></a>Gestion des erreurs avec les fonctions MIDI

Les fonctions audio MIDI retournent un code d’erreur différent de zéro. Pour les erreurs associées à MIDI, les fonctions [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) et [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) récupèrent les descriptions textuelles des codes d’erreur. L’application doit toujours examiner la valeur d’erreur elle-même pour déterminer comment procéder, mais elle peut utiliser les descriptions d’erreur dans les boîtes de dialogue pour informer les utilisateurs des conditions d’erreur.

Les seules fonctions MIDI qui ne retournent pas de codes d’erreur sont les fonctions [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) et [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) . Ces fonctions retournent une valeur de zéro si aucun appareil n’est présent dans un système ou si des erreurs sont rencontrées par la fonction.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Services MIDI](midi-services.md)
</dt> </dl>

 

 