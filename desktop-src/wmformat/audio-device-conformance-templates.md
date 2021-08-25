---
title: Modèles de conformité des périphériques audio
description: Modèles de conformité des périphériques audio
ms.assetid: dad3dd2c-595e-45ce-bd84-2a20bc656cfb
keywords:
- Windows Media Format SDK, modèles de conformité des appareils
- ASF (Advanced Systems Format), modèles de conformité des appareils
- ASF (format des systèmes avancés), modèles de conformité des appareils
- Windows Media Format SDK, modèles de conformité de périphérique audio
- ASF (Advanced Systems Format), modèles de conformité des périphériques audio
- ASF (format de systèmes avancés), modèles de conformité de périphérique audio
- Windows Codec audio 9 Media, modèles de conformité de périphérique audio
- codecs, codec Windows Media Audio 9
- modèles de conformité des appareils, vidéo
- modèles de conformité des périphériques audio
- modèles, modèles de conformité de périphérique audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b66c3c414ef2132120cb0824e1e48847310396cf8002d95be13d7f841a0ff6db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840249"
---
# <a name="audio-device-conformance-templates"></a>Modèles de conformité des périphériques audio

le tableau suivant répertorie les modèles de conformité de périphérique et les paramètres associés pour le codec Windows Media Audio 9, ou version ultérieure.



| Chaîne de modèle | Plage de vitesses de transmission     | Remarques                                                                                                                                                                                                                                |
|-----------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ko            | 64 Kbits/s 160 kbps | Ce modèle est destiné aux appareils audio uniquement limités.                                                                                                                                                                        |
| NIV            | <= 160 Kbits/s     | ce modèle correspond à la classe 4 dans le kit de portage des Windows Media Audio, qui prend en charge l’intégralité de l’implémentation du décodeur Windows Media Audio.                                                                                   |
| Mémoire            | <= 384 Kbits/s     | ce modèle correspond à la classe 4 dans le kit de portage des Windows Media Audio, qui prend en charge l’intégralité de l’implémentation du décodeur Windows Media Audio. La plage de vitesses de transmission est la seule différence entre ce modèle et le niveau 2.<br/> |
| Budget             | Toutes les vitesses de transmission      | Ce modèle est destiné uniquement aux ordinateurs personnels, et est généralement utilisé pour présenter les fonctionnalités complètes du codec.                                                                                                           |



 

le tableau suivant répertorie les modèles de conformité de périphérique et les paramètres associés pour le codec vocal Windows Media Audio 9.



| Chaîne de modèle | Plage de vitesses de transmission | Remarques                                                                                                                      |
|-----------------|----------------|----------------------------------------------------------------------------------------------------------------------------|
| V1            | <= 20 Kbits/s  | Ce modèle est destiné uniquement aux appareils très peu complexes. Ce modèle est uniquement vocal.<br/>                    |
| S2            | <= 20 Kbits/s  | Il s’agit du modèle recommandé pour la plupart des applications. Ce modèle prend en charge les combinaisons de voix et de musique.<br/> |



 

le tableau suivant répertorie les modèles de conformité de périphérique et les paramètres associés pour le Windows Media Audio 9 Professional codec ou version ultérieure.



| Chaîne de modèle | Propriétés                                                                                   | Remarques                                                                                                                                                                                                                                           |
|-----------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| M1            | Vitesse de transmission <= 384 KbpsSampling <= 48 kHz<br/> Canaux <= 5,1<br/>   | Ce modèle est recommandé pour les films standard avec un son surround.                                                                                                                                                                           |
| Carré            | Vitesse de transmission <= 768 KbpsSampling <= 96 kHz<br/> Canaux <= 5,1<br/>   | Ce modèle est recommandé pour les films haute définition avec un son surround.                                                                                                                                                                    |
| M3            | Vitesse de transmission <= 1 500 KbpsSampling <= 96 kHz<br/> Canaux <= 7,1<br/> | Ce modèle est recommandé pour les films haute définition avec un son surround à 8 canaux, tel que le contenu encodé pour la présentation dans des théâtres.                                                                                                    |
| "M"             | Taux d’échantillonnage de tous les bits ratesAll<br/> Tous les canaux<br/>                           | Ce modèle est destiné uniquement aux ordinateurs personnels, et est généralement utilisé pour présenter les fonctionnalités complètes du codec. il s’agit également de la désignation du modèle pour toutes les données audio encodées avec le codec Windows Media Audio 9 Lossless.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Paramètres du modèle de conformité des appareils**](device-conformance-template-parameters.md)
</dt> <dt>

[**Combinaisons recommandées de modèles de conformité des appareils**](recommended-device-conformance-template-combinations.md)
</dt> <dt>

[**Modèles de conformité des périphériques vidéo**](video-device-conformance-templates.md)
</dt> </dl>

 

 





