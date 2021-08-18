---
description: À propos du contrôle du taux
ms.assetid: 509b2cc8-6017-41a9-ae80-9af21dce9367
title: À propos du contrôle du taux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61ae8ad5bcfaaf415c888418a7a6bd5d77f72434150e30fcac071d078b8ee6d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035657"
---
# <a name="about-rate-control"></a>À propos du contrôle du taux

Dans Media Foundation, la *Vitesse* de lecture est exprimée sous la forme du rapport entre le taux de lecture actuel et le taux de lecture normal. Par exemple, un taux de 2,0 est de deux fois la vitesse normale et 0,5 à une vitesse normale. Les valeurs négatives indiquent une lecture inversée. Un taux de lecture de-2,0 est lu en arrière dans le flux à deux reprises à la vitesse normale. Un taux de zéro provoque le rendu d’une trame ; Après cela, l’horloge de la présentation n’avance pas. Pour obtenir une autre image au taux de zéro, l’application doit rechercher une nouvelle position.

Les applications utilisent les interfaces suivantes pour contrôler la vitesse de lecture.

-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport). Utilisé pour déterminer les taux de lecture les plus rapides et les plus lents possibles.
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol). Utilisé pour modifier la vitesse de lecture.

Pour accéder à ces deux interfaces, appelez [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sur la session multimédia. L’identificateur de service est le \_ service de contrôle de taux MF \_ \_ .

En utilisant le service de contrôle de la fréquence, une application peut implémenter une lecture rapide et en avance rapide.

## <a name="thinning"></a>Éclaircir

La *réduction est un* processus qui réduit le nombre d’échantillons dans un flux, afin de réduire la vitesse de transmission globale. Pour la vidéo, l’affinage s’effectue généralement en supprimant les images Delta et en ne livrant que les images clés. Souvent, le pipeline peut prendre en charge des vitesses de lecture plus rapides à l’aide de la lecture fine, car la vitesse des données est inférieure, car les images delta ne sont pas décodées.

L’affinage ne modifie pas les horodatages ou les durées sur les échantillons. Par exemple, si la vitesse nominale du flux vidéo est de 25 images par seconde, la durée de chaque image est toujours marquée comme 40 millisecondes, même si la source du média supprime toutes les images Delta. Cela signifie qu’il y aura un intervalle de temps entre la fin d’une image et le début de la suivante.

## <a name="scrubbing"></a>Nettoyage

Le *nettoyage* est le processus qui consiste à rechercher instantanément des points spécifiques dans le flux en interagissant avec une barre de défilement, une chronologie ou une autre représentation visuelle du temps. Le terme vient de l’ère des lecteurs de bandes ENROULES sur bande lorsqu’il s’agit de faire basculer une bande vers l’avant pour localiser une section, comme le nettoyage de la tête de lecture avec la bande.

Le nettoyage est implémenté dans Media Foundation en affectant à la vitesse de lecture la valeur zéro. Pour plus d’informations, consultez [Comment effectuer un nettoyage](how-to-perform-scrubbing.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôle de la fréquence](rate-control.md)
</dt> <dt>

[recherche, Avance rapide et la lecture inversée](seeking--fast-forward--and-reverse-play.md)
</dt> <dt>

[Interfaces de service](service-interfaces.md)
</dt> </dl>

 

 



