---
title: Instructions relatives aux extensions de métafichiers
description: Instructions relatives aux extensions de métafichiers
ms.assetid: 079fac31-7a6f-4775-a337-870ad25a56a0
keywords:
- Windows Fichiers multimédias, extensions
- Windows Fichiers multimédias, extensions de nom de fichier
- refichiers, extensions
- sous-fichiers, extensions de nom de fichier
- Windows Médias, sous-fichiers
- extensions de nom de fichier pour Windows les fichiers multimédias
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2793b19576e26096bc30c834666828cf9ed29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008370"
---
# <a name="metafile-extension-guidelines"></a>Instructions relatives aux extensions de métafichiers

Une extension de nom de fichier fournit à un éditeur de logiciels indépendant (ISV) des informations sur les exigences de rendu d’une application qui utilise l’extension et permet aux créateurs de contenu de cibler les types généraux de joueurs.

Windows les extensions de nom de métafichier multimédia sont utilisées pour identifier le format des fichiers multimédias Windows qu’un métafichier référence. Windows Les fichiers multimédias avec des extensions. Wax,. wvx ou. asx avec les extensions. WMA,. wmv et. ASF, respectivement. Tous les sous-fichiers, quelle que soit l’extension de nom de fichier utilisée, comportent la balise d’élément **ASX** au début du fichier avec l’attribut de **version** spécifié.

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

[**Windows Guide du métafichier multimédia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




