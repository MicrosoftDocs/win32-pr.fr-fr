---
description: filtre de superposition Mixer 2
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: filtre de superposition Mixer 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b51dceb2a7f82a91fe30275cacfaad4ad78eded
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312346"
---
# <a name="overlay-mixer-2-filter"></a>filtre de superposition Mixer 2

le filtre de superposition Mixer 2 est identique à la [superposition Mixer](overlay-mixer-filter.md) le filtre, sauf :

-   Il prend uniquement en charge les types de média avec les formats [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .
-   Sa valeur est plus élevée, ce qui lui permet d’être ajouté automatiquement à un graphique de filtre.

le Mixer de superposition 2 est fourni afin que le gestionnaire de Graph de filtre l’ajoute au graphique lors du rendu d’une vidéo MPEG-2 non DVD. le choix entre l’utilisation de la superposition Mixer ou la superposition Mixer 2 est géré par le composant qui génère le graphique, à savoir le gestionnaire de Graph de filtre, le générateur de Graph de Capture ou le générateur de Graph DVD. Du point de vue de l’application, il s’agit du même filtre, avec les mêmes interfaces et fonctionnalités.

le tableau suivant contient des informations spécifiques à la superposition Mixer 2. Pour toutes les autres données de filtre, reportez-vous à la documentation de la Mixer de superposition.




| Étiquette | Valeur |
|--------|-------|
| Types de média de broche d’entrée | Type de format : Format_VIDEOINFO2 | 
| CLSID du filtre | CLSID_OverlayMixer2 | 
| <a href="merit.md">Mérite</a> | <ul><li>MERIT_UNLIKELY</li><li>Windows Vista ou version ultérieure : MERIT_DO_NOT_USE</li></ul> | 




 

dans Windows Vista ou version ultérieure, le mérite du filtre de superposition Mixer 2 n’est \_ \_ pas \_ utilisé, car les convertisseurs vidéo les plus récents (vmr-7, vmr-9 et EVR) prennent tous en charge les formats **VIDEOINFOHEADER2** , et il n’est donc pas nécessaire d’utiliser le Mixer de superposition.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 



