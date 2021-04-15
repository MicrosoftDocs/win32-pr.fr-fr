---
title: Assistant de plug-in DSP
description: Assistant de plug-in DSP
ms.assetid: 3d1ae5ef-12c4-4db3-815a-2adc73353f20
keywords:
- Plug-ins du lecteur Windows Media, Assistant plug-in
- plug-ins, Assistant de plug-in
- plug-ins de traitement de signal numérique, Assistant plug-in
- Plug-ins DSP, Assistant plug-in
- Assistant de plug-in
- Visual Studio, Assistant de plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a7228056d821d2c2bca258f5c236fe1dce11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507186"
---
# <a name="dsp-plug-in-wizard"></a>Assistant de plug-in DSP

Le kit de développement logiciel (SDK) du lecteur Windows Media fournit un assistant de plug-in que vous pouvez ajouter à Visual Studio. L’Assistant peut générer un exemple de code pour différents plug-ins, y compris les types suivants de plug-ins DSP :

-   Plug-in DSP audio
-   Plug-in audio DSP (mode double)
-   Plug-in de vidéo DSP
-   Plug-in de vidéo DSP (double mode)

Chacun des deux exemples de plug-ins de base, DSP et Video DSP, fonctionne comme un objet de média DirectX (DMO). Autrement dit, chaque exemple de plug-in implémente l’interface **IMediaObject** . Chacun des deux exemples de plug-ins en mode double peut fonctionner en tant qu’DMO ou en tant que transformation de Media Foundation (MFT). Autrement dit, chaque plug-in d’exemple en mode double implémente à la fois l’interface **IMediaObject** et l’interface **IMFTransform** .

Vous pouvez compiler, lier, inscrire et tester l’exemple de code de plug-in. Vous pouvez ensuite modifier l’exemple de code généré pour créer votre propre plug-in DSP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Génération d’un plug-in DSP**](building-a-dsp-plug-in.md)
</dt> <dt>

[**Vue d’ensemble des développeurs de plug-ins DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**Mises à jour de l’Assistant de plug-in DSP pour le lecteur Windows Media 11**](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)
</dt> </dl>

 

 




