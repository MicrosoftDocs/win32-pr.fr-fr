---
title: Modèles de conformité des périphériques audio
description: Modèles de conformité des périphériques audio
ms.assetid: dad3dd2c-595e-45ce-bd84-2a20bc656cfb
keywords:
- Windows Media Format SDK, modèles de conformité des appareils
- ASF (Advanced Systems Format), modèles de conformité des appareils
- ASF (format des systèmes avancés), modèles de conformité des appareils
- Windows Media Format SDK, modèles de conformité des périphériques audio
- ASF (Advanced Systems Format), modèles de conformité des périphériques audio
- ASF (format de systèmes avancés), modèles de conformité de périphérique audio
- Codec Windows Media Audio 9, modèles de conformité de périphérique audio
- codecs, codec Windows Media Audio 9
- modèles de conformité des appareils, vidéo
- modèles de conformité des périphériques audio
- modèles, modèles de conformité de périphérique audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e1065395e64fdd2d8e60585900307a4dd3f39b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309989"
---
# <a name="audio-device-conformance-templates"></a>Modèles de conformité des périphériques audio

Le tableau suivant répertorie les modèles de conformité de périphérique et les paramètres associés pour le codec Windows Media Audio 9, ou version ultérieure.



| Chaîne de modèle | Plage de vitesses de transmission     | Notes                                                                                                                                                                                                                                |
|-----------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ko            | 64 Kbits/s 160 kbps | Ce modèle est destiné aux appareils audio uniquement limités.                                                                                                                                                                        |
| NIV            | <= 160 Kbits/s     | Ce modèle correspond à la classe 4 dans le kit de portage des Windows Media Audio, qui prend en charge l’intégralité de l’implémentation du décodeur Windows Media Audio.                                                                                   |
| Mémoire            | <= 384 Kbits/s     | Ce modèle correspond à la classe 4 dans le kit de portage des Windows Media Audio, qui prend en charge l’intégralité de l’implémentation du décodeur Windows Media Audio. La plage de vitesses de transmission est la seule différence entre ce modèle et le niveau 2.<br/> |
| Budget             | Toutes les vitesses de transmission      | Ce modèle est destiné uniquement aux ordinateurs personnels, et est généralement utilisé pour présenter les fonctionnalités complètes du codec.                                                                                                           |



 

Le tableau suivant répertorie les modèles de conformité de périphérique et les paramètres associés pour le codec vocal Windows Media Audio 9.



| Chaîne de modèle | Plage de vitesses de transmission | Notes                                                                                                                      |
|-----------------|----------------|----------------------------------------------------------------------------------------------------------------------------|
| V1            | <= 20 Kbits/s  | Ce modèle est destiné uniquement aux appareils très peu complexes. Ce modèle est uniquement vocal.<br/>                    |
| S2            | <= 20 Kbits/s  | Il s’agit du modèle recommandé pour la plupart des applications. Ce modèle prend en charge les combinaisons de voix et de musique.<br/> |



 

Le tableau suivant répertorie les modèles de conformité de périphérique et les paramètres associés pour le codec Windows Media Audio 9 Professional, ou version ultérieure.



| Chaîne de modèle | Propriétés                                                                                   | Notes                                                                                                                                                                                                                                           |
|-----------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| M1            | Vitesse de transmission <= 384 KbpsSampling <= 48 kHz<br/> Canaux <= 5,1<br/>   | Ce modèle est recommandé pour les films standard avec un son surround.                                                                                                                                                                           |
| Carré            | Vitesse de transmission <= 768 KbpsSampling <= 96 kHz<br/> Canaux <= 5,1<br/>   | Ce modèle est recommandé pour les films haute définition avec un son surround.                                                                                                                                                                    |
| M3            | Vitesse de transmission <= 1 500 KbpsSampling <= 96 kHz<br/> Canaux <= 7,1<br/> | Ce modèle est recommandé pour les films haute définition avec un son surround à 8 canaux, tel que le contenu encodé pour la présentation dans des théâtres.                                                                                                    |
| "M"             | Taux d’échantillonnage de tous les bits ratesAll<br/> Tous les canaux<br/>                           | Ce modèle est destiné uniquement aux ordinateurs personnels, et est généralement utilisé pour présenter les fonctionnalités complètes du codec. Il s’agit également de la désignation du modèle pour toutes les données audio encodées avec le codec Windows Media Audio 9 Lossless.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Paramètres du modèle de conformité des appareils**](device-conformance-template-parameters.md)
</dt> <dt>

[**Combinaisons recommandées de modèles de conformité des appareils**](recommended-device-conformance-template-combinations.md)
</dt> <dt>

[**Modèles de conformité des périphériques vidéo**](video-device-conformance-templates.md)
</dt> </dl>

 

 





