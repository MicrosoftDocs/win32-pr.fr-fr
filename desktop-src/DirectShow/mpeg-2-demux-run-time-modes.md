---
description: Modes de Run-Time MPEG-2 demux
ms.assetid: b0d0c725-9220-43a5-af1c-d3c5c72e1ef3
title: Modes de Run-Time MPEG-2 demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e4e7a1dea0bfeccd60d8680a31b99cc10271ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219036"
---
# <a name="mpeg-2-demux-run-time-modes"></a>Modes de Run-Time MPEG-2 demux

Le [démultiplexeur MPEG-2](mpeg-2-demultiplexer.md) (« demux ») peut fonctionner en mode push ou en mode par extraction. En mode push, les données proviennent d’une source active, telle qu’une diffusion réseau. En mode par extraction, les données proviennent d’un fichier local.

-   le mode par extraction est disponible dans Windows XP et versions ultérieures, uniquement pour les flux de programme. Sur les plateformes de niveau supérieur, utilisez le filtre de [séparateur MPEG-2](mpeg-2-splitter.md) .
-   Le mode push est disponible sur toutes les plateformes, pour les flux de programme et les flux de transport.

Le demux prend donc en charge trois modes possibles : les flux de programme en mode par extraction, les flux de programme en mode push et les flux de transport en mode push. Le demux détermine le mode à utiliser au moment de l’exécution. Le mode est déterminé lorsque la broche d’entrée se connecte, ou lorsque la première broche de sortie est configurée, selon ce qui se produit en premier :

-   lorsque la broche d’entrée se connecte : sur Windows XP et versions ultérieures, le demux interroge le filtre en amont pour l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ; Si le filtre en amont expose cette interface, demux se configure lui-même pour les flux de programme en mode par extraction. Dans le cas contraire, le demux utilise le mode push et le type de média détermine le type de flux (flux de programme ou flux de transport). Pour obtenir la liste des types d’entrée, consultez [**types de média MPEG-2 DEMULTIPLEXEUR**](mpeg-2-demultiplexer-media-types.md) .
-   Quand la première broche de sortie est configurée : Si vous créez une broche de sortie et que vous la interrogez pour [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap), le demux se configure pour les flux de transport en mode push. Si vous interrogez le code PIN pour [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap), le demux se configure lui-même pour les flux de programme, également en mode push. Toutes les requêtes suivantes pour l’autre interface échouent, car le demux ne peut pas fonctionner en deux modes à la fois.

Une fois que le demux a été configuré pour un mode particulier, il reste dans ce mode. Pour utiliser un mode différent, vous devez créer une nouvelle instance de demux.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du démultiplexeur MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



