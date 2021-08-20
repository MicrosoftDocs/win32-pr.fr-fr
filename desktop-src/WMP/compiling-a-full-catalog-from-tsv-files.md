---
title: Compilation d’un catalogue complet à partir de fichiers TSV
description: Compilation d’un catalogue complet à partir de fichiers TSV
ms.assetid: fba80b32-dc78-4c4a-a351-e8786f9a7131
keywords:
- Lecteur Windows Media des magasins en ligne, compilation de catalogues
- magasins en ligne, compilation de catalogues
- types 1 magasins en ligne, compilation des catalogues
- Lecteur Windows Media des magasins en ligne, fichiers TSV
- magasins en ligne, fichiers TSV
- types 1 magasins en ligne, fichiers TSV
- Lecteur Windows Media des magasins en ligne, catcomp.exe
- magasins en ligne, catcomp.exe
- tapez 1 magasins en ligne, catcomp.exe
- catcomp.exe
- compilation des catalogues
- fichiers de valeurs séparées par des tabulations (TSV)
- Fichiers TSV (valeurs séparées par des tabulations)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c5bc0648c19c3c8a6f9ddb819d77e48235bcd684d4911bc8a324a109c49daf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863799"
---
# <a name="compiling-a-full-catalog-from-tsv-files"></a>Compilation d’un catalogue complet à partir de fichiers TSV

De nouveaux catalogues sont créés à partir d’un ensemble de fichiers TSV (valeurs séparées par des tabulations). Les fichiers doivent être au format Unicode. Placez les fichiers TSV requis listés ci-dessous dans un dossier (l’argument de chemin d’entrée pour catcomp.exe) et appelez catcomp.exe à l’aide de la syntaxe suivante :


```C++
catcomp <input path> [version number] [locale ID] [debug]
```



Si aucun numéro de version n’est fourni, le numéro de version est défini sur 0. Si aucun ID de paramètres régionaux n’est fourni, les paramètres régionaux système sont utilisés. Si un seul argument numérique facultatif est fourni, il est supposé être le numéro de version. Si debug est spécifié, la sortie à l’écran fournira des informations de diagnostic plus détaillées.

Par exemple, le code suivant compile un catalogue à partir des fichiers de C : \\ CatalogData \\ 210 et donne au catalogue le numéro de version 210 :


```C++
catcomp C:\CatalogData\210 210
```



Pour afficher des messages d’erreur plus détaillés, l’argument de débogage facultatif peut être ajouté, comme suit :


```C++
catcomp C:\CatalogData\210 210 debug
```



## <a name="required-tsv-files"></a>Fichiers TSV requis

Chacun des fichiers suivants doit être présent, mais un fichier vide peut être utilisé s’il n’y a pas de données pour un fichier. Par exemple, si votre catalogue ne contient pas de canaux radio, radio.csv peut être vide. Les fichiers doivent être nommés exactement comme indiqué.

[track.csv](track-csv.md)

[album.csv](album-csv.md)

[artist.csv](artist-csv.md)

[genre.csv](genre-csv.md)

[subgenre.csv](subgenre-csv.md)

[list.csv](list-csv.md)

[listitem.csv](listitem-csv.md)

[radio.csv](radio-csv.md)

> [!Note]  
> Bien que les noms de fichiers doivent avoir des extensions de .csv, les fichiers ne sont pas au format CSV (valeurs séparées par des virgules). Les fichiers doivent être au format de valeurs séparées par des tabulations (TSV).

 

Si la compilation réussit, catcomp.exe crée trois fichiers de sortie.



| Nom de fichier                   | Description                                                                                                                                                                         |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Catalog. WMDB                | Catalogue compilé non compressé.                                                                                                                                                      |
| Catalog. WMDB. LZ             | Catalogue au format compressé. votre plug-in peut fournir l’emplacement de ce fichier à Lecteur Windows Media dans [IWMPContentPartner :: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl). |
| \_words.txt unique \_ compilé | Fichier de sortie intermédiaire. non utilisé par Lecteur Windows Media.                                                                                                                      |



 

 

 




