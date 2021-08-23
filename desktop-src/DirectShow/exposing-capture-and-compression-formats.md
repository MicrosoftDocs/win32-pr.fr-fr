---
description: Exposition des formats de capture et de compression
ms.assetid: f7466cfe-b13e-4ee9-82f9-0528ed97bf99
title: Exposition des formats de capture et de compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80821ade82b894a7c3e2752528ffdd72bc2223a4616b629f7e2b236461b31e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685739"
---
# <a name="exposing-capture-and-compression-formats"></a>Exposition des formats de capture et de compression

Cet article explique comment retourner des formats de capture et de compression à l’aide de la méthode [**IAMStreamConfig :: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) . Cette méthode peut obtenir plus d’informations sur les types de médias acceptés que la méthode classique d’énumération des types de média d’un pin. il est donc préférable de l’utiliser à la place. **GetStreamCaps** peut retourner des informations sur les types de formats autorisés pour l’audio ou la vidéo. En outre, cet article fournit un exemple de code qui montre comment reconnecter la broche d’entrée d’un filtre de transformation pour garantir que votre filtre peut produire une sortie particulière.

La méthode **GetStreamCaps** retourne un tableau de paires de structures de type de média et de fonctionnalités. Le type de média est une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) et les fonctionnalités sont représentées soit par une structure d' [**\_ \_ \_ embout de la configuration de flux audio**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) , soit par une structure de [**\_ \_ configuration \_ de flux vidéo**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) . La première section de cet article présente un exemple de vidéo et la deuxième présente un exemple audio.

Cet article contient les rubriques suivantes :

-   [Fonctionnalités vidéo](video-capabilities.md)
-   [Fonctionnalités audio](audio-capabilities.md)
-   [Reconnexion de votre entrée pour garantir des types de sortie spécifiques](reconnecting-your-input-to-ensure-specific-output-types.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[écriture de filtres de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



