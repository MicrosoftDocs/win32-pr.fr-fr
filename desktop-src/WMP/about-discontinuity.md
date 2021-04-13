---
title: À propos de la discontinuité
description: À propos de la discontinuité
ms.assetid: 29210758-a1e6-47f2-9428-38f79623fbca
keywords:
- Plug-ins du lecteur Windows Media, DSP audio
- plug-ins, DSP audio
- plug-ins de traitement de signal numérique, discontinuité audio
- Plug-ins DSP, discontinuité audio
- plug-ins DSP audio, discontinuité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0448220d4616122b3c99670357bbbd78de11c392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379658"
---
# <a name="about-discontinuity"></a>À propos de la discontinuité

À tout moment, le lecteur Windows Media peut signaler une interruption dans le flux d’entrée en appelant la méthode **IMediaObject ::D iscontinuity** . Cela se produit régulièrement au début et à la fin d’un flux, ainsi qu’avant chaque opération de recherche ou lorsque le contenu de diffusion en continu est interrompu pour une raison quelconque. L’exemple de plug-in DSP généré par l’Assistant de plug-in du lecteur Windows Media n’a pas besoin de traiter les discontinuités pour les raisons suivantes :

-   Les exemples PCM sont atomiques, ce qui signifie qu’ils peuvent être traités sans tenir compte des autres exemples dans le flux. Certains formats vidéo contiennent des données qui dépendent d’images clés et d’exemples compressés.
-   L’exemple de code est écrit pour toujours forcer le client à traiter toute la sortie avant que le plug-in n’accepte davantage d’entrées.

L’implémentation par défaut de **IMediaObject ::D iscontinuity** retourne simplement S \_ OK.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation d’un plug-in DSP audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




