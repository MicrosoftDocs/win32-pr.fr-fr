---
title: Génération de codes Four-Character
description: Génération de codes Four-Character
ms.assetid: dfb771f1-9273-4f60-a3af-3a62a3794e59
keywords:
- e/s de fichier multimédia, codes à quatre caractères
- e/s de fichier, codes à quatre caractères
- entrées et sorties (e/s), codes à quatre caractères
- E/s (entrée et sortie), codes à quatre caractères
- codes à quatre caractères
- mmioStringToFOURCC fonction)
- mmioFOURCC macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c83540b49d83ee325479542e5a2917ac61ce19b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368415"
---
# <a name="generating-four-character-codes"></a>Génération de codes Four-Character

Vous pouvez utiliser la macro [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) ou la fonction [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) pour générer des codes à quatre caractères. L’exemple suivant utilise **mmioFOURCC** pour générer un code à quatre caractères pour « Wave ».


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioFOURCC('W', 'A', 'V', 'E'); 
 
```



L’exemple suivant utilise [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) pour générer un code à quatre caractères pour « Wave ».


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioStringToFOURCC("WAVE", 0); 
```



Le deuxième paramètre dans [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) spécifie des indicateurs pour la conversion de la chaîne en code à quatre caractères. Si vous spécifiez l' \_ indicateur MMIO TOUPPER, **mmioStringToFOURCC** convertit tous les caractères alphabétiques de la chaîne en majuscules. Cela est utile lorsque vous devez spécifier un code à quatre caractères pour identifier une procédure d’e/s personnalisée, car les codes à quatre caractères identifiant les noms d’extension de fichier doivent être en majuscules.

 

 