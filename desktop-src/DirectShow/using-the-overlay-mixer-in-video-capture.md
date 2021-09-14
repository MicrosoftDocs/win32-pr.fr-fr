---
description: utilisation de la superposition Mixer dans la Capture vidéo
ms.assetid: 43468fa2-6dea-439d-9e24-f47a053ad561
title: utilisation de la superposition Mixer dans la Capture vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bff115d566654732e80c0bcb0f554c4ad96e65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857350"
---
# <a name="using-the-overlay-mixer-in-video-capture"></a>utilisation de la superposition Mixer dans la Capture vidéo

Il existe certains genres de vidéos que le filtre de [convertisseur vidéo](video-renderer-filter.md) ne peut pas afficher par lui-même. dans ce cas, le convertisseur vidéo doit fonctionner avec la [superposition Mixer](overlay-mixer-filter.md) filtre. le Mixer de superposition gère le rendu, tandis que le convertisseur vidéo gère la fenêtre vidéo. le Mixer de superposition est nécessaire dans les situations suivantes :

-   Broches du port vidéo (VP). si le périphérique de capture utilise un port vidéo, le Mixer de superposition gère la superposition matérielle.
-   Vidéo entrelacée. Pour la vidéo entrelacée, le décodeur requiert un format [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , que le convertisseur vidéo ne prend pas en charge.
-   Sous-titres. le texte de légende est rendu sous forme de bitmaps de 8 bits par pixel, que la superposition Mixer recouvre sur la vidéo.

la méthode **RenderStream** de Capture Graph du générateur insère l’Mixer de superposition chaque fois que nécessaire. toutefois, si vous générez le graphique sans utiliser le générateur de Graph de Capture, vous devez vérifier chacune de ces situations et insérer la superposition Mixer vous-même.

-   \[! Précieuse\]  
    > si l’appareil possède un code confidentiel de directeur, vous devez connecter le Mixer de recouvrement, même si vous n’avez pas besoin de la fonctionnalité d’aperçu dans votre application. avec un port vidéo, l’appareil de capture envoie toujours les données vidéo à la superposition matérielle, de sorte que le Mixer de recouvrement est toujours nécessaire.

     

Les filtres de convertisseur de mixage vidéo (VMR-7 et VMR-9) prennent tous deux en charge la vidéo entrelacée et peuvent combiner des bitmaps de sous-titres sur la vidéo principale. Si vous utilisez VMR pour ces scénarios, vous n’avez pas besoin d’utiliser la Mixer de superposition. VMR-9 ne prend pas en charge les connexions à un pin de vice-président. VMR-7 prend en charge les connexions de vice-président via le filtre du gestionnaire de port vidéo. Toutefois, vous constaterez peut-être que certains pilotes ne fonctionnent pas correctement avec le gestionnaire de port vidéo. c’est la raison pour laquelle le Mixer de superposition est toujours recommandé pour les broches du VP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rubriques avancées sur la capture](advanced-capture-topics.md)
</dt> <dt>

[Broches de port vidéo](video-port-pins.md)
</dt> <dt>

[Type de format VideoInfo2](videoinfo2-format-type.md)
</dt> </dl>

 

 



