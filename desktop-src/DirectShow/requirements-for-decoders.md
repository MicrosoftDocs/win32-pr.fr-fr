---
description: Conditions requises pour les décodeurs
ms.assetid: 149aea20-0d37-4b1c-a098-8446c4088ce1
title: Conditions requises pour les décodeurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461120bec88636e4c015c2e319d855571e8ac1b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481449"
---
# <a name="requirements-for-decoders"></a>Conditions requises pour les décodeurs

Les décodeurs qui fournissent des exemples au VMR doivent respecter les règles suivantes :

-   Un cadre de sous-image doit être remis à VMR pour chaque image vidéo. Les deux frames doivent avoir le même horodatage.
-   Si la sous-image n’a pas changé, utilisez \_ l' \_ indicateur AM GBF NOTASYNCPOINT dans la méthode [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) pour forcer l’allocateur à retourner une mémoire tampon contenant la dernière trame remise à VMR. Il vous suffit de placer un nouvel horodatage sur l’échantillon et de le remettre dans le VMR. Si la représentation sous-image est vide, vous devez toujours la remettre. VMR détecte le frame vide et ne le fusionne pas avec la vidéo. Ce test est effectué par la puce VGA et n’affecte pas les performances de lecture.
-   Tous les exemples, à l’exception des flux Live, doivent avoir des horodatages de début et de fin valides attachés. (Le DVD n’est pas un flux en direct.)
-   Les horodatages de l’échantillon de support doivent être contigus
-   Le décodeur doit s’identifier comme étant conforme à VMR pour une utilisation par les générateurs de graphiques.
-   Le flux de sous-image doit maintenant contenir des valeurs alpha par pixel incorporées. Le type de surface ARGB4444 est idéal pour les sous-images.
-   Ne supposez pas que le Stride de la sous-image est identique à la largeur de la surface. Ce n’est pas toujours le cas avec VMR.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de l’accélération vidéo DirectX](about-directx-video-acceleration.md)
</dt> </dl>

 

 



