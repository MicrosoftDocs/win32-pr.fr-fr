---
title: bordures pour la Lecteur Windows Media (déconseillée)
description: bordures pour la Lecteur Windows Media (déconseillée)
ms.assetid: defa461b-ffa5-4fee-bed4-aba3e733b8c4
keywords:
- Lecteur Windows Media, bordures
- habillages Lecteur Windows Media, bordures
- apparences, bordures
- bordures, comparaison avec les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32e16fa6e334c5c47f24feadc777b82cee1a12477211bc4e613d22e8fdc4521
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123849"
---
# <a name="borders-for-windows-media-player-deprecated"></a>bordures pour la Lecteur Windows Media (déconseillée)

cette page documente une fonctionnalité qui peut ne pas être disponible dans les futures versions de Lecteur Windows Media et le kit de développement logiciel (SDK) Lecteur Windows Media.

une bordure est similaire à une apparence, mais au lieu de remplacer l’interface utilisateur pour le mode compact de Lecteur Windows Media, une bordure est incorporée dans le volet de diffusion en cours du Lecteur Windows Media en mode complet.

à l’aide d’un package Windows Media Download, vous pouvez inclure du contenu avec une bordure, ce qui vous permet de reformer les applications multimédias.

un exemple Windows package de téléchargement multimédia qui inclut une bordure et du contenu incorporé est inclus dans le répertoire d’exemples de ce kit de développement logiciel (SDK).

## <a name="creating-a-border"></a>Création d’une bordure

Une bordure est créée de la même façon qu’une apparence. La seule différence est que l’apparence est incorporée dans le volet **Playing Now** . Cela signifie que la taille de l’apparence ne peut pas être calculée et que tous les éléments d’apparence doivent être relatifs. si l’utilisateur redimensionne Lecteur Windows Media, certaines parties de la bordure peuvent être découpées et invisibles.

## <a name="loading-a-border"></a>Chargement d’une bordure

une bordure est chargée lorsqu’un Windows métafichier multimédia qui utilise l’élément d' **apparence** est chargé. L’attribut **href** de l’élément **Skin** doit faire référence à une apparence. Un élément d' **apparence** typique ressemble à ceci :


```C++
<SKIN HREF="myborder.wmz">

```



Pour plus d’informations, consultez [élément Skin (déconseillé)](skin-element--deprecated.md).

## <a name="including-content-with-a-border"></a>Inclusion de contenu avec une bordure

vous pouvez inclure du contenu avec une bordure à l’aide d’un fichier de téléchargement Windows Media (avec l’extension de nom de fichier. wmd). Procédez comme suit :

1.  Créez la bordure. Veillez à la créer de telle sorte que le redimensionnement ne supprimera pas la composition de la bordure. Par exemple, n’incluez pas de fichier d’arrière-plan ; rendre l’arrière-plan transparent pour qu’une visualisation puisse s’exécuter derrière.
2.  compressez le contenu de l’apparence (art, JScript fichiers et le fichier de définition d’apparence) dans un fichier avec l’extension de nom de fichier. wmz.
3.  créez un métafichier Windows Media (avec une extension de nom de fichier. asx) qui fait référence au fichier de bordure compressé (avec l’extension de nom de fichier. wmz). Le métafichier peut inclure des informations de sélection avec les métadonnées de l’art et des URL pour du contenu spécifique.
4.  Assemblez le contenu multimédia numérique.
5.  Compressez la bordure, le métafichier et le contenu dans un seul fichier et attribuez-lui une extension de nom de fichier. WMD.

## <a name="using-a-border"></a>Utilisation d’une bordure

une fois que vous avez créé le fichier Windows Media Download, il suffit de double-cliquer dessus pour l’utilisateur. Le fichier sera téléchargé sur l’ordinateur de l’utilisateur. les fichiers à l’intérieur du package seront décompressés, la sélection sera ajoutée aux sélections, la bordure s’affichera dans le volet de **lecture** en cours du Lecteur Windows Media en mode complet, et le premier élément de la nouvelle sélection commencera à être lu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des apparences**](about-skins.md)
</dt> <dt>

[**Exemples**](samples.md)
</dt> <dt>

[**Windows Packages de téléchargement de médias (déconseillés)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




