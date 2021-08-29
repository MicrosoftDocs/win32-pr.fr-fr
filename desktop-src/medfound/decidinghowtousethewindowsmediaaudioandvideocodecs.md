---
description: Utilisation des objets codec et DSP
ms.assetid: ec571d31-6542-421a-8027-d4c61ce00035
title: Utilisation des objets codec et DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f411c292a9b933ca480e3de053317005b14fa03a0f073b7ecfd3b67f3c4d02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061959"
---
# <a name="using-the-codec-and-dsp-objects"></a>Utilisation des objets codec et DSP

il existe plusieurs façons d’utiliser la Windows Media Audio et les codecs vidéo et dsp pour encoder, décoder ou transformer votre contenu multimédia numérique. le codec Windows Media Audio et vidéo et l’API dsp sont destinés aux utilisateurs qui doivent configurer les objets codec et dsp manuellement ou les utiliser en dehors du contexte de l’un des kits de développement logiciel (sdk) Windows media, tels que le kit de développement logiciel (sdk) Windows media Format ou le kit de développement logiciel (sdk) Media Foundation.

les créateurs de contenu et les utilisateurs finaux peuvent utiliser un large éventail d’outils et d’applications pour encoder du contenu dans des flux de Windows Media Audio ou Windows Media Video. Windows L’encodeur multimédia, par exemple, est spécifiquement conçu pour faciliter le processus d’encodage. de même, Lecteur Windows Media est spécialement conçu pour fonctionner correctement avec les données multimédias numériques qui sont codées dans Windows formats multimédias. pour de nombreuses applications, il suffit d’utiliser le kit de développement logiciel (sdk) Media encoder Windows ou le kit de développement logiciel (sdk) Lecteur Windows Media. En particulier, ces deux technologies conviennent parfaitement aux scénarios qui ressemblent à la fonctionnalité des outils qu’elles automatisent.

si vous avez besoin d’un meilleur contrôle sur le processus d’encodage ou de décodage, mais que vous envisagez d’utiliser le format ASF (Advanced Systems format) comme conteneur pour vos données multimédias, le kit de développement logiciel (SDK) du format multimédia Windows peut être un bon choix. les objets du kit de développement logiciel (SDK) Windows Media Format offrent un framework flexible pour la création de fichiers ASF et offrent une prise en charge intégrée des codecs Windows Media Audio et vidéo.

le kit de développement logiciel (SDK) Media Foundation, qui est nouveau pour Windows Vista, simplifie grandement l’encodage et le décodage en fournissant un pipeline de média personnalisable. Vous pouvez définir les propriétés du média d’entrée et de sortie et le chargeur de topologie Media Foundation configurera les codecs et les DSP nécessaires pour vous.

la raison principale de l’utilisation directe des objets codec est l’utilisation des codecs Windows Media Audio et vidéo en dehors du conteneur ASF. L’utilisation des objets codec et DSP fournit également un niveau de contrôle qui n’est pas disponible à l’aide des technologies les plus abstraites.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Codecs Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



