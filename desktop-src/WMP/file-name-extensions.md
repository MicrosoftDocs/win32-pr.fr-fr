---
title: Extensions de noms de fichiers
description: Extensions de noms de fichiers
ms.assetid: c17bf4e5-b469-45b6-bc22-2b451723d85e
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
ms.openlocfilehash: d95d5bcba9bbad5f04b0d085ba712d5b9306c8b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509401"
---
# <a name="file-name-extensions"></a>Extensions de noms de fichiers

Il existe des instructions spécifiques pour l’utilisation des extensions de nom de fichier pour les fichiers Windows Media. Les extensions de nom de métafichier Windows Media sont utilisées pour identifier les différents types de fichiers Windows Media. Une extension de nom de fichier fournit à un éditeur de logiciels indépendant (ISV) des informations sur les exigences de rendu d’une application qui utilise une extension particulière, et permet aux créateurs de contenu de cibler des types généraux de lecteurs multimédias.

Les règles d’extension de nom de fichier sont répertoriées dans le tableau suivant. Il est recommandé d’utiliser le type MIME d’un fichier, situé dans l’en-tête de fichier, pour l’identification du type de fichier.



| Extension de nom de fichier | type MIME      | le contenu d’un fichier ;                                                                                                                                                                            |
|---------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .wma                | audio/x-ms-WMA | Fichier Windows Media avec contenu audio uniquement. Généralement utilisé pour télécharger et lire des fichiers ou pour diffuser du contenu en continu.                                                                             |
| .wmv                | vidéo/x-ms-WMV | Fichier Windows Media avec du contenu audio et/ou vidéo. Généralement utilisé pour télécharger et lire des fichiers ou pour diffuser du contenu en continu.                                                                     |
| .asf                | vidéo/x-ms-asf | Contenu hérité. Généralement utilisé pour télécharger et lire des fichiers ou pour diffuser du contenu en continu. Peut contenir du contenu audio et/ou vidéo. Généralement utilisé pour télécharger et lire des fichiers ou pour diffuser du contenu en continu. |
| . WM                 | vidéo/x-ms-WM  | Réservé                                                                                                                                                                                |
| . Wax                | audio/x-ms-Wax | Les sous-fichiers qui font référence à des fichiers Windows Media avec des extensions de nom de fichier. ASF,. WMA ou. Wax.                                                                                             |
| . wvx                | vidéo/x-ms-wvx | Les sous-fichiers qui font référence à des fichiers Windows Media avec des extensions de nom de fichier. WMA,. wmv,. wvx ou. Wax.                                                                                       |
| .asx                | vidéo/x-ms-asf | Les sous-fichiers qui font référence à des fichiers Windows Media avec des extensions de nom de fichier. WMA,. Wax,. wmv,. wvx,. ASF ou. asx.                                                                           |
| . WMX                | vidéo/x-ms-wvx | Réservé.                                                                                                                                                                               |



 

## <a name="remarks"></a>Notes

La gestion des scripts et de la gestion des droits numériques (DRM) doit être prise en charge par toutes les applications qui affichent des fichiers Windows Media.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guide des métafichiers Windows Media**](windows-media-metafile-guide.md)
</dt> <dt>

[**Informations de référence sur les métafichiers Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 




