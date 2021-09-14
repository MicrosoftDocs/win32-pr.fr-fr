---
title: Interfaces requises (kit de développement logiciel (SDK) Lecteur Windows Media)
description: en savoir plus sur les interfaces requises que Lecteur Windows Media implémente dans DirectShow ou Media Foundation.
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- plug-ins Lecteur Windows Media, interfaces
- plug-ins, interfaces
- plug-ins de traitement de signal numérique, interfaces
- Plug-ins DSP, interfaces
- interfaces, plug-ins DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d27a0c0ed56db5f35c8cde8203fcf99a81a9260
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416194"
---
# <a name="required-interfaces-windows-media-player-sdk"></a>Interfaces requises (kit de développement logiciel (SDK) Lecteur Windows Media)

Lecteur Windows Media restitue l’audio et la vidéo à l’aide de l’un des pipelines suivants.

-   DirectShow
-   Media Foundation

dans Microsoft Windows XP et versions antérieures, le lecteur utilise DirectShow. dans Windows Vista, le lecteur utilise parfois DirectShow et parfois utilise Media Foundation.

Un plug-in DSP implémente une partie ou l’ensemble des interfaces suivantes :

-   **IMediaObject**
-   **IWMPPluginEnable**
-   **IMFTransform**
-   **IMFGetService**
-   **ISpecifyPropertyPages**

un plug-in qui implémente **IMediaObject** et **IWMPPluginEnable** peut s’exécuter dans le pipeline DirectShow. Il peut également s’exécuter dans le pipeline Media Foundation à l’intérieur d’un wrapper fourni par Media Foundation. Un plug-in de ce type est appelé objet multimédia Microsoft DirectX (DMO). il est courant de considérer un DMO comme étant analogue à un objet de filtre dans DirectShow. la documentation DMO se trouve dans la section DirectShow de la SDK Windows.

Un plug-in qui implémente **IMFTransform** et **IMFGetService** peut s’exécuter en mode natif (aucun Wrapper requis) dans le pipeline Media Foundation. Un plug-in de ce type est appelé Media Foundation transformation (MFT). la documentation MFT se trouve dans la section Media Foundation de la SDK Windows.

un plug-in qui implémente **IMediaObject**, **IWMPPluginEnable**, **IMFTransform** et **IMFGetService** peut s’exécuter dans le pipeline DirectShow et peut également s’exécuter en mode natif dans le pipeline Media Foundation. ce type de plug-in, qui est appelé un *plug-in DSP à double mode*, peut jouer le rôle d’un DMO ou d’une table MFT.

lorsque Lecteur Windows Media utilise un plug-in DSP à deux modes dans le pipeline Media Foundation, il commence par interroger l’interface **IMFTransform** . en cas d’échec de cette requête, Lecteur Windows Media des requêtes pour l’interface **IMediaObject** . Si la requête **IMediaObject** est réussie, le plug-in est encapsulé et ajouté au pipeline Media Foundation.

Quel que soit le pipeline, tout plug-in DSP permettant à l’utilisateur de définir des propriétés doit implémenter **ISpecifyPropertyPages**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble des développeurs de plug-ins DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**Interfaces du plug-in DSP**](dsp-plug-in-interfaces.md)
</dt> <dt>

[**Empaquetage du plug-in DSP**](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




