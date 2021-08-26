---
title: À propos de la discontinuité
description: À propos de la discontinuité
ms.assetid: 29210758-a1e6-47f2-9428-38f79623fbca
keywords:
- plug-ins Lecteur Windows Media, DSP audio
- plug-ins, DSP audio
- plug-ins de traitement de signal numérique, discontinuité audio
- Plug-ins DSP, discontinuité audio
- plug-ins DSP audio, discontinuité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40de4c75c2d17699f0c72416873d64177e47d81761b27e5ffd465d89c9ecb9c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903569"
---
# <a name="about-discontinuity"></a>À propos de la discontinuité

à tout moment, Lecteur Windows Media pouvez signaler une interruption dans le flux d’entrée en appelant la méthode **IMediaObject ::D iscontinuity** . Cela se produit régulièrement au début et à la fin d’un flux, ainsi qu’avant chaque opération de recherche ou lorsque le contenu de diffusion en continu est interrompu pour une raison quelconque. l’exemple de plug-in DSP généré par l’assistant de plug-in Lecteur Windows Media n’a pas besoin de traiter les discontinuités pour les raisons suivantes :

-   Les exemples PCM sont atomiques, ce qui signifie qu’ils peuvent être traités sans tenir compte des autres exemples dans le flux. Certains formats vidéo contiennent des données qui dépendent d’images clés et d’exemples compressés.
-   L’exemple de code est écrit pour toujours forcer le client à traiter toute la sortie avant que le plug-in n’accepte davantage d’entrées.

L’implémentation par défaut de **IMediaObject ::D iscontinuity** retourne simplement S \_ OK.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation d’un plug-in DSP audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




