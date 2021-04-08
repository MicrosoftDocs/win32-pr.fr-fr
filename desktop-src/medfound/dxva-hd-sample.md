---
description: Montre comment utiliser la haute définition de l’accélération vidéo Microsoft DirectX (DXVA-HD).
ms.assetid: dfd5cf5c-7d6e-4894-8d9b-41ef0293b3d3
title: DXVA-HD, exemple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ae1945a98bc668aa12cc6cdf8d9e4693cbde27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861802"
---
# <a name="dxva-hd-sample"></a>DXVA-HD, exemple

Montre comment utiliser la haute définition de l’accélération vidéo Microsoft DirectX (DXVA-HD).

Cet exemple est essentiellement un port de l' [ \_ exemple DXVA2 VideoProc](dxva2-videoproc-sample.md). Il a les mêmes fonctions de base, et la plupart des commandes de clavier sont les mêmes.

L’exemple génère par programmation une vidéo avec un flux principal et un sous-flux. Le flux principal affiche les barres de couleur SMPTE. Le sous-flux est mélangé en alpha sur le flux principal à l’aide du masquage par luminance. L’utilisateur peut modifier les paramètres de traitement vidéo, y compris la valeur alpha planaire, les rectangles source et destination, les réglages de couleur et l’espace colorimétrique. L’illustration suivante montre la vidéo qui est générée.

![capture d’écran de l’exemple DXVA-HD](images/dxva-hd-sample.png)

## <a name="apis-demonstrated"></a>API illustrées

Cet exemple illustre les interfaces DXVA-HD suivantes :

-   [**\_Appareil IDXVAHD**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device)
-   [**IDXVAHD \_ VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor)

## <a name="requirements"></a>Configuration requise



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> <dt>

[Exemples du kit de développement logiciel Media Foundation](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



