---
title: À propos des plug-ins de conversion
description: À propos des plug-ins de conversion
ms.assetid: bd6d1020-e8e1-492e-9c76-9f3cf04190de
keywords:
- Lecteur Windows Media, plug-ins de conversion
- Plug-ins du lecteur Windows Media, conversion
- plug-ins, conversion
- plug-ins de conversion, à propos de
- ASF (Advanced Systems Format)
- ASF (format avancé des systèmes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada6e2a8fa41b657a593dc03082f871503b53eba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671569"
---
# <a name="about-conversion-plug-ins"></a>À propos des plug-ins de conversion

Vous pouvez créer un plug-in de lecteur Windows Media pour convertir des fichiers multimédias numériques créés à l’aide de technologies non fournies par Microsoft, au format ASF (Advanced Systems Format).

Les plug-ins de conversion sont des objets COM (Component Object Model) qui sont empaquetés et distribués en tant que fichiers exécutables (. exe). Le lecteur Windows Media instancie les plug-ins de conversion pour convertir des formats multimédias numériques tiers dans les scénarios suivants :

-   Le contenu multimédia numérique est copié sur l’ordinateur à partir d’un appareil mobile.
-   Le contenu multimédia numérique est ajouté à la bibliothèque à l’aide de **IWMPMediaCollection :: Add**.
-   Le contenu multimédia numérique est ajouté à la bibliothèque à l’aide de la fonctionnalité de recherche du lecteur Windows Media.
-   Le contenu multimédia numérique est ajouté à la bibliothèque par la fonctionnalité de surveillance des dossiers du lecteur Windows Media.
-   Le contenu multimédia numérique est ajouté à la liste de synchronisation lorsque l’utilisateur fait glisser et supprime un fichier.

Une fois que le lecteur Windows Media a créé une instance d’un plug-in de conversion, le plug-in doit convertir le fichier fourni en ASF ou WMA et ajouter les métadonnées appropriées. (N’utilisez pas le plug-in de conversion pour Transcoder le fichier.) Le plug-in doit ensuite copier le fichier converti dans le dossier spécifié et retourner le chemin d’accès au nouveau fichier dans le lecteur Windows Media.

Les plug-ins de conversion doivent implémenter l’interface **IWMPConvert** . Consultez [les informations de référence sur la programmation de plug-ins de conversion](conversion-plug-ins-programming-reference.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos du processus de conversion**](about-the-conversion-process.md)
</dt> <dt>

[**Ajout de métadonnées aux fichiers convertis**](adding-metadata-to-converted-files.md)
</dt> <dt>

[**Plug-ins de conversion du lecteur Windows Media**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




