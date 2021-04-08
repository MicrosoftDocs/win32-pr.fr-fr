---
description: Utilisation du mélangeur de superposition dans la capture vidéo
ms.assetid: 43468fa2-6dea-439d-9e24-f47a053ad561
title: Utilisation du mélangeur de superposition dans la capture vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bff115d566654732e80c0bcb0f554c4ad96e65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034811"
---
# <a name="using-the-overlay-mixer-in-video-capture"></a>Utilisation du mélangeur de superposition dans la capture vidéo

Il existe certains genres de vidéos que le filtre de [convertisseur vidéo](video-renderer-filter.md) ne peut pas afficher par lui-même. Dans ce cas, le convertisseur vidéo doit fonctionner avec le filtre de [mixage de superposition](overlay-mixer-filter.md) . Le mélangeur de superposition gère le rendu, tandis que le convertisseur vidéo gère la fenêtre vidéo. Le mélangeur de superposition est nécessaire dans les situations suivantes :

-   Broches du port vidéo (VP). Si le périphérique de capture utilise un port vidéo, le mélangeur de superpositions gère la superposition matérielle.
-   Vidéo entrelacée. Pour la vidéo entrelacée, le décodeur requiert un format [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , que le convertisseur vidéo ne prend pas en charge.
-   Sous-titres. Le texte de légende est rendu sous forme de bitmaps de 8 bits par pixel, que le mélangeur de superposition recouvre sur la vidéo.

La méthode **RenderStream** du générateur de graphiques de capture insère le mélangeur de superposition chaque fois que nécessaire. Toutefois, si vous générez le graphique sans utiliser le générateur de graphiques de capture, vous devez vérifier chacune de ces situations et insérer vous-même le mélangeur de superposition.

-   \[! Précieuse\]  
    > Si l’appareil possède un code confidentiel de VP, vous devez le connecter même si vous n’avez pas besoin de la fonctionnalité d’aperçu dans votre application. Avec un port vidéo, l’appareil de capture envoie toujours les données vidéo à la superposition matérielle, de sorte que le mélangeur de superposition est toujours nécessaire.

     

Les filtres de convertisseur de mixage vidéo (VMR-7 et VMR-9) prennent tous deux en charge la vidéo entrelacée et peuvent combiner des bitmaps de sous-titres sur la vidéo principale. Si vous utilisez VMR pour ces scénarios, vous n’avez pas besoin d’utiliser le mélangeur de superposition. VMR-9 ne prend pas en charge les connexions à un pin de vice-président. VMR-7 prend en charge les connexions de vice-président via le filtre du gestionnaire de port vidéo. Toutefois, vous constaterez peut-être que certains pilotes ne fonctionnent pas correctement avec le gestionnaire de port vidéo. Pour cette raison, le mélangeur de superposition est toujours recommandé pour les broches du VP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rubriques avancées sur la capture](advanced-capture-topics.md)
</dt> <dt>

[Broches de port vidéo](video-port-pins.md)
</dt> <dt>

[Type de format VideoInfo2](videoinfo2-format-type.md)
</dt> </dl>

 

 



