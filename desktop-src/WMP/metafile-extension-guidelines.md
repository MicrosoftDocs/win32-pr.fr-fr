---
title: Instructions relatives aux extensions de métafichiers
description: Instructions relatives aux extensions de métafichiers
ms.assetid: 079fac31-7a6f-4775-a337-870ad25a56a0
keywords:
- Fichiers Windows Media, extensions
- Fichiers Windows Media, extensions de nom de fichier
- refichiers, extensions
- sous-fichiers, extensions de nom de fichier
- Windows Media, sous-fichiers
- extensions de nom de fichier pour les fichiers Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2793b19576e26096bc30c834666828cf9ed29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029784"
---
# <a name="metafile-extension-guidelines"></a>Instructions relatives aux extensions de métafichiers

Une extension de nom de fichier fournit à un éditeur de logiciels indépendant (ISV) des informations sur les exigences de rendu d’une application qui utilise l’extension et permet aux créateurs de contenu de cibler les types généraux de joueurs.

Les extensions de nom de métafichier Windows Media sont utilisées pour identifier le format des fichiers Windows Media référencés par un métafichier. Les sous-fichiers Windows Media avec des extensions. Wax,. wvx ou. asx sont respectivement des fichiers de référence. WMA,. wmv et. ASF. Tous les sous-fichiers, quelle que soit l’extension de nom de fichier utilisée, comportent la balise d’élément **ASX** au début du fichier avec l’attribut de **version** spécifié.

Le tableau suivant présente les types de fichiers multimédias référencés par chaque type d’extension de nom de fichier de métafichier. Les colonnes répertorient les extensions de nom de fichier multimédia, les lignes répertorient les extensions de nom de métafichier. Un X dans une colonne indique un type de fichier multimédia qui peut être référencé par une extension de nom de fichier de métafichier particulière.



| Extension | .asf | .wma | .wmv |
|-----------|------|------|------|
| . wvx      | X    | X    | X    |
| . Wax      | X    | X    |      |
| .asx      | X    |      |      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Extensions de noms de fichiers**](file-name-extensions.md)
</dt> <dt>

[**Sélections de métafichiers**](metafile-playlists.md)
</dt> <dt>

[**Guide des métafichiers Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




