---
title: Création d’un package de téléchargement Windows Media (déconseillé)
description: Création d’un package de téléchargement Windows Media (déconseillé)
ms.assetid: 95d6a214-9da6-496d-ba40-4476814b1d5a
keywords:
- Fichiers Windows Media, packages de téléchargement Windows Media
- Windows Media Player, packages de téléchargement Windows Media
- sous-fichiers, packages de téléchargement Windows Media
- Windows Media, packages de téléchargement Windows Media
- Packages de téléchargement Windows Media, création
- création de packages de téléchargement Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a8716e1783f0e00cb561c3aba1d15a2c3e5b147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029416"
---
# <a name="creating-a-windows-media-download-package-deprecated"></a>Création d’un package de téléchargement Windows Media (déconseillé)

Cette page décrit une fonctionnalité qui peut ne pas être disponible dans les versions ultérieures du lecteur Windows Media et du kit de développement logiciel (SDK) du lecteur Windows Media.

Pour créer un package de téléchargement Windows Media, procédez comme suit.

1.  **Créer une bordure.** Utilisez les mêmes techniques que celles que vous utiliseriez pour créer une apparence pour le lecteur Windows Media. Concevez la bordure afin que le redimensionnement du lecteur Windows Media ne supprimera pas la composition des éléments de la bordure. Par exemple, utilisez une couleur unie ou une visualisation comme arrière-plan, car celles-ci sont mises à l’échelle et le lecteur Windows Media est redimensionné.
2.  **Compresser le contenu de la bordure.** Créez un dossier compressé (avec l’extension de nom de fichier. zip) qui contient les fichiers de bordure : images, fichiers JScript et fichier de définition d’apparence avec une extension de nom de fichier. WMS. Renommez le fichier compressé afin qu’il ait une extension de nom de fichier. WMZ.
3.  **Écrire un métafichier Windows Media.** Le lecteur Windows Media ne chargera pas la bordure, sauf si vous créez un métafichier Windows Media avec une extension de nom de fichier. asx qui implémente l’élément d' **apparence** . Le métafichier peut également être utilisé pour créer une sélection qui décrit le contenu inclus dans le package.
4.  **Assemblez votre contenu.** Placez tous les fichiers que vous souhaitez utiliser dans un dossier. Cela comprend les fichiers audio, les fichiers vidéo, les fichiers de données et les fichiers de définition de bordure.
5.  **Créez le package.** Créez un dossier compressé (avec l’extension de nom de fichier. zip) qui contient le fichier de bordure, les fichiers de contenu et le métafichier. Remplacez l’extension de nom de fichier de ce fichier. zip par une extension de nom de fichier. WMD.
6.  **Publiez le package sur un site Web.** Le package terminé est prêt à être publié sur un site Web et téléchargé par les utilisateurs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Packages de téléchargement Windows Media (déconseillés)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




