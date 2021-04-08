---
title: Récupération des informations de catalogue
description: Récupération des informations de catalogue
ms.assetid: f2ec795f-6e6f-4c0c-9332-f1e96524221a
keywords:
- Magasins en ligne du lecteur Windows Media, récupération des informations du catalogue
- magasins en ligne, récupération des informations de catalogue
- types 1 magasins en ligne, récupération des informations du catalogue
- Magasins en ligne du lecteur Windows Media, informations de diagnostic sur les catalogues
- magasins en ligne, informations de diagnostic sur les catalogues
- tapez 1 magasins en ligne, informations de diagnostic sur les catalogues
- Windows Media Player Online stores, catcomp.exe
- magasins en ligne, catcomp.exe
- tapez 1 magasins en ligne, catcomp.exe
- catcomp.exe
- informations de diagnostic sur les catalogues
- récupération des informations de catalogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721d6ba3e4d6b5106cf44446d4c96ed842ccd61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674685"
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



 

 




