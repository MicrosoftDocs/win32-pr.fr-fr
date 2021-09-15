---
description: Configuration système requise pour VMR
ms.assetid: fd50b312-73f0-4c68-a8b1-3497d958bc8f
title: Configuration système requise pour VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d54d6d1604c3e514f3ceef379eaba4a8fa1ee1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238937"
---
# <a name="vmr-system-requirements"></a>Configuration système requise pour VMR

VMR utilise exclusivement les capacités de traitement graphique de la carte graphique de l’ordinateur ; VMR n’effectue pas de fusion ou de rendu vidéo à l’aide du processeur hôte, car cela aurait un impact considérable sur la fréquence d’images et la qualité de la vidéo affichée. En tirant parti des nouvelles fonctionnalités offertes par le VMR, notamment la fusion de plusieurs flux vidéo et/ou d’images d’application, les performances globales obtenues dépendent fortement des capacités de la carte graphique utilisée sur l’ordinateur. Les cartes graphiques qui fonctionnent correctement avec VMR intègrent la prise en charge matérielle suivante :

-   Prise en charge des surfaces YUV et « non-puissance de 2 ».
-   Capacité à StretchBlt des surfaces YUV à RVB DirectDraw.
-   Au moins 16 Mo de mémoire vidéo si plusieurs flux vidéo doivent être mélangés ensemble. La quantité réelle de mémoire requise dépend de la taille de l’image des flux vidéo et de la résolution du mode d’affichage utilisé.
-   Prise en charge d’une superposition RVB ou possibilité d’effectuer une fusion sur une surface de recouvrement YUV.
-   Décodage vidéo accélérée par le matériel (prise en charge du décodage DirectX Video Acceleration).
-   Taux de remplissage de pixels élevés.

> [!Note]  
> VMR requiert la définition du moniteur système pour une profondeur de couleur d’au moins 16 bits. Le VMR ne peut pas être placé dans un état d’exécution si l’analyse est définie sur 256 couleurs. En outre, certaines cartes vidéo ne peuvent pas effectuer d’opérations Direct3D lorsque l’affichage est défini sur 24 bits par pixel.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos du rendu de mixage vidéo](about-the-video-mixing-render.md)
</dt> </dl>

 

 



