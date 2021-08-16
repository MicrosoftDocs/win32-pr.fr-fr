---
title: Empaquetage du plug-in DSP
description: Empaquetage du plug-in DSP
ms.assetid: 5d40a39b-0fe8-4f77-9465-8e31d1f2708e
keywords:
- plug-ins Lecteur Windows Media, pipeline Media Foundation
- plug-ins, pipeline Media Foundation
- plug-ins de traitement de signal numérique, pipeline Media Foundation
- Plug-ins DSP, pipeline Media Foundation
- Pipeline Media Foundation
- plug-ins Lecteur Windows Media, pipeline DirectShow
- plug-ins, pipeline DirectShow
- plug-ins de traitement de signal numérique, pipeline DirectShow
- plug-ins DSP, pipeline DirectShow
- pipeline DirectShow
- plug-ins de traitement de signal numérique, de base
- Plug-ins DSP, de base
- plug-ins Lecteur Windows Media, DSP de base
- plug-ins, DSP de base
- plug-ins de base DSP
- plug-ins Lecteur Windows Media, DSP en deux modes
- plug-ins, DSP en deux modes
- plug-ins de traitement de signal numérique, double mode
- Plug-ins DSP, double mode
- plug-ins DSP à double mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bd87e1729b4d8759f3b9f1d7d4d7993660512d49c34ea9bf9aa34802b69cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749504"
---
# <a name="dsp-plug-in-packaging"></a>Empaquetage du plug-in DSP

Lecteur Windows Media restitue l’audio et la vidéo à l’aide de l’un des pipelines suivants.

-   DirectShow
-   Media Foundation

dans Microsoft Windows XP et versions antérieures, le lecteur utilise DirectShow. dans Windows Vista, le lecteur utilise parfois DirectShow et parfois utilise Media Foundation.

un plug-in dsp conçu pour s’exécuter dans le pipeline DirectShow est appelé un *plug-in dsp de base*. Un plug-in DSP de base agit comme un objet média DirectX (DMO). un plug-in DSP de base peut s’exécuter en mode natif dans le pipeline DirectShow et peut également s’exécuter dans le pipeline Media Foundation à l’intérieur d’un wrapper fourni par Media Foundation.

un plug-in dsp conçu pour s’exécuter en mode natif (aucun wrapper requis) à la fois dans les pipelines DirectShow et Media Foundation est appelé un *plug-in dsp à double mode*. un plug-in DSP à deux modes peut agir en tant que DMO ou en tant que transformation de Media Foundation (MFT).

Un plug-in DSP est un objet COM qui est empaqueté comme un fichier de .dll auto-inscrit. Les interfaces implémentées par le plug-in varient selon que le plug-in est conçu comme un plug-in DSP de base ou en tant que plug-in DSP à double mode. Pour obtenir des informations détaillées sur les interfaces que les plug-ins DSP doivent implémenter, consultez [interfaces requises](required-interfaces.md).

Un plug-in DSP qui s’exécute dans le pipeline Media Foundation (soit en mode natif, soit encapsulé) doit inscrire son modèle de thread comme « both ». Pour plus d’informations sur les sous-clés et les entrées de Registre associées aux plug-ins DSP, consultez [inscription des plug-ins DSP](registering-dsp-plug-ins.md).

Un plug-in DSP qui implémente des interfaces personnalisées et s’exécute dans le pipeline Media Foundation (en mode natif ou encapsulé) doit être associé à un fichier de .dll proxy-stub qui peut marshaler les interfaces personnalisées entre les limites du processus. pour plus d’informations sur le composant proxy-stub, consultez [mise à jour des plug-ins dsp existants](updating-existing-dsp-plug-ins.md) et [mises à jour de l’assistant de plug-in dsp pour Lecteur Windows Media 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).

Les objets de plug-in DSP ne doivent pas être créés en tant que singletons. Lecteur Windows Media devez être en mesure de créer plusieurs instances distinctes d’un plug-in DSP particulier.

les plug-ins DSP qui s’exécutent dans le chemin d’accès au support protégé Windows Vista (PMP) doivent être signés. pour plus d’informations, consultez [signature du Code pour les composants multimédias protégés dans Windows Vista](/windows-hardware/test/hlk/).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble des développeurs de plug-ins DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 