---
title: Types d’affichages de texte
description: Types d’affichages de texte
ms.assetid: 6aa3fc89-e5f5-420f-82e0-c605676078cb
keywords:
- Lecteur Windows Media Skins mobiles, texte
- texte dans les apparences, types d’affichage
- apparences, texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01826f35db0d3877a3ecd34c351315872760b1b9b0713a36955bb3161ed6ba8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134602"
---
# <a name="text-display-types"></a>Types d’affichages de texte

Vous n’avez pas besoin d’inclure des affichages de texte dans votre apparence, mais il existe de nombreuses instances où vous pouvez souhaiter. Par exemple, vous pouvez inclure un TrackBar de recherche pour permettre à l’utilisateur de se déplacer vers n’importe quelle position dans l’élément multimédia, mais vous pouvez également inclure un affichage de texte qui indique le nombre de secondes qui se sont écoulées depuis le début de la diffusion de l’élément multimédia actuel.

**Zones d’affichage**

Voici plusieurs attributs pouvant être affichés par un élément de texte :

-   Temps
-   Sélection
-   Assurer\#
-   \#Musique
-   Intitulé
-   Auteur
-   copyright
-   Nom de fichier
-   FilenameExt
-   Bitrate
-   Fréquence
-   Statut
-   VolPercent

Pour plus d’informations sur les types d’affichage de texte, consultez la section de [texte](text.md) de la référence d’apparence.

**Défilement du texte**

En plus d’utiliser des éléments de texte individuels, vous pouvez combiner un ou plusieurs attributs dans un texte défilant. Cela est utile si vous souhaitez afficher un regroupement d’informations textuelles associées dans une petite zone. Par exemple, vous pouvez afficher le titre, l’auteur et les informations de copyright dans un texte défilant.

Pour plus d’informations sur la création d’un texte défilant, consultez la section [Marquee](marquee.md) de la référence de l’apparence.

**Affichage de l’État**

L’affichage de l’État est un autre type d’affichage de texte. cela vous permet d’afficher automatiquement les informations relatives à l’état actuel de Lecteur Windows Media Mobile. Par exemple, l’affichage de l’état indique à l’utilisateur quand un élément multimédia est mis en mémoire tampon, de sorte qu’il est évident que le lecteur fonctionne.

Les messages suivants s’affichent dans l’affichage de l’État :

-   des réponses
-   Connecting
-   Suspendu
-   Lecture en cours
-   Ready
-   Arrêté

> [!Note]  
> Lorsqu’un élément multimédia est lu, l’affichage de l’État pivote dans le sous-titre, l’artiste, l’album, le genre et la vitesse de transmission actuelle.

 

Pour plus d’informations sur la création d’un affichage d’État à l’aide de l’élément Status, consultez la section [Status](status.md) de la référence Skin. Toutefois, il est préférable d’utiliser l’attribut Status dans l’élément Text au lieu de l’élément Status.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecteur Windows Media Fonctionnalités mobiles**](windows-media-player-mobile-functionality.md)
</dt> </dl>

 

 




