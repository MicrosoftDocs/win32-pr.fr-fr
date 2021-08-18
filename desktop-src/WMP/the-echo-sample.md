---
title: Exemple Echo
description: Exemple Echo
ms.assetid: f28af52f-e948-464c-9600-aa516ab984f4
keywords:
- plug-ins Lecteur Windows Media, vue d’ensemble de l’exemple Echo
- plug-ins, vue d’ensemble de l’exemple Echo
- plug-ins de traitement de signal numérique, vue d’ensemble de l’exemple Echo
- Plug-ins DSP, vue d’ensemble de l’exemple Echo
- Guide de programmation, plug-ins DSP
- exemples, plug-ins DSP
- Echo DSP, exemple de plug-in, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103054e82157d83085713937759de8aa9ed250a5491146ebe0c71559ab1ca338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762789"
---
# <a name="the-echo-sample"></a>Exemple Echo

l’assistant de plug-in Lecteur Windows Media peut créer un projet de plug-in DSP pour Microsoft Visual C++. Le code par défaut généré par l’Assistant permet à l’utilisateur de fournir un facteur d’échelle compris entre 0 et 1, qui est utilisé par le programme comme un multiplicateur pour les échantillons audio. il s’agit d’une implémentation très simple que vous pouvez étudier pour comprendre comment Lecteur Windows Media interagit avec les plug-ins DSP. Les informations de la section intitulée [à propos des plug-ins DSP](about-dsp-plug-ins.md) peuvent vous aider à comprendre l’implémentation par défaut.

L’exemple décrit dans cette section est un peu plus complexe. Cet exemple permet à l’utilisateur de spécifier un délai, en millisecondes, et un niveau d’effet. Le code utilise ces valeurs pour générer un effet d’écho lors de la lecture de fichiers qui contiennent l’audio PCM (Pulse Code Modulation). la plupart des types de fichiers qui Lecteur Windows Media restituent utilisent l’audio PCM.

Ce guide comprend les sections suivantes :



| Section                                                                                | Description                                                                                                         |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Vue d’ensemble de l’exemple Echo](echo-sample-overview.md)                                       | Décrit les spécifications générales et les spécifications de l’exemple. Décrit le fonctionnement du plug-in.              |
| [Exemples de propriétés Echo](echo-sample-properties.md)                                   | Décrit comment modifier la propriété de code de l’Assistant et ajouter des méthodes pour la nouvelle propriété requise pour l’exemple Echo. |
| [Modification de la page de propriétés de l’exemple Echo](modifying-the-echo-sample-property-page.md) | Montre comment modifier l’implémentation de la page de propriétés existante pour qu’elle fonctionne avec l’exemple Echo.                         |
| [Utilisation des ressources de streaming](working-with-streaming-resources.md)               | Montre comment ajouter du code pour allouer et libérer une mémoire tampon requise pour l’exemple Echo.                                |
| [Implémentation de CEcho ::D oProcessOutput](implementing-cecho--doprocessoutput.md)         | Décrit comment implémenter le code qui crée l’effet Echo.                                                   |
| [Utilisation du plug-in Echo Sample DSP](using-the-echo-sample-dsp-plug-in.md)             | Décrit comment utiliser l’exemple terminé.                                                                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation de plug-ins DSP**](dsp-plug-ins-programming-guide.md)
</dt> </dl>

 

 




