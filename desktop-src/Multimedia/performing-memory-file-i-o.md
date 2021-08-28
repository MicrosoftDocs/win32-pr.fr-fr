---
title: Exécution des e/s de fichier de mémoire
description: Exécution des e/s de fichier de mémoire
ms.assetid: c0a5c8a0-978f-47d9-8ef0-ad391b9d1e63
keywords:
- e/s de fichier multimédia, mémoire
- e/s de fichier, mémoire
- entrée et sortie (e/s), mémoire
- E/s (entrée et sortie), mémoire
- e/s de mémoire
- mmioOpen fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90a2b1e2e47ffccc21b2684dcb6bd285b7e55470776fb57eb382a969091a19e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805889"
---
# <a name="performing-memory-file-io"></a>Exécution des e/s de fichier de mémoire

Les services d’e/s de fichier multimédia vous permettent de traiter un bloc de mémoire comme un fichier. Cela peut être utile si vous avez déjà une image de fichier en mémoire. Les fichiers mémoire vous permettent de réduire le nombre de conditions de cas spéciaux dans votre code, car, à des fins d’e/s, vous pouvez traiter les fichiers de mémoire comme s’il s’agissait de fichiers sur disque. Vous pouvez également utiliser des fichiers de mémoire avec le presse-papiers.

Comme pour les mémoires tampons d’e/s, les fichiers mémoire peuvent utiliser la mémoire allouée par l’application ou par le gestionnaire d’e/s de fichier. En outre, les fichiers mémoire peuvent être développables ou non développables. Lorsque le gestionnaire d’e/s de fichier atteint la fin d’un fichier mémoire extensible, il étend le fichier de mémoire à un incrément prédéfini.

Pour ouvrir un fichier de mémoire, utilisez la fonction [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) avec le paramètre *SzFilename* défini sur **null** et l' \_ indicateur MMIO ReadWrite définis dans le paramètre *dwOpenFlags* . Définissez le paramètre *lpmmioinfo* pour qu’il pointe vers une structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) qui a été configurée comme suit :

1.  Affectez la valeur **null** au membre **pIOProc** .
2.  Définissez le membre **fccIOProc** sur FourCC \_ MEM.
3.  Définissez le membre **pchBuffer** pour qu’il pointe vers le bloc de mémoire. Pour demander que le gestionnaire d’e/s de fichier alloue le bloc de mémoire, affectez à **pchBuffer** la **valeur null**.
4.  Définissez le membre **cchBuffer** sur la taille initiale du bloc de mémoire.
5.  Définissez le membre **adwInfo** sur la taille d’expansion minimale du bloc de mémoire. Pour un fichier de mémoire non développable, affectez à **adwInfo** la **valeur null**.
6.  Affectez la valeur zéro à tous les autres membres.

Il n’existe aucune restriction quant à l’allocation de mémoire pour une utilisation en tant que fichier mémoire non développable.

 

 