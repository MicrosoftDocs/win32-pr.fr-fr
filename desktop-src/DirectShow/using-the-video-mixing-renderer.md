---
description: Utilisation du convertisseur de mixage vidéo
ms.assetid: 3d0fdfac-ec7e-4e02-886b-2039c607dac7
title: Utilisation du convertisseur de mixage vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5baf7d559eed0d3111876924520952b55c6da2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518771"
---
# <a name="using-the-video-mixing-renderer"></a>Utilisation du convertisseur de mixage vidéo

En termes de performances et d’étendue des fonctionnalités, le filtre de mixage vidéo (VMR) représente la prochaine génération de rendu vidéo sur la plateforme Windows. VMR remplace le [mélangeur de recouvrement](overlay-mixer-filter.md) et le [convertisseur vidéo](video-renderer-filter.md), et ajoute de nombreuses nouvelles fonctionnalités de mixage.

Il existe deux versions de VMR :

-   VMR-7, qui utilise DirectDraw 7 pour le rendu.
-   VMR-9, qui utilise Direct3D 9.

VMR-7 est disponible sur Windows XP et versions ultérieures, mais n’est pas disponible pour la redistribution. VMR-9 est disponible pour la redistribution sur toutes les plateformes prises en charge par DirectX 9. Les deux filtres VMR sont très similaires dans leur implémentation et les interfaces qu’ils exposent.

VMR-9 possède son propre CLSID et son propre ensemble d’interfaces, de structures et de types d’énumération qui ne sont pas toujours identiques aux types de données correspondants pour VMR-7, en raison des différences sous-jacentes entre DirectDraw 7 et Direct3D 9. Les interfaces VMR-9 se terminent toutes par « 9 », par exemple **IVMRStreamConfig9**, et les types de structures et d’énumération ont tous « VMR9 » dans leur nom pour les distinguer des types de données utilisés avec VMR-7.

Pour garantir la compatibilité descendante, VMR-9 n’est pas le convertisseur par défaut sur un système. Pour utiliser VMR-9, vous devez l’ajouter explicitement au graphique de filtre à l’aide de la méthode [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) , puis le configurer avant de le connecter à des filtres en amont.

Cet article contient les sections suivantes. Sauf mention contraire, les informations contenues dans ces sections s’appliquent aux filtres VMR-7 et VMR-9.

-   [À propos du rendu de mixage vidéo](about-the-video-mixing-render.md)
-   [Modes de fonctionnement VMR](vmr-modes-of-operation.md)
-   [Création d’un graphique de filtre VMR-9](building-a-vmr-9-filter-graph.md)
-   [Utilisation du mode de mixage VMR](using-vmr-mixing-mode.md)
-   [Définition des préférences de désentrelacement](setting-deinterlace-preferences.md)
-   [Utilisation de VMR pour les développeurs de filtres DirectShow](using-the-vmr-for-directshow-filter-developers.md)
-   [Utilisation du protocole COPP (Certified Output Protection Protocol)](using-certified-output-protection-protocol--copp.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtre de convertisseur de mixage vidéo 7](video-mixing-renderer-filter-7.md)
</dt> <dt>

[Filtre de convertisseur de mixage vidéo 9](video-mixing-renderer-filter-9.md)
</dt> </dl>

 

 



