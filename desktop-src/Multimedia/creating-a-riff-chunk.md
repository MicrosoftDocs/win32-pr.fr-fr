---
title: Création d’un bloc RIFF
description: Création d’un bloc RIFF
ms.assetid: d17f6215-f04f-4776-826e-eedb245f549b
keywords:
- e/s de fichier multimédia, création de bloc RIFF
- e/s de fichier, création d’un bloc RIFF
- entrée et sortie (e/s), création d’un bloc RIFF
- E/s (entrée et sortie), création d’un bloc RIFF
- création du bloc RIFF
- mmioCreateChunk fonction)
- RIFF (Resource Interchange File Format)
- RIFF (Resource Interchange File Format)
- E/S RIFF
- Bloc RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca2cca96b45ecf0313f811b5df4e966be8fc0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842194"
---
# <a name="creating-a-riff-chunk"></a>Création d’un bloc RIFF

L’exemple suivant utilise la fonction [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) pour créer un segment avec un identificateur de segment « Riff » et un type de formulaire « RDIB ».


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfo; 
. 
. 
. 
mmckinfo.fccType = mmioFOURCC('R', 'D', 'I', 'B'); 
mmioCreateChunk(hmmio, &mmckinfo, MMIO_CREATERIFF); 
```



Si vous créez un bloc « RIFF » ou « LIST », vous devez spécifier le type de formulaire ou le type de liste dans le membre **fccType** de la structure [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) . Dans l’exemple précédent, « RDIB » est le type de formulaire.

Si vous connaissez la taille du champ de données dans un nouveau bloc, vous pouvez définir le membre **cksize** de la structure **MMCKINFO** lors de la création du bloc. Cette valeur sera écrite dans le champ de la taille des données dans le nouveau bloc. Si cette valeur n’est pas correcte lorsque vous appelez [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) pour marquer la fin du segment, elle est automatiquement réécrite pour refléter la taille correcte du champ de données.

Une fois que vous avez créé un segment à l’aide de la fonction [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) , la position de fichier est définie sur le champ de données du segment (8 octets à partir du début du bloc). Si le segment est un bloc « RIFF » ou « LIST », la position de fichier est définie sur l’emplacement suivant le type de formulaire ou le type de liste (12 octets à partir du début du bloc).

 

 