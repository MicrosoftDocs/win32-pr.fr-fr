---
title: Compilateur de catalogue pour les magasins en ligne de type 1
description: Compilateur de catalogue pour les magasins en ligne de type 1
ms.assetid: 49c03d3b-3381-4663-83c8-5bc8fa70f7c3
keywords:
- magasins en ligne Lecteur Windows Media, compilateur de catalogue
- magasins en ligne, compilateur de catalogue
- magasins en ligne de type 1, compilateur de catalogue
- Lecteur Windows Media des magasins en ligne, catcomp.exe
- magasins en ligne, catcomp.exe
- tapez 1 magasins en ligne, catcomp.exe
- compilateur de catalogue
- catcomp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2764da5e19c84145bd0a11127aebc8f518031744626ca1b41c75c43c6e10093f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864209"
---
# <a name="catalog-compiler-for-type-1-online-stores"></a>Compilateur de catalogue pour les magasins en ligne de type 1

le compilateur de catalogue (catcomp.exe) est un outil en ligne de commande utilisé par les magasins de Type 1 en ligne pour compiler l’ensemble de fichiers TSV (valeurs séparées par des tabulations) contenant les données de catalogue du magasin en ligne dans un catalogue compressé qui peut être téléchargé par Lecteur Windows Media. Le compilateur de catalogue compile également les fichiers de mise à jour du catalogue contenant uniquement les informations du catalogue qui ont été modifiées depuis la dernière mise à jour du catalogue.

les fichiers de catalogue compressés ou les fichiers de mise à jour du catalogue doivent être fournis à Lecteur Windows Media à des fins de téléchargement dans l’implémentation du plug-in de magasin en ligne de [IWMPContentPartner :: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).

Tâches courantes

-   [Compilation d’un catalogue complet à partir de fichiers TSV](compiling-a-full-catalog-from-tsv-files.md)
-   [Compilation d’une mise à jour de catalogue à partir de catalogues complets](compiling-a-catalog-update-from-full-catalogs.md)

Tâches de diagnostic

-   [Affichage de l’aide](displaying-help.md)
-   [Récupération des informations de catalogue](retrieving-catalog-information.md)
-   [Application d’une mise à jour à un catalogue](applying-an-update-to-a-catalog.md)

 

 




