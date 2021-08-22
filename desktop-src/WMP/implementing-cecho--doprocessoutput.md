---
title: Implémentation de CEcho DoProcessOutput
description: Implémentation de CEcho DoProcessOutput
ms.assetid: afd91022-4e2d-46a2-a0f4-cd2b558536d6
keywords:
- plug-ins Lecteur Windows Media, méthode DoProcessOutput d’exemple Echo
- plug-ins, ECHO, exemple DoProcessOutput, méthode
- plug-ins de traitement de signal numérique, méthode DoProcessOutput d’exemple Echo
- DSP plug-ins, ECHO, exemple DoProcessOutput, méthode
- Echo DSP, exemple de plug-in, méthode DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07054950cabadbc835c9904d48cdb4e6ddf5f05c0822c997558381958a9857d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135642"
---
# <a name="implementing-cechodoprocessoutput"></a>Implémentation de CEcho ::D oProcessOutput

La méthode **DoProcessOutput** effectue le traitement du signal numérique. il s’agit de la méthode qui apporte les modifications aux données fournies par Lecteur Windows Media. C’est le résultat de cette méthode que vous entendrez comme un effet d’écho lorsque votre plug-in Echo Sample est terminé.

Pour cet exemple, le plug-in traitera uniquement les données audio 8 bits ou 16 bits. Vous devrez apporter certaines modifications à l’exemple de code de l’Assistant de plug-in pour supprimer les sections qui traitent des données audio de profondeur en bits plus élevées. Toutefois, il est utile d’étudier ces sections, car vous pouvez décider d’ajouter votre propre implémentation d’écho pour ces formats.

Les sections suivantes détaillent les modifications que vous devez apporter au code :

-   [Suppression du code pour traiter une valeur supérieure à 16 bits](removing-the-code-to-process-greater-than-16-bits.md)
-   [Traitement des données audio](processing-the-audio-data.md)
-   [Variables pour effectuer le traitement](variables-to-perform-processing.md)
-   [Création de l’effet Echo](creating-the-echo-effect.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemple Echo**](the-echo-sample.md)
</dt> </dl>

 

 




