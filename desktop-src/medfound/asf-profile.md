---
description: Cette rubrique explique comment utiliser des profils ASF dans Microsoft Media Foundation.
ms.assetid: 03a0981b-29c3-450d-aa58-bc56a76e6cb6
title: Profil ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616670e7de68fd73c168c474544fc6236f1586e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296378"
---
# <a name="asf-profile"></a>Profil ASF

Cette rubrique explique comment utiliser des profils ASF dans Microsoft Media Foundation.

Un fichier ASF (Advanced Systems Format) contient un ou plusieurs flux. Pour chaque flux, l’en-tête ASF contient un en-tête de propriétés de flux qui décrit le flux. Au niveau de la couche [WMContainer](wmcontainer-asf-components.md) , les objets suivants sont utilisés pour définir ou lire les propriétés des flux ASF :

-   Objet *Profil ASF* : décrit les flux et leurs relations entre eux. L’objet profil ASF expose l’interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .
-   Objet de *configuration de flux* : décrit un flux. L’objet de configuration de flux contient un type de média qui décrit le format du flux. Pour les flux audio et vidéo, le type de média décrit exactement comment le flux est configuré et est utilisé par les codecs qui encodent ou décodent le flux. L’objet de configuration de flux expose l’interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) . Un profil ASF valide contient au moins un objet de configuration de flux.
-   Objet d' *exclusion mutuelle* : décrit plusieurs flux qui ne sont pas destinés à être lus simultanément. Un objet d’exclusion mutuelle expose l’interface [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) . Un profil ASF contient zéro ou plusieurs objets d’exclusion mutuelle.

Le diagramme suivant montre la relation entre le profil ASF et les objets contenus dans le profil.

![diagramme arborescent d’un nœud de profil ASF avec des nœuds enfants de configuration de flux ; le premier point vers le type de média, les deux à l’exclusion mutuelle suivante](images/asf-components02.png)

Pour la lecture, le profil ASF est utilisé pour énumérer les flux et rechercher les formats de flux. Pour l’encodage, le profil ASF est utilisé pour configurer les flux dans le fichier de destination.

Le profil ASF est également utilisé pour configurer le [récepteur de média ASF](asf-media-sinks.md). Pour chaque flux du profil ASF, le récepteur multimédia ASF crée un récepteur de flux correspondant.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                           | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Création d’un profil ASF](creating-an-asf-profile.md)<br/>                               | Décrit comment créer un objet de profil ASF.<br/>          |
| [Création et configuration d’Flux ASF](creating-and-configuring-asf-streams.md)<br/>     | Décrit comment ajouter des flux à un profil ASF.<br/>         |
| [Utilisation de l’exclusion mutuelle pour les Flux ASF](using-mutual-exclusion-for-asf-streams.md)<br/> | Décrit comment ajouter des exclusions mutuelles à des flux ASF. <br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de médias](media-types.md)
</dt> <dt>

[didacticiel : encodage de média de Windows Pass](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[Didacticiel : écriture d’un fichier WMA à l’aide de l’encodage CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> <dt>

[Composants WMContainer ASF](wmcontainer-asf-components.md)
</dt> </dl>

 

 




