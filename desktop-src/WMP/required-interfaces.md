---
title: Interfaces requises (Windows Media Player SDK)
description: En savoir plus sur les interfaces requises que le lecteur Windows Media implémente dans DirectShow ou Media Foundation.
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Plug-ins du lecteur Windows Media, interfaces
- plug-ins, interfaces
- plug-ins de traitement de signal numérique, interfaces
- Plug-ins DSP, interfaces
- interfaces, plug-ins DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d27a0c0ed56db5f35c8cde8203fcf99a81a9260
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406092"
---
# <a name="required-interfaces-windows-media-player-sdk"></a>Interfaces requises (Windows Media Player SDK)

Le lecteur Windows Media effectue le rendu des données audio et vidéo à l’aide de l’un des pipelines suivants.

-   DirectShow
-   Media Foundation

Dans Microsoft Windows XP et les versions antérieures, le lecteur utilise DirectShow. Dans Windows Vista, le lecteur utilise parfois DirectShow et utilise parfois Media Foundation.

Un plug-in DSP implémente une partie ou l’ensemble des interfaces suivantes :

-   **IMediaObject**
-   **IWMPPluginEnable**
-   **IMFTransform**
-   **IMFGetService**
-   **ISpecifyPropertyPages**

Un plug-in qui implémente **IMediaObject** et **IWMPPluginEnable** peut s’exécuter dans le pipeline DirectShow. Il peut également s’exécuter dans le pipeline Media Foundation à l’intérieur d’un wrapper fourni par Media Foundation. Un plug-in de ce type est appelé Microsoft DirectX Media Object (DMO). Il est courant de considérer qu’un DMO est analogue à un objet filtre dans DirectShow. La documentation DMO se trouve dans la section DirectShow du SDK Windows.

Un plug-in qui implémente **IMFTransform** et **IMFGetService** peut s’exécuter en mode natif (aucun Wrapper requis) dans le pipeline Media Foundation. Un plug-in de ce type est appelé Media Foundation transformation (MFT). La documentation MFT se trouve dans la section Media Foundation de la SDK Windows.

Un plug-in qui implémente **IMediaObject**, **IWMPPluginEnable**, **IMFTransform** et **IMFGetService** peut s’exécuter dans le pipeline DirectShow et peut également s’exécuter en mode natif dans le pipeline Media Foundation. Ce type de plug-in, qui est appelé un *plug-in DSP à double mode*, peut jouer le rôle d’un module DMO ou d’une table MFT.

Lorsque le lecteur Windows Media utilise un plug-in DSP à double mode dans le pipeline Media Foundation, il commence par interroger l’interface **IMFTransform** . Si cette requête échoue, le lecteur Windows Media recherche l’interface **IMediaObject** . Si la requête **IMediaObject** est réussie, le plug-in est encapsulé et ajouté au pipeline Media Foundation.

Quel que soit le pipeline, tout plug-in DSP permettant à l’utilisateur de définir des propriétés doit implémenter **ISpecifyPropertyPages**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble des développeurs de plug-ins DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**Interfaces du plug-in DSP**](dsp-plug-in-interfaces.md)
</dt> <dt>

[**Empaquetage du plug-in DSP**](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




