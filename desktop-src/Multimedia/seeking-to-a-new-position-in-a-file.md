---
title: Recherche d’une nouvelle position dans un fichier
description: Recherche d’une nouvelle position dans un fichier
ms.assetid: 276c3e43-bf9f-4a0a-b33a-7eaa701e92a6
keywords:
- e/s de fichier multimédia, déplacement vers le début des fichiers
- e/s de fichier, déplacement vers le début des fichiers
- entrée et sortie (e/s), déplacement vers le début des fichiers
- E/s (entrée et sortie), déplacement vers le début des fichiers
- passage au début des fichiers d’e/s
- e/s de fichier multimédia, recherche d’une nouvelle position dans les fichiers
- e/s de fichier, recherche d’une nouvelle position dans les fichiers
- entrée et sortie (e/s), recherche d’une nouvelle position dans les fichiers
- E/s (entrée et sortie), recherche d’une nouvelle position dans les fichiers
- recherche d’une nouvelle position dans des fichiers d’e/s
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e51ab51065bcdf89af84f2fd622558261dd4cf42cac3e50fe54fb116a7ad9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136583"
---
# <a name="seeking-to-a-new-position-in-a-file"></a>Recherche d’une nouvelle position dans un fichier

L’exemple suivant passe au début d’un fichier ouvert à l’aide de la fonction [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) .


```C++
mmioSeek(hFile, 0L, SEEK_SET); 
```



L’exemple suivant passe à la fin d’un fichier ouvert.


```C++
mmioSeek(hFile, 0L, SEEK_END); 
```



L’exemple suivant passe à une position de 10 octets à partir de la fin d’un fichier ouvert.


```C++
mmioSeek(hFile, -10L, SEEK_END); 

```



 

 