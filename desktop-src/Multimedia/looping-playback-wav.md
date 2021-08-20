---
title: Lecture en boucle (Wave audio)
description: Lecture en boucle (Wave audio)
ms.assetid: 8411290b-a3c5-4347-bee3-43c35188f736
keywords:
- audio Wave, sons en boucle
- Waveform-interface audio, bouclage des sons
- audio Wave, lecture en boucle
- Waveform-interface audio, lecture en boucle
- bouclage des sons Wave Audio
- bouclage-lecture audio
- waveOutWrite fonction)
- waveOutBreakLoop fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d98732ccc0a1d75ad13a10dc881b66a3bb634beab03a95a86a9db5689890979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139310"
---
# <a name="looping-playback"></a>Lecture en boucle

Le bouclage d’un son est contrôlé par les membres **dwLoops** et **dwFlags** dans les structures [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) passées à l’appareil avec la fonction [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) . Utilisez les indicateurs **WHDR \_ BEGINLOOP** et **WHDR \_ ENDLOOP** dans le membre **dwFlags** pour spécifier les blocs de données de début et de fin pour la boucle.

Pour effectuer une boucle sur un bloc de données unique, spécifiez les deux indicateurs pour le même bloc. Pour spécifier le nombre de boucles, utilisez le membre **dwLoops** dans la structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) pour le premier bloc de la boucle.

Vous pouvez appeler la fonction [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) pour arrêter un son en boucle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Jeux de fichiers Waveform-Audio](playing-waveform-audio-files.md)
</dt> </dl>

 

 
