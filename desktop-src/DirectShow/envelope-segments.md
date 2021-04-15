---
description: Segments d’enveloppe
ms.assetid: 1b59cd1c-7c37-4c70-a36c-2ee1f42b42c5
title: Segments d’enveloppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bac997667f52ef9bbf14760584889fa16cbbd04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521636"
---
# <a name="envelope-segments"></a>Segments d’enveloppe

Une courbe de paramètres se compose d’un ou de plusieurs segments d’enveloppe, définis à l’aide de la structure de [**\_ \_ segment d’enveloppe MP**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) . Cette structure contient les informations suivantes :

-   Heures de début et de fin.
-   Valeurs de début et de fin.
-   Le type de courbe (linéaire, carré, etc.).
-   Indicateurs facultatifs, décrits dans un instant.

Le client ajoute des segments d’enveloppe à un paramètre en appelant la méthode [**IMediaParams :: AddEnvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) et en passant un tableau de structures de **\_ \_ segment d’enveloppe MP** . Le client doit trier les segments dans l’ordre chronologique croissant avant d’appeler la méthode. Au fur et à mesure que DMO traite les données, vous pouvez imaginer le paramètre en déplacement sur chaque segment d’enveloppe, par exemple une voiture qui se dirige sur une série de collines. La méthode [**IMediaParams :: GetParam**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam) retourne la valeur la plus récente.

Deux segments adjacents peuvent avoir un intervalle entre eux. Pendant les lacunes, le paramètre conserve sa valeur précédente, comme suit :

-   Avant le premier segment, la valeur est la valeur neutre.
-   Entre les segments, la valeur est la valeur de fin du segment précédent.
-   Après le dernier segment, la valeur reste à la valeur de fin de ce segment.
-   Si le client vide le DMO, la valeur est rétablie à la valeur neutre.

Vous pouvez modifier un segment en définissant l’un des indicateurs suivants :

-   MPF \_ ENVLP \_ Begin \_ CURRENTVAL. DMO utilise la valeur la plus récente du paramètre comme valeur de départ du segment. Il peut s’agir de la valeur neutre ou de la valeur de fin du segment précédent. DMO ignore le membre **valStart** de la structure **du \_ \_ segment d’enveloppe MP** .
-   MPF \_ ENVLP \_ Begin \_ NEUTRALVAL. DMO utilise la valeur neutre du paramètre comme valeur de départ du segment. Elle ignore **valStart**.

Vous pouvez considérer ces indicateurs comme saisissant le point de départ du segment et le déplacer vers le haut ou vers le haut, tandis que la valeur de fin reste fixe. Le segment est « stretch » en conséquence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres de média](media-parameters.md)
</dt> </dl>

 

 



