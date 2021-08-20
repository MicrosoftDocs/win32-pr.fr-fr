---
title: Extensions de noms de fichiers
description: Extensions de noms de fichiers
ms.assetid: c17bf4e5-b469-45b6-bc22-2b451723d85e
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
ms.openlocfilehash: 6c69c36a5865b3496cf63e8cc08d73b9187f5107b14bf0bbb0d52b462e90c88a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054987"
---
# <a name="file-name-extensions"></a>Extensions de noms de fichiers

il existe des instructions spécifiques pour l’utilisation des extensions de nom de fichier pour Windows les fichiers multimédias. Windows les extensions de nom de métafichier multimédia sont utilisées pour identifier les différents types de fichiers multimédias Windows. Une extension de nom de fichier fournit à un éditeur de logiciels indépendant (ISV) des informations sur les exigences de rendu d’une application qui utilise une extension particulière, et permet aux créateurs de contenu de cibler des types généraux de lecteurs multimédias.

Les règles d’extension de nom de fichier sont répertoriées dans le tableau suivant. Il est recommandé d’utiliser le type MIME d’un fichier, situé dans l’en-tête de fichier, pour l’identification du type de fichier.



| Extension de nom de fichier | type MIME      | le contenu d’un fichier ;                                                                                                                                                                            |
|---------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .wma                | audio/x-ms-WMA | Windows Fichier multimédia avec contenu audio uniquement. Généralement utilisé pour télécharger et lire des fichiers ou pour diffuser du contenu en continu.                                                                             |
| .wmv                | vidéo/x-ms-WMV | Windows Fichier multimédia avec du contenu audio et/ou vidéo. Généralement utilisé pour télécharger et lire des fichiers ou pour diffuser du contenu en continu.                                                                     |
| .asf                | vidéo/x-ms-asf | Contenu hérité. Généralement utilisé pour télécharger et lire des fichiers ou pour diffuser du contenu en continu. Peut contenir du contenu audio et/ou vidéo. Généralement utilisé pour télécharger et lire des fichiers ou pour diffuser du contenu en continu. |
| . WM                 | vidéo/x-ms-WM  | Réservé                                                                                                                                                                                |
| . Wax                | audio/x-ms-Wax | les sous-fichiers qui référencent Windows fichiers multimédias avec des extensions de nom de fichier. asf,. wma ou. wax.                                                                                             |
| . wvx                | vidéo/x-ms-wvx | les sous-fichiers qui référencent Windows fichiers multimédias avec des extensions de nom de fichier. wma,. wmv,. wvx ou. wax.                                                                                       |
| .asx                | vidéo/x-ms-asf | les sous-fichiers qui référencent Windows fichiers multimédias avec des extensions de nom de fichier. wma,. wax,. wmv,. wvx,. asf ou. asx.                                                                           |
| . WMX                | vidéo/x-ms-wvx | Réservé.                                                                                                                                                                               |



 

## <a name="remarks"></a>Remarques

la gestion des scripts et de la gestion des droits numériques (DRM) doit être prise en charge par toute application qui rend Windows fichiers multimédias.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guide du métafichier multimédia**](windows-media-metafile-guide.md)
</dt> <dt>

[**Windows Référence du métafichier multimédia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 




