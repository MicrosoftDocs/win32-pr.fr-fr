---
title: Empaquetage du plug-in DSP
description: Empaquetage du plug-in DSP
ms.assetid: 5d40a39b-0fe8-4f77-9465-8e31d1f2708e
keywords:
- Plug-ins du lecteur Windows Media, pipeline Media Foundation
- plug-ins, pipeline Media Foundation
- plug-ins de traitement de signal numérique, pipeline Media Foundation
- Plug-ins DSP, pipeline Media Foundation
- Pipeline Media Foundation
- Plug-ins du lecteur Windows Media, pipeline DirectShow
- plug-ins, pipeline DirectShow
- plug-ins de traitement de signal numérique, pipeline DirectShow
- Plug-ins DSP, pipeline DirectShow
- Pipeline DirectShow
- plug-ins de traitement de signal numérique, de base
- Plug-ins DSP, de base
- Plug-ins du lecteur Windows Media, DSP de base
- plug-ins, DSP de base
- plug-ins de base DSP
- Plug-ins du lecteur Windows Media, DSP en deux modes
- plug-ins, DSP en deux modes
- plug-ins de traitement de signal numérique, double mode
- Plug-ins DSP, double mode
- plug-ins DSP à double mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62535abe0d82975bf07fef178ac43cf066c6afbd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513530"
---
# <a name="dsp-plug-in-packaging"></a>Empaquetage du plug-in DSP

Le lecteur Windows Media effectue le rendu des données audio et vidéo à l’aide de l’un des pipelines suivants.

-   DirectShow
-   Media Foundation

Dans Microsoft Windows XP et les versions antérieures, le lecteur utilise DirectShow. Dans Windows Vista, le lecteur utilise parfois DirectShow et utilise parfois Media Foundation.

Un plug-in DSP conçu pour s’exécuter dans le pipeline DirectShow est appelé un *plug-in DSP de base*. Un plug-in DSP de base agit comme un objet de média DirectX (DMO). Un plug-in DSP de base peut s’exécuter en mode natif dans le pipeline DirectShow et peut également s’exécuter dans le pipeline Media Foundation à l’intérieur d’un wrapper fourni par Media Foundation.

Un plug-in DSP conçu pour s’exécuter en mode natif (aucun Wrapper requis) à la fois dans les pipelines DirectShow et Media Foundation est appelé un *plug-in DSP à double mode*. Un plug-in DSP à deux modes peut agir comme DMO ou comme une transformation de Media Foundation (MFT).

Un plug-in DSP est un objet COM qui est empaqueté en tant que fichier. dll à inscription automatique. Les interfaces implémentées par le plug-in varient selon que le plug-in est conçu comme un plug-in DSP de base ou en tant que plug-in DSP à double mode. Pour obtenir des informations détaillées sur les interfaces que les plug-ins DSP doivent implémenter, consultez [interfaces requises](required-interfaces.md).

Un plug-in DSP qui s’exécute dans le pipeline Media Foundation (soit en mode natif, soit encapsulé) doit inscrire son modèle de thread comme « both ». Pour plus d’informations sur les sous-clés et les entrées de Registre associées aux plug-ins DSP, consultez [inscription des plug-ins DSP](registering-dsp-plug-ins.md).

Un plug-in DSP qui implémente des interfaces personnalisées et s’exécute dans le pipeline Media Foundation (en mode natif ou encapsulé) doit être associé à un fichier. dll proxy-stub qui peut marshaler les interfaces personnalisées au-delà des limites du processus. Pour plus d’informations sur le composant proxy-stub, consultez [mise à jour des plug-ins DSP existants](updating-existing-dsp-plug-ins.md) et [mises à jour de l’Assistant de plug-in DSP pour le lecteur Windows Media 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).

Les objets de plug-in DSP ne doivent pas être créés en tant que singletons. Le lecteur Windows Media doit être en mesure de créer plusieurs instances distinctes d’un plug-in DSP particulier.

Les plug-ins DSP qui s’exécutent dans le chemin d’accès de support protégé de Windows Vista (PMP) doivent être signés. Pour plus d’informations, consultez [signature du code pour les composants multimédias protégés dans Windows Vista](/windows-hardware/test/hlk/).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble des développeurs de plug-ins DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 