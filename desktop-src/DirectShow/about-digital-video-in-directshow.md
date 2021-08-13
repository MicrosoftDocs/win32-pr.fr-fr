---
description: À propos de la vidéo numérique dans DirectShow
ms.assetid: 0570bf7c-c38d-4ada-9593-27b9be117893
title: À propos de la vidéo numérique dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061927618c1cb3340e0771376a7a1e232e078e043a554829f99580262ea29c58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664809"
---
# <a name="about-digital-video-in-directshow"></a>À propos de la vidéo numérique dans DirectShow

La vidéo numérique (DV) peut être capturée à partir d’une caméra DV, stockée dans un fichier sur l’ordinateur de l’utilisateur, ou stockée sur bande à l’aide d’un magnétoscope vidéo. Par conséquent, les opérations qu’une application peut effectuer sur un flux DV sont les suivantes :

-   Capturez des vidéos en direct à partir d’une caméra DV.
-   Transmettez les données DV de VTR tape sur l’ordinateur.
-   Transmettez les données DV de l’ordinateur au magnétoscope.
-   Lire des données DV à partir d’un fichier.
-   Écrire des données DV dans un fichier.
-   Affichez l’audio et la vidéo dans un flux DV.

DirectShow fournit les filtres DV suivants :

-   [Pilote MSDV](msdv-driver.md). Le pilote MSDV contrôle un périphérique DV, tel qu’un caméscope. L’appareil peut avoir une sous-unité de caméra et une sous-unité VTR. MSDV contrôle les deux sous-unités. le pilote MSDV apparaît pour les applications sous la forme d’un filtre DirectShow.
-   Filtre de [séparateur DV](dv-splitter-filter.md) . Les images DV contiennent des données audio et vidéo dans le même cadre. Le filtre de séparateur DV extrait les données audio et les renvoie sous la forme d’un ou de deux flux audio. Il génère les données d’origine sous la forme d’un flux vidéo DV distinct.
-   Filtre de [décodage vidéo DV](dv-video-decoder-filter.md) . Décode la vidéo DV en vidéo non compressée.
-   Filtre d' [encodeur vidéo DV](dv-video-encoder-filter.md) . Encode la vidéo non compressée en vidéo encodée en DV.
-   [Du multiplexeur DV](dv-muxer-filter.md). Combine un flux vidéo DV avec un ou deux flux audio pour créer un flux DV entrelacé unique.

Le séparateur DV et le décodeur vidéo DV fonctionnent ensemble. Le séparateur prend le flux entrelacé et génère des flux de données audio et vidéo DV distincts. Le décodeur convertit la vidéo DV en vidéo non compressée. L’illustration suivante montre ce processus.

![séparateur DV et décodeur DV](images/dv-filters1.png)

L’encodeur vidéo DV et le DV du multiplexeur inversent le processus : l’encodeur convertit la vidéo non compressée en vidéo DV et le multiplexeur combine une vidéo audio et DV pour créer un flux entrelacé unique, comme indiqué dans le diagramme suivant.

![encodeur DV et DV du multiplexeur](images/dv-filters2.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vidéo numérique en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



