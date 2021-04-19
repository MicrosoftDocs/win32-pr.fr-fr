---
description: Filtre de mixage de superposition 2
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: Filtre de mixage de superposition 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22976a58b272cf04c098c102d32d154e361b8b9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544556"
---
# <a name="overlay-mixer-2-filter"></a>Filtre de mixage de superposition 2

Le filtre de mixage de superposition 2 est identique au filtre de [mixage de superposition](overlay-mixer-filter.md) , sauf :

-   Il prend uniquement en charge les types de média avec les formats [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .
-   Sa valeur est plus élevée, ce qui lui permet d’être ajouté automatiquement à un graphique de filtre.

Le mélangeur de superposition 2 est fourni afin que le gestionnaire de graphes de filtre l’ajoute au graphique lors du rendu d’une vidéo MPEG-2 non DVD. La possibilité d’utiliser le mélangeur de superposition ou le mélangeur de superposition 2 est gérée par le composant qui génère le graphique, soit le gestionnaire de graphes de filtre, le générateur de graphiques de capture ou le générateur de graphiques de DVD. Du point de vue de l’application, il s’agit du même filtre, avec les mêmes interfaces et fonctionnalités.

Le tableau suivant contient des informations spécifiques au mélangeur de superposition 2. Pour toutes les autres données de filtre, reportez-vous à la documentation du mélangeur de superposition.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Types de média de broche d’entrée</td>
<td>Type de format : Format_VIDEOINFO2</td>
</tr>
<tr class="even">
<td>CLSID du filtre</td>
<td>CLSID_OverlayMixer2</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Mérite</a></td>
<td><ul>
<li>MERIT_UNLIKELY</li>
<li>Windows Vista ou version ultérieure : MERIT_DO_NOT_USE</li>
</ul></td>
</tr>
</tbody>
</table>



 

Dans Windows Vista ou version ultérieure, les mérites du filtre de mixage de superposition 2 méritent de \_ ne \_ pas \_ être utilisés, car les convertisseurs vidéo plus récents (VMR-7, VMR-9 et EVR) prennent tous en charge les formats **VIDEOINFOHEADER2** , et il n’est donc pas nécessaire d’utiliser le mélangeur de superposition.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 



