---
description: Définition de la vitesse de lecture
ms.assetid: 74ae45d3-4fea-491c-af1f-46768df41c5f
title: Définition de la vitesse de lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0404e67d716616a4c383c134a4fb4e75060e3094023abec52df1d38099b92b33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583319"
---
# <a name="setting-the-playback-rate"></a>Définition de la vitesse de lecture

Pour modifier la vitesse de lecture, appelez la méthode [**IMediaSeeking ::**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) se. Spécifiez le nouveau taux comme une fraction du taux d’origine. Par exemple, pour jouer à deux fois la vitesse normale, utilisez les éléments suivants :


```C++
pSeek->SetRate(2.0)
```



Les taux supérieurs à un sont plus rapides que le débit normal. Les taux entre zéro et un sont plus lents que la normale. Les taux négatifs sont définis en tant que lecture descendante, mais dans la pratique, la plupart des filtres ne le prennent pas en charge. actuellement, aucun des filtres de DirectShow standard ne prend en charge la lecture inversée.

Quelle que soit la vitesse de lecture, la position actuelle et la position d’arrêt sont toujours exprimées par rapport à la source d’origine. Par exemple, si un fichier source a une durée de lecture normale de 20 secondes, le fait de définir la position actuelle sur 10 secondes recherche le milieu du fichier. Si la vitesse de lecture est de 2,0, la position d’arrêt est de 20 secondes et vous recherchez la position à 10 secondes, le fichier est lu pendant 5 secondes de temps réel : 10 secondes, à deux fois la vitesse de lecture normale. À une vitesse de lecture de 2,0, la position actuelle augmente à deux fois le taux de l’horloge de référence.

 

 



