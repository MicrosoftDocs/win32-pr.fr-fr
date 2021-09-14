---
title: À propos de l’exemple de plug-in audio DSP
description: À propos de l’exemple de plug-in audio DSP
ms.assetid: e60b055b-77e6-470e-91f6-9882827cf238
keywords:
- plug-ins Lecteur Windows Media, exemples
- plug-ins, exemples
- plug-ins de traitement de signal numérique, exemples
- Plug-ins DSP, exemples
- plug-ins Lecteur Windows Media, DSP audio
- plug-ins, DSP audio
- plug-ins de traitement de signal numérique, exemples audio
- Plug-ins DSP, exemples audio
- exemples, plug-ins DSP
- plug-ins DSP audio, exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edc3a5860c0c52837bfece16d2e709bf16d836d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856348"
---
# <a name="about-the-sample-audio-dsp-plug-in"></a>À propos de l’exemple de plug-in audio DSP

L’exemple de plug-in audio DSP fournit une implémentation de traitement simple qui met à l’échelle l’amplitude du son en fonction d’un facteur fourni par l’utilisateur dans la page de propriétés. Le plug-in accepte des valeurs comprises entre 0 et 1. La valeur par défaut est 1. La valeur 1 n’a aucun effet sur le son ; d’autres facteurs de mise à l’échelle sont des multiplicateurs pour les échantillons audio. Par exemple, une valeur de 0,5 entraînerait une baisse de 6 décibels du volume. La valeur zéro produit un silence.

L’exemple de plug-in audio DSP fonctionne avec le son stéréo ou mono PCM.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Génération d’un plug-in DSP**](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




