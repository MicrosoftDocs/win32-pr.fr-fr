---
title: Lecture audio simple
description: Lecture audio simple
ms.assetid: 51a0244d-123d-4efe-92e9-972e914cef78
keywords:
- audio multimédia, forme d’onde
- audio, forme d’onde
- audio Wave, lecture simple
- MessageBeep, fonction
- sndPlaySound fonction)
- PlaySound, fonction, lecture simple
- audio multimédia, fonction PlaySound
- audio, PlaySound, fonction
- Wave audio, fonction PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6388f9800f93080e995ae537c2458a22da033ab2149b4bfca114c25025d97434
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688689"
---
# <a name="simple-audio-playback"></a>Lecture audio simple

Vous pouvez utiliser les fonctions suivantes pour lire les données audio de forme d’onde dans votre application dans un appel de fonction unique.



| Fonction                                                      | Description                                                                                                         |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [MessageBeep](/windows/win32/api/winuser/nf-winuser-messagebeep) | Lit le son qui correspond à un niveau d’alerte système spécifié.                                                 |
| [**sndPlaySound**](/previous-versions//dd798676(v=vs.85))                          | Lit le son qui correspond au son du système entré dans le registre ou le contenu du fichier spécifié. |
| [**PlaySound**](/previous-versions//dd743680(v=vs.85))                                | Fournit toutes les fonctionnalités de [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) et peut accéder directement aux ressources.           |



 

La fonction **MessageBeep** est une partie standard de l’API Win32. étant donné que ses fonctionnalités sont très limitées et qu’elles sont documentées ailleurs, elles ne sont pas abordées ici.

Les fonctions listées prennent en charge les sources audio Wave suivantes :

-   Fichiers Waveform-Audio associés aux niveaux d’alerte système
-   Fichiers Waveform-Audio spécifiés par les entrées dans le registre
-   Ressources d’ondulation en mémoire
-   Waveform-fichiers audio spécifiés par le nom

Les fonctions [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) et [**PlaySound**](/previous-versions//dd743680(v=vs.85)) chargent l’intégralité d’un fichier Waveform-Audio en mémoire et limitent, en effet, la taille du fichier qu’ils peuvent lire. Utilisez **sndPlaySound** et **PlaySound** pour lire des fichiers audio Waveform de petite taille, jusqu’à 100 000. Ces deux fonctions nécessitent également que les données audio soient dans un format lisible par l’un des pilotes audio Wave installés, y compris le Mappeur Wave.

Pour les fichiers audio plus volumineux, utilisez les services MCI (Media Control Interface). Pour plus d’informations, consultez [MCI](mci.md).

 

 