---
title: Compilateur de catalogue pour les magasins en ligne de type 1
description: Compilateur de catalogue pour les magasins en ligne de type 1
ms.assetid: 49c03d3b-3381-4663-83c8-5bc8fa70f7c3
keywords:
- Magasins en ligne du lecteur Windows Media, compilateur de catalogue
- magasins en ligne, compilateur de catalogue
- magasins en ligne de type 1, compilateur de catalogue
- Windows Media Player Online stores, catcomp.exe
- magasins en ligne, catcomp.exe
- tapez 1 magasins en ligne, catcomp.exe
- compilateur de catalogue
- catcomp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c54ffd054c5e72b04ddd32eef12c7fe6b6cc89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106509428"
---
# <a name="catalog-compiler-for-type-1-online-stores"></a>Compilateur de catalogue pour les magasins en ligne de type 1

Le compilateur de catalogue (catcomp.exe) est un outil de ligne de commande utilisé par les magasins de type 1 en ligne pour compiler l’ensemble de fichiers TSV (valeurs séparées par des tabulations) contenant les données de catalogue du magasin en ligne dans un catalogue compressé qui peut être téléchargé par le lecteur Windows Media. Le compilateur de catalogue compile également les fichiers de mise à jour du catalogue contenant uniquement les informations du catalogue qui ont été modifiées depuis la dernière mise à jour du catalogue.

Les fichiers de catalogue compressé ou les fichiers de mise à jour de catalogue doivent être fournis au lecteur Windows Media pour téléchargement dans l’implémentation du plug-in de magasin en ligne de [IWMPContentPartner :: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).

Tâches courantes

-   [Compilation d’un catalogue complet à partir de fichiers TSV](compiling-a-full-catalog-from-tsv-files.md)
-   [Compilation d’une mise à jour de catalogue à partir de catalogues complets](compiling-a-catalog-update-from-full-catalogs.md)

Tâches de diagnostic

-   [Affichage de l’aide](displaying-help.md)
-   [Récupération des informations de catalogue](retrieving-catalog-information.md)
-   [Application d’une mise à jour à un catalogue](applying-an-update-to-a-catalog.md)

 

 




