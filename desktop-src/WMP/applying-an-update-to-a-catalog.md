---
title: Application d’une mise à jour à un catalogue
description: Application d’une mise à jour à un catalogue
ms.assetid: 4aedb0d6-36c7-425c-b6d3-e16161cf6828
keywords:
- Lecteur Windows Media des magasins en ligne, application de mises à jour aux catalogues
- magasins en ligne, appliquer des mises à jour à des catalogues
- tapez 1 magasins en ligne, en appliquant des mises à jour aux catalogues
- Lecteur Windows Media des magasins en ligne, mise à jour des catalogues
- magasins en ligne, mise à jour des catalogues
- types 1 magasins en ligne, mise à jour des catalogues
- Lecteur Windows Media des magasins en ligne, mises à jour de catalogue
- magasins en ligne, mises à jour de catalogue
- types 1 magasins en ligne, mises à jour de catalogue
- mises à jour du catalogue
- mise à jour des catalogues
- application de mises à jour aux catalogues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114b5b341df1101b221a3d8227bf0526bfa32af744f1dca7b0a53ca2d7793c46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124029"
---
# <a name="applying-an-update-to-a-catalog"></a>Application d’une mise à jour à un catalogue

> [!Note]  
> Cela n’est généralement pas fait, sauf à des fins de diagnostic, par exemple pour vous aider à vérifier qu’un fichier de différences est valide. le catalogue généré de cette façon n’est pas au format compressé et ne doit pas être transmis à Lecteur Windows Media.

 

Un nouveau fichier de catalogue peut être créé à l’aide de la syntaxe ci-dessous, où *inputcatalog* est l’emplacement du catalogue d’origine et *inputdiff* est l’emplacement du fichier de différences à appliquer. Les fichiers de catalogue doivent être au format non compressé.


```C++
catcomp applydiff <inputcatalog> <inputdiff>
```



Par exemple, le code suivant crée un nouveau catalogue à partir de C : \\ Catalog210 \\ Catalog. WMDB et de c : \\ Catalog210 \\ Catalog. diff.


```C++
catcomp applydiff C:\Catalog210\catalog.wmdb C:\Catalog210\catalog.diff
```



Si la compilation réussit, catcomp.exe crée les fichiers de sortie suivants.



| Nom de fichier        | Description       |
|------------------|-------------------|
| Catalog. WMDB. New | Nouveau fichier de catalogue. |



 

 

 




