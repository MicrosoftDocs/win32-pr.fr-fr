---
title: Récupération des informations de catalogue
description: Récupération des informations de catalogue
ms.assetid: f2ec795f-6e6f-4c0c-9332-f1e96524221a
keywords:
- Lecteur Windows Media des magasins en ligne, extraction d’informations de catalogue
- magasins en ligne, récupération des informations de catalogue
- types 1 magasins en ligne, récupération des informations du catalogue
- Lecteur Windows Media des magasins en ligne, informations de diagnostic sur les catalogues
- magasins en ligne, informations de diagnostic sur les catalogues
- tapez 1 magasins en ligne, informations de diagnostic sur les catalogues
- Lecteur Windows Media des magasins en ligne, catcomp.exe
- magasins en ligne, catcomp.exe
- tapez 1 magasins en ligne, catcomp.exe
- catcomp.exe
- informations de diagnostic sur les catalogues
- récupération des informations de catalogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3b28da6d2d5f5143dab0664c10d0c906f971a6a60e4fdb502f4331fa71f408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570200"
---
# <a name="retrieving-catalog-information"></a>Récupération des informations de catalogue

Vous pouvez afficher les informations de diagnostic sur un catalogue en exécutant catcomp avec la syntaxe suivante :


```C++
catcomp info <catalogpath> [track|artist|album] [ID]
```



Par exemple, la commande suivante affiche des informations sur un catalogue entier, y compris la version, les paramètres régionaux et les informations internes sur les éléments du catalogue :


```C++
catcomp info C:\Catalog210\catalog.wmdb
```



La commande suivante affiche des informations sur la piste avec l’ID 3256 :


```C++
catcomp info C:\Catalog210\catalog.wmdb track 3256
```



 

 




