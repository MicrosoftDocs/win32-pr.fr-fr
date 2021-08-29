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
ms.openlocfilehash: d01130a34759d8445913704a37406d93a1bbce0b8ad714f4467783e4b3a63b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144732"
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

 

 