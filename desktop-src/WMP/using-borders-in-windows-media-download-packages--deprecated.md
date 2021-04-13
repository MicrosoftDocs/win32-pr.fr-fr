---
title: Utilisation des bordures dans les packages de téléchargement Windows Media (déconseillés)
description: Utilisation des bordures dans les packages de téléchargement Windows Media (déconseillés)
ms.assetid: d3961c5f-8cce-439d-9a13-41be2f45d92c
keywords:
- Fichiers Windows Media, packages de téléchargement Windows Media
- Windows Media Player, packages de téléchargement Windows Media
- sous-fichiers, packages de téléchargement Windows Media
- Windows Media, packages de téléchargement Windows Media
- bordures, à propos de
- Packages de téléchargement Windows Media, bordures
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 87f7d0fec341bb79bfe9b8dd739b63a9ba3a66ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380031"
---
# <a name="using-borders-in-windows-media-download-packages-deprecated"></a>Utilisation des bordures dans les packages de téléchargement Windows Media (déconseillés)

Cette page décrit une fonctionnalité qui peut ne pas être disponible dans les versions ultérieures du lecteur Windows Media et du kit de développement logiciel (SDK) du lecteur Windows Media.

Les bordures vous permettent de créer une interface utilisateur graphique personnalisée pour votre contenu empaqueté. La bordure peut inclure des éléments tels que des images, des contrôles interactifs et des liens vers des sites Web. Vous pouvez utiliser des bordures dans les cas où vous souhaitez ajouter de la valeur supplémentaire à votre contenu empaqueté, par exemple pour la personnalisation ou la publicité. Une fois que les utilisateurs ont téléchargé et ouvert votre package de téléchargement Windows Media, le lecteur Windows Media affiche automatiquement votre bordure personnalisée quand il lit le contenu empaqueté.

Contrairement à une apparence, qui permet aux utilisateurs de remplacer complètement l’interface utilisateur du lecteur Windows Media, une bordure s’affiche uniquement dans le volet de **lecture** en cours du lecteur en mode complet. Toutefois, les outils et les technologies que vous utilisez pour créer des apparences sont également utilisés pour créer des bordures. L’illustration suivante montre une bordure.

![une bordure affiche le lecteur Windows Media 10](images/border-v10.png)

Il est important de comprendre les techniques de base pour créer une apparence avant de tenter de créer une bordure. La programmation des bordures s’effectue à l’aide de deux langages de programmation : Extensible Markup Language (XML) et Microsoft JScript. XML est utilisé pour définir des éléments d’interface tels que des boutons, des curseurs et des zones de texte. Vous n’avez pas besoin de comprendre tous les détails du XML, car vous n’avez pas à écrire de nouveaux éléments de code XML. vous pouvez simplement utiliser ceux fournis par le lecteur Windows Media. Même si JScript n’est pas requis pour la création de bordures, il peut être utilisé pour fournir des fonctionnalités supplémentaires.

Un fichier de bordure compressé avec une extension de nom de fichier. WMZ comprend un fichier de définition de bordure avec une extension de nom de fichier. WMS et tous les fichiers image utilisés dans la bordure.

Pour inclure une bordure dans un package de téléchargement Windows Media, il vous suffit de créer une bordure et de faire référence à cette bordure dans une sélection de métafichiers Windows Media. Le fichier de bordure est chargé dans le lecteur Windows Media une fois que le lecteur a analysé le métafichier et interprète l’élément d' **apparence** qui fait référence à la bordure. L’élément **Skin** est utilisé uniquement pour les bordures, et l’attribut href de l’élément **Skin** ne peut faire référence qu’à une seule apparence pour chaque package.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Bordures du lecteur Windows Media (déconseillée)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Packages de téléchargement Windows Media (déconseillés)**](windows-media-download-packages--deprecated.md)
</dt> <dt>

[**Apparences du lecteur Windows Media**](windows-media-player-skins.md)
</dt> </dl>

 

 




