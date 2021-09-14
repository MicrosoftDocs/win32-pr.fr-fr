---
title: Compilation d’une mise à jour de catalogue à partir de catalogues complets
description: Compilation d’une mise à jour de catalogue à partir de catalogues complets
ms.assetid: 046c0a01-0ad7-41b6-bad5-dcab953a3980
keywords:
- Lecteur Windows Media des magasins en ligne, compilation de catalogues
- magasins en ligne, compilation de catalogues
- types 1 magasins en ligne, compilation des catalogues
- Lecteur Windows Media des magasins en ligne, mises à jour de catalogue
- magasins en ligne, mises à jour de catalogue
- types 1 magasins en ligne, mises à jour de catalogue
- Lecteur Windows Media des magasins en ligne, des catalogues complets
- magasins en ligne, catalogues complets
- tapez 1 magasins en ligne, catalogues complets
- compilation des catalogues
- mises à jour du catalogue
- catalogues complets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abaa6d1bc0d3dbc4fefaffe1498be03259716a5e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008486"
---
# <a name="compiling-a-catalog-update-from-full-catalogs"></a>Compilation d’une mise à jour de catalogue à partir de catalogues complets

Une mise à jour du catalogue contenant les modifications entre deux versions d’un catalogue compilé peut être créée à l’aide de la syntaxe ci-dessous, où *chemin1* est le répertoire contenant le premier catalogue, *chemin2* le répertoire contenant le deuxième catalogue et le débogage peut être éventuellement inclus pour afficher des informations détaillées sur l’erreur à l’écran. Les fichiers de catalogue doivent être dans un format non compressé : le nom de fichier du catalogue compilé est catalog. WMDB, plutôt que Catalog. WMDB. LZ.


```C++
catcomp diff <path1> <path2> [debug]
```



Par exemple, si le répertoire C : \\ Catalog210 \\ contient la version 210 d’un catalogue compilé complet et que le répertoire c : \\ Catalog211 \\ contient la version 211, la commande suivante crée un fichier de différences qui contient les modifications entre les deux versions :


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\
```



Pour afficher des informations détaillées sur l’erreur, vous pouvez ajouter le paramètre de débogage facultatif comme suit :


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\ debug
```



Si la compilation réussit, catcomp.exe crée les fichiers de sortie listés ci-dessous et les enregistre dans le répertoire qui contient le premier catalogue.



| Nom de fichier             | Description                                                                                                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Catalog. diff          | Fichier de différences compilées non compressées.                                                                                                                                                           |
| Catalog. diff. LZ       | Version compressée du fichier de mise à jour du catalogue. votre plug-in peut fournir l’emplacement de ce fichier à Lecteur Windows Media dans [IWMPContentPartner :: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl). |
| Catalog. WMDB. Delta    | Fichier de sortie intermédiaire. non utilisé par Lecteur Windows Media                                                                                                                                       |
| Catalog. WMDB. modified | Fichier de sortie intermédiaire. non utilisé par Lecteur Windows Media                                                                                                                                       |



 

 

 




