---
title: Extraction d’un CD
description: Extraction d’un CD
ms.assetid: f5c1b5bf-d616-48cb-8690-e0237c56e402
keywords:
- Lecteur Windows Media, extraction de CD
- modèle d’objet Lecteur Windows Media, extraction de CD
- modèle d’objet, extraction de CD
- contrôle de ActiveX Lecteur Windows Media, extraction de CD
- contrôle de ActiveX, extraction de CD
- Lecteur Windows Media contrôle de ActiveX Mobile, extraction de CD
- Lecteur Windows Media Mobile, extraction de CD
- Extraction de CD, à propos de
- extraction de CD, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767734b3449fd0a64b31c8f351406bbf9f6c805b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416180"
---
# <a name="ripping-a-cd"></a>Extraction d’un CD

il existe deux façons d’extraire un CD à l’aide du contrôle Lecteur Windows Media. Lecteur Windows Media 9 peut extraire des cd à l’aide de **IWMPPlayerServices :: setTaskPane**. Lecteur Windows Media 11 introduit l’interface **IWMPCdromRip** pour l’extraction des CDs. Cette interface offre plus de fonctionnalités que **IWMPPlayerServices :: setTaskPane**, et il est recommandé d’utiliser **IWMPCdromRip** si elle est disponible.

les sections suivantes décrivent comment extraire un CD à l’aide de Lecteur Windows Media.

-   [Extraction à l’aide de l’interface IWMPCdromRip](ripping-by-using-the-iwmpcdromrip-interface.md)
-   [Extraction à l’aide de IWMPPlayerServices :: setTaskPane](ripping-by-using-iwmpplayerservices--settaskpane.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de contrôle du lecteur**](player-control-guide.md)
</dt> </dl>

 

 




