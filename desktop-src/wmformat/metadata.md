---
title: Métadonnées
description: Dans le cadre de ce kit de développement logiciel (SDK), les métadonnées sont des informations qui décrivent un fichier ASF ou le contenu du fichier.
ms.assetid: 4ccca0c3-52c5-4291-bdab-354705db9b10
keywords:
- Windows Media Format SDK, vue d’ensemble des métadonnées
- ASF (Advanced Systems Format), vue d’ensemble des métadonnées
- ASF (format des systèmes avancés), vue d’ensemble des métadonnées
- métadonnées, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552e968ab4a5908ec1a2a80012ecba3a5b959c6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311251"
---
# <a name="metadata"></a>Métadonnées

Dans le cadre de ce kit de développement logiciel (SDK), les métadonnées sont des informations qui décrivent un fichier ASF ou le contenu du fichier. La section d’en-tête d’un fichier ASF contient toutes les métadonnées associées à ce fichier. Les éléments de métadonnées d’un fichier ASF sont appelés attributs. Chaque attribut a un nom et une valeur. Tout au long de cette documentation, les constantes globales sont utilisées pour identifier les attributs. Par exemple, le titre d’un fichier ASF est stocké dans l’attribut **g \_ wszWMTitle** .

Un certain nombre d’attributs sont définis dans le kit de développement logiciel (SDK) Windows Media format pour gérer les métadonnées les plus courantes. En outre, vous pouvez créer vos propres attributs. Toutefois, lorsque vous nommez des attributs personnalisés, vous devez être prudent, car d’autres développeurs d’applications peuvent utiliser les mêmes noms et des conflits peuvent se produire.

Certains attributs sont définis par le kit de développement logiciel (SDK) et ne peuvent pas être modifiés manuellement. Par exemple, lorsque vous indexez un fichier ASF, le kit de développement logiciel (SDK) définit l’attribut **g \_ wszWMSeekable** pour indiquer que le fichier peut désormais être lu à partir de n’importe quel point spécifié.

D’autres attributs sont purement informatifs et doivent être définis manuellement. Par exemple, si vous souhaitez effectuer le suivi de l’auteur d’un fichier, vous devez définir **g \_ wszWMAuthor**.

Le kit de développement logiciel (SDK) Windows Media format prend en charge les attributs qui s’appliquent à l’ensemble du fichier, ainsi que les attributs qui s’appliquent aux flux individuels.

Vous pouvez utiliser le kit de développement logiciel (SDK) de format Windows Media pour modifier les métadonnées dans les fichiers MP3, même si vous devez toujours utiliser des attributs conformes à ID3 dans des fichiers MP3 pour maintenir la compatibilité avec d’autres programmes de manipulation MP3.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Concepts**](concepts.md)
</dt> <dt>

[**Éditeur de métadonnées, objet**](metadata-editor-object.md)
</dt> <dt>

[**Fonctionnalités de métadonnées**](metadata-features.md)
</dt> <dt>

[**Utilisation des métadonnées**](working-with-metadata.md)
</dt> </dl>

 

 




