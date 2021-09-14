---
title: Implémentation d’un plug-in DSP audio
description: Implémentation d’un plug-in DSP audio
ms.assetid: 93ff0c45-f418-443d-8fba-c0a62f6e4e80
keywords:
- plug-ins Lecteur Windows Media, DSP audio
- plug-ins, DSP audio
- plug-ins de traitement de signal numérique, implémentation du code
- Plug-ins DSP, implémentation du code
- plug-ins de traitement de signal numérique, modification de l’exemple de code
- Plug-ins DSP, modification de l’exemple de code
- plug-ins de traitement de signal numérique, implémentation audio
- Plug-ins DSP, implémentation audio
- plug-ins DSP audio, implémentation du code
- plug-ins DSP audio, modification de l’exemple de code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdde8e7f00fc9ea3ad9bb8b7adb2d0a8bfba6b32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008430"
---
# <a name="implementing-an-audio-dsp-plug-in"></a>Implémentation d’un plug-in DSP audio

pour créer un plug-in Lecteur Windows Media DSP qui traite le son, vous devez modifier l’exemple de code dans la fonction nommée **DoProcessOutput**. **DoProcessOutput** est appelé chaque fois que Lecteur Windows Media appelle **IMediaObject ::P rocessoutput**. C’est la fonction qui effectue les tâches de traitement de signal numérique qui produisent le résultat audible que le plug-in DSP est destiné à produire.

Le traitement d’un flux audio est semblable à la gestion d’un événement chronométré. **DoProcessOutput** sera appelé à plusieurs reprises et à des intervalles spécifiques. Chaque fois que votre code s’exécute, il doit traiter un nombre spécifique d’octets de données. **DoProcessOutput** contient les paramètres suivants :



| Paramètre          | Description                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| *pbOutputData*     | Il s’agit d’un pointeur d' **octet** vers la mémoire tampon dans laquelle votre implémentation de **DoProcessOutput** doit copier ses données traitées. |
| *pbInputData*      | Il s’agit d’un pointeur d' **octet** constant vers la mémoire tampon qui contient les données à traiter.                               |
| *cbBytesToProcess* | Il s’agit d’une valeur **DWORD** qui contient le nombre d’octets dans la mémoire tampon d’entrée à traiter.             |



 

les sections suivantes fournissent des détails sur la modification du code généré par l’assistant de plug-in Lecteur Windows Media pour créer votre propre Plug-in DSP audio :

-   [Implémentation de DoProcessOutput](implementing-doprocessoutput.md)
-   [Ajout de propriétés à l’exemple de plug-in DSP audio](adding-properties-to-the-sample-audio-dsp-plug-in.md)
-   [Implémentation de la page de propriétés pour un plug-in DSP](implementing-the-property-page-for-a-dsp-plug-in.md)
-   [Modification de la propriété exemple de plug-in DSP audio](changing-the-sample-audio-dsp-plug-in-property.md)
-   [À propos de la discontinuité](about-discontinuity.md)
-   [À propos de l’allocation des ressources de streaming](about-allocating-streaming-resources.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des plug-ins DSP**](about-dsp-plug-ins.md)
</dt> </dl>

 

 




