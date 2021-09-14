---
description: Ajout d’une source
ms.assetid: 8c5d1050-a696-4a5d-be68-806420d0cd78
title: Ajout d’une source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee583cd8971c183f2e03b92f68e2d6ba555c41db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112354"
---
# <a name="adding-a-source"></a>Ajout d’une source

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Créez un objet source de la même façon que vous créez d’autres objets Timeline. Toutefois, avant de l’insérer dans la chronologie, vous devez spécifier au moins les propriétés suivantes sur la source.

-   Heures de début et de fin, par rapport à la chronologie. Appelez la méthode [**IAMTimelineObj :: SetStartStop**](iamtimelineobj-setstartstop.md) .
-   Fichier multimédia à utiliser comme source. Appelez la méthode [**IAMTimelineSrc :: SetMediaName**](iamtimelinesrc-setmedianame.md) avec une chaîne de caractères larges représentant le nom du fichier.
-   Les heures de début et de fin des médias, qui sont relatives au fichier d’origine. Appelez la méthode [**IAMTimelineSrc :: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) . pour plus d’informations sur les temps de support, consultez [l’heure dans DirectShow Services d’édition](time-in-directshow-editing-services.md).

Dans l’exemple suivant, l’élément source démarre quatre secondes dans le fichier. La durée du média est de 10 secondes, soit deux fois plus longue que la durée de la chronologie, ce qui signifie que la source est lue à deux fois la vitesse normale. Les unités constantes sont définies comme 10 millions (10 ^ 7) et sont égales à une seconde.


```C++
pSourceObj->SetStartStop(0, 50000000)
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.avi"), 15);
pSource->SetMediaName(bstrFile); 
SysFreeString(bstrFile);
pSource->SetMediaTimes(40000000, 140000000);
```



> [!Note]  
> Actuellement, les ne peuvent pas afficher simultanément plus de 75 sources compressées avec des codecs VCM (Video Compression Manager). En outre, si le projet dans son ensemble contient plus de 75 de telles sources, vous devez utiliser la reconnexion dynamique ou DES ne peuvent pas afficher un aperçu du projet. Pour plus d’informations, consultez [**IRenderEngine :: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).

 

Pour plus d’informations sur les sources, consultez [utilisation des sources](working-with-sources.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Construction d’une chronologie](constructing-a-timeline.md)
</dt> </dl>

 

 



