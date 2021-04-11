---
title: Bordures du lecteur Windows Media (déconseillée)
description: Bordures du lecteur Windows Media (déconseillée)
ms.assetid: defa461b-ffa5-4fee-bed4-aba3e733b8c4
keywords:
- Windows Media Player, bordures
- Apparences du lecteur Windows Media, bordures
- apparences, bordures
- bordures, comparaison avec les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a48ff3ec17230002e9c6b4a1eb17e3024375a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309982"
---
# <a name="borders-for-windows-media-player-deprecated"></a>Bordures du lecteur Windows Media (déconseillée)

Cette page décrit une fonctionnalité qui peut ne pas être disponible dans les versions ultérieures du lecteur Windows Media et du kit de développement logiciel (SDK) du lecteur Windows Media.

Une bordure est similaire à une apparence, mais au lieu de remplacer l’interface utilisateur pour le mode compact du lecteur Windows Media, une bordure est incorporée dans le volet de lecture en cours du lecteur Windows Media en mode plein.

À l’aide d’un package de téléchargement Windows Media, vous pouvez inclure du contenu avec une bordure, ce qui vous permet de reformer les applications multimédias.

Un exemple de package de téléchargement Windows Media incluant une bordure et du contenu incorporé est inclus dans le répertoire d’exemples de ce kit de développement logiciel (SDK).

## <a name="creating-a-border"></a>Création d’une bordure

Une bordure est créée de la même façon qu’une apparence. La seule différence est que l’apparence est incorporée dans le volet **Playing Now** . Cela signifie que la taille de l’apparence ne peut pas être calculée et que tous les éléments d’apparence doivent être relatifs. Si l’utilisateur redimensionne le lecteur Windows Media, certaines parties de la bordure peuvent être découpées et invisibles.

## <a name="loading-a-border"></a>Chargement d’une bordure

Une bordure est chargée lorsqu’un métafichier Windows Media qui utilise l’élément d' **apparence** est chargé. L’attribut **href** de l’élément **Skin** doit faire référence à une apparence. Un élément d' **apparence** typique ressemble à ceci :


```C++
<SKIN HREF="myborder.wmz">

```



Pour plus d’informations, consultez [élément Skin (déconseillé)](skin-element--deprecated.md).

## <a name="including-content-with-a-border"></a>Inclusion de contenu avec une bordure

Vous pouvez inclure du contenu avec une bordure à l’aide d’un fichier de téléchargement Windows Media (avec l’extension de nom de fichier. WMD). Suivez ces étapes :

1.  Créez la bordure. Veillez à la créer de telle sorte que le redimensionnement ne supprimera pas la composition de la bordure. Par exemple, n’incluez pas de fichier d’arrière-plan ; rendre l’arrière-plan transparent pour qu’une visualisation puisse s’exécuter derrière.
2.  Compressez le contenu de l’apparence (art, fichiers JScript et fichier de définition d’apparence) dans un fichier portant l’extension de nom de fichier. WMZ.
3.  Créez un métafichier Windows Media (avec une extension de nom de fichier. asx) qui fait référence au fichier de bordure compressé (avec l’extension de nom de fichier. WMZ). Le métafichier peut inclure des informations de sélection avec les métadonnées de l’art et des URL pour du contenu spécifique.
4.  Assemblez le contenu multimédia numérique.
5.  Compressez la bordure, le métafichier et le contenu dans un seul fichier et attribuez-lui une extension de nom de fichier. WMD.

## <a name="using-a-border"></a>Utilisation d’une bordure

Une fois que vous avez créé le fichier de téléchargement Windows Media, il suffit de double-cliquer dessus pour l’utilisateur. Le fichier sera téléchargé sur l’ordinateur de l’utilisateur. Les fichiers à l’intérieur du package seront décompressés, la sélection sera ajoutée aux playlists, la bordure apparaîtra dans le volet de **lecture** en cours du lecteur Windows Media en mode plein et le premier élément de la nouvelle sélection commencera à s’exécuter.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des apparences**](about-skins.md)
</dt> <dt>

[**Exemples**](samples.md)
</dt> <dt>

[**Packages de téléchargement Windows Media (déconseillés)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




