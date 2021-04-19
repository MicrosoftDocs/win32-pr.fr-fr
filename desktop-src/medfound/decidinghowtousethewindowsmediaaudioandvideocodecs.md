---
description: Utilisation des objets codec et DSP
ms.assetid: ec571d31-6542-421a-8027-d4c61ce00035
title: Utilisation des objets codec et DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a88670298bfc16ca1dc5053cabeb4f4e631c5c47
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106535743"
---
# <a name="using-the-codec-and-dsp-objects"></a>Utilisation des objets codec et DSP

Il existe plusieurs façons d’utiliser la Windows Media Audio et les codecs vidéo et DSP pour encoder, décoder ou transformer votre contenu multimédia numérique. Le codec Windows Media Audio et vidéo et l’API DSP sont destinés aux utilisateurs qui doivent configurer les objets codec et DSP manuellement ou les utiliser en dehors du contexte de l’un des kits de développement logiciel (SDK) Windows Media, tels que le kit de développement logiciel (SDK) Windows Media format ou le kit de développement logiciel (SDK) Media Foundation.

Les créateurs de contenu et les utilisateurs finaux peuvent utiliser un large éventail d’outils et d’applications pour encoder du contenu dans des flux de Windows Media Audio ou Windows Media Video. Windows Media Encoder, par exemple, est spécifiquement conçu pour faciliter le processus d’encodage. De même, le lecteur Windows Media est spécialement conçu pour fonctionner correctement avec les données multimédias numériques qui sont codées dans les formats Windows Media. Pour de nombreuses applications, l’utilisation du kit de développement logiciel (SDK) Windows Media Encoder ou du kit SDK Windows Media Player est tout ce qui est nécessaire. En particulier, ces deux technologies conviennent parfaitement aux scénarios qui ressemblent à la fonctionnalité des outils qu’elles automatisent.

Si vous avez besoin d’un meilleur contrôle sur le processus d’encodage ou de décodage, mais que vous envisagez d’utiliser le format ASF (Advanced Systems Format) comme conteneur pour vos données multimédias, le kit de développement logiciel (SDK) du format Windows Media peut être un bon choix. Les objets du kit de développement logiciel (SDK) du format Windows Media offrent une infrastructure flexible pour la création de fichiers ASF et offrent une prise en charge intégrée des codecs vidéo et Windows Media Audio.

Le kit de développement logiciel (SDK) Media Foundation, qui est nouveau pour Windows Vista, simplifie grandement l’encodage et le décodage en fournissant un pipeline de média personnalisable. Vous pouvez définir les propriétés du média d’entrée et de sortie et le chargeur de topologie Media Foundation configurera les codecs et les DSP nécessaires pour vous.

La raison principale de l’utilisation directe des objets codec est l’utilisation des codecs Windows Media Audio et vidéo en dehors du conteneur ASF. L’utilisation des objets codec et DSP fournit également un niveau de contrôle qui n’est pas disponible à l’aide des technologies les plus abstraites.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Codecs Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



