---
title: Implémentation de votre code DSP
description: Implémentation de votre code DSP
ms.assetid: e1feaaee-1127-4a3a-9a4c-a30584a7e8ff
keywords:
- plug-ins Lecteur Windows Media, traitement des signaux numériques (DSP)
- plug-ins, traitement des signaux numériques (DSP)
- plug-ins de traitement de signal numérique, implémentation du code
- Plug-ins DSP, implémentation du code
- plug-ins de traitement de signal numérique, modification de l’exemple de code
- Plug-ins DSP, modification de l’exemple de code
- plug-ins DSP audio, implémentation du code
- plug-ins vidéo DSP, implémentation du code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c9e17dad39a4ba0ebe79e31d9f3eead843d7f81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217049"
---
# <a name="implementing-your-dsp-code"></a>Implémentation de votre code DSP

une fois que vous avez créé l’exemple de plug-in dsp, vous pouvez modifier le code pour créer votre propre plug-in Lecteur Windows Media dsp. Les méthodes que vous modifiez et celles que vous pouvez conserver comme elles dépendent des facteurs suivants :

-   Nombre de propriétés que vous voulez autoriser l’utilisateur à modifier. Vous souhaiterez certainement modifier l’implémentation de la page de propriétés par défaut en fonction de vos besoins, et vous devrez peut-être ajouter des propriétés supplémentaires.
-   Si votre plug-in DSP doit allouer des ressources de streaming. Votre plug-in peut nécessiter des mémoires tampons supplémentaires.
-   si votre plug-in audio DSP doit continuer à sortir les données une fois que Lecteur Windows Media a cessé de fournir des données dans la mémoire tampon d’entrée.

les sections suivantes utilisent l’exemple de code du plug-in DSP généré par l’assistant de plug-in Lecteur Windows Media pour illustrer des concepts importants. il peut s’avérer utile d’ouvrir Microsoft Visual Studio et de générer l’exemple de code en premier afin de pouvoir vous y référer au fur et à mesure que vous lisez cette section. pour plus d’informations sur l’utilisation de l’assistant de plug-in Lecteur Windows Media, consultez [génération d’un plug-in DSP](building-a-dsp-plug-in.md).



| Section                                                                    | Description                                                                                                       |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Implémentation d’un plug-in DSP audio](implementing-an-audio-dsp-plug-in.md) | Décrit ce que vous devez savoir pour créer votre propre plug-in DSP audio basé sur l’exemple généré par l’Assistant. |
| [Implémentation d’un plug-in de DSP vidéo](implementing-a-video-dsp-plug-in.md)   | Décrit ce que vous devez savoir pour créer votre propre plug-in DSP vidéo basé sur l’exemple généré par l’Assistant. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des plug-ins DSP**](about-dsp-plug-ins.md)
</dt> </dl>

 

 




