---
title: Extraction d’un CD
description: Extraction d’un CD
ms.assetid: f5c1b5bf-d616-48cb-8690-e0237c56e402
keywords:
- Lecteur Windows Media, extraction de CD
- Modèle d’objet du lecteur Windows Media, extraction de CD
- modèle d’objet, extraction de CD
- Contrôle Windows Media Player ActiveX, extraction de CD
- Contrôle ActiveX, extraction de CD
- Windows Media Player Mobile contrôle ActiveX, extraction de CD
- Windows Media Player Mobile, extraction de CD
- Extraction de CD, à propos de
- extraction de CD, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767734b3449fd0a64b31c8f351406bbf9f6c805b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840457"
---
# <a name="ripping-a-cd"></a>Extraction d’un CD

Il existe deux façons d’extraire un CD à l’aide du contrôle du lecteur Windows Media. Le lecteur Windows Media 9 peut extraire des CD à l’aide de **IWMPPlayerServices :: setTaskPane**. Le lecteur Windows Media 11 introduit l’interface **IWMPCdromRip** pour l’extraction des CD. Cette interface offre plus de fonctionnalités que **IWMPPlayerServices :: setTaskPane**, et il est recommandé d’utiliser **IWMPCdromRip** si elle est disponible.

Les sections suivantes décrivent comment extraire un CD à l’aide du lecteur Windows Media.

-   [Extraction à l’aide de l’interface IWMPCdromRip](ripping-by-using-the-iwmpcdromrip-interface.md)
-   [Extraction à l’aide de IWMPPlayerServices :: setTaskPane](ripping-by-using-iwmpplayerservices--settaskpane.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de contrôle du lecteur**](player-control-guide.md)
</dt> </dl>

 

 




