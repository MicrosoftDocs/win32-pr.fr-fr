---
title: Exemple Echo
description: Exemple Echo
ms.assetid: f28af52f-e948-464c-9600-aa516ab984f4
keywords:
- Plug-ins du lecteur Windows Media, vue d’ensemble de l’exemple Echo
- plug-ins, vue d’ensemble de l’exemple Echo
- plug-ins de traitement de signal numérique, vue d’ensemble de l’exemple Echo
- Plug-ins DSP, vue d’ensemble de l’exemple Echo
- Guide de programmation, plug-ins DSP
- exemples, plug-ins DSP
- Echo DSP, exemple de plug-in, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498f2dfe6a59257b8a16dc31a5b4cb751d649cd6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940053"
---
# <a name="the-echo-sample"></a>Exemple Echo

L’Assistant de plug-in du lecteur Windows Media peut créer un projet de plug-in DSP pour Microsoft Visual C++. Le code par défaut généré par l’Assistant permet à l’utilisateur de fournir un facteur d’échelle compris entre 0 et 1, qui est utilisé par le programme comme un multiplicateur pour les échantillons audio. Il s’agit d’une implémentation très simple que vous pouvez étudier pour comprendre comment le lecteur Windows Media interagit avec les plug-ins DSP. Les informations de la section intitulée [à propos des plug-ins DSP](about-dsp-plug-ins.md) peuvent vous aider à comprendre l’implémentation par défaut.

L’exemple décrit dans cette section est un peu plus complexe. Cet exemple permet à l’utilisateur de spécifier un délai, en millisecondes, et un niveau d’effet. Le code utilise ces valeurs pour générer un effet d’écho lors de la lecture de fichiers qui contiennent l’audio PCM (Pulse Code Modulation). La plupart des types de fichiers que le lecteur Windows Media affiche utilisent l’audio PCM.

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

 

 




