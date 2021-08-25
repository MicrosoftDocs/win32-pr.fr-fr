---
title: À propos des plug-ins de conversion
description: À propos des plug-ins de conversion
ms.assetid: bd6d1020-e8e1-492e-9c76-9f3cf04190de
keywords:
- Lecteur Windows Media, plug-ins de conversion
- plug-ins Lecteur Windows Media, conversion
- plug-ins, conversion
- plug-ins de conversion, à propos de
- ASF (Advanced Systems Format)
- ASF (format avancé des systèmes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4331f2cc0cdf8726e2ba26e834c56546ee614e012a9dd6acdad56906d450b66e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903549"
---
# <a name="about-conversion-plug-ins"></a>À propos des plug-ins de conversion

vous pouvez créer un plug-in Lecteur Windows Media pour convertir des fichiers multimédias numériques créés à l’aide de technologies non fournies par Microsoft, au Format ASF (Advanced Systems Format).

Les plug-ins de conversion sont des objets COM (Component Object Model) qui sont empaquetés et distribués en tant que fichiers exécutables (.exe). Lecteur Windows Media instancie des plug-ins de conversion pour convertir des formats multimédias numériques tiers dans les scénarios suivants :

-   Le contenu multimédia numérique est copié sur l’ordinateur à partir d’un appareil mobile.
-   Le contenu multimédia numérique est ajouté à la bibliothèque à l’aide de **IWMPMediaCollection :: Add**.
-   le contenu multimédia numérique est ajouté à la bibliothèque à l’aide de la fonctionnalité de recherche de Lecteur Windows Media.
-   le contenu multimédia numérique est ajouté à la bibliothèque à l’aide de la fonctionnalité d’analyse de dossiers de Lecteur Windows Media.
-   Le contenu multimédia numérique est ajouté à la liste de synchronisation lorsque l’utilisateur fait glisser et supprime un fichier.

une fois que Lecteur Windows Media créé une instance d’un plug-in de conversion, le plug-in doit convertir le fichier fourni en ASF ou WMA et ajouter les métadonnées appropriées. (N’utilisez pas le plug-in de conversion pour Transcoder le fichier.) le plug-in doit ensuite copier le fichier converti dans le dossier spécifié et retourner le chemin d’accès au nouveau fichier à Lecteur Windows Media.

Les plug-ins de conversion doivent implémenter l’interface **IWMPConvert** . Consultez [les informations de référence sur la programmation de plug-ins de conversion](conversion-plug-ins-programming-reference.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos du processus de conversion**](about-the-conversion-process.md)
</dt> <dt>

[**Ajout de métadonnées aux fichiers convertis**](adding-metadata-to-converted-files.md)
</dt> <dt>

[**Lecteur Windows Media Plug-ins de conversion**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




