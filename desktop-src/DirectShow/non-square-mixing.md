---
description: Mélange non carré
ms.assetid: 8d27a921-5638-43ac-807d-e3bd7b9b2de8
title: Mélange non carré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d23f423f0dbe19f1ff0ba35c44f8fd2f8732bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522052"
---
# <a name="non-square-mixing"></a>Mélange non carré

Cette rubrique s’applique à Windows XP Service Pack 2 ou version ultérieure.

Lorsque VMR-9 mélange deux flux ou plus, il y a deux points où la mise à l’échelle peut se produire : lorsque le mélange composite les flux d’entrée, et lorsque l’Allocator-Presenter effectue le rendu de l’image composite.

![opérations de mixage VMR](images/vmr-nonsquare-mixing.png)

Les versions précédentes de VMR-9 ont toujours composé les flux d’entrée à l’aide d’un ratio de pixels carré (1:1), même s’il n’y avait qu’un seul flux vidéo. Si le flux d’entrée comportait des pixels non carrés, cela provoquait une opération de mise à l’échelle inutile. La mise à l’échelle doit être évitée, bien sûr, car elle dégrade la qualité finale de l’image.

À compter de Windows XP Service Pack 2, VMR-9 prend en charge deux méthodes différentes pour éviter le problème de la double mise à l’échelle :

-   Implémentez un Allocator-Presenter personnalisé et prenez en charge l’interface [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) .
-   Utilisez le mode de mélange non carré.

Cette section décrit le mode de mélange non carré. Les applications peuvent combiner les deux techniques.

**Fonctionnement du mixage non carré**

En mode de mélange non carré, VMR-9 sélectionne un flux d’entrée comme taille cible et PAR défaut. Le mélangeur VMR ne met pas à l’échelle la vidéo à partir de ce flux ou de tout autre flux avec la même taille et la même image. Les flux avec une taille ou un proportions différentes sont mis à l’échelle pour correspondre au PAR-dessus cible et à letterboxed pour correspondre à la taille finale de l’image de sortie.

Le choix des flux dépend du mode de mixage actuel :

-   Le mode de mixage YUV est limité à un flux vidéo sur le pin 0. (Les autres broches peuvent avoir une sous-image ou des flux de sous-titres.) Par conséquent, VMR-9 sélectionne toujours la broche 0 pour la taille et le pair de l’image cible.
-   En mode de mixage RVB, VMR sélectionne le flux avec la plus grande taille d’image. S’il en existe plusieurs, il sélectionne celui dont l’ordre de plan est le plus élevé. et s’il y a toujours un lien, il sélectionne le flux avec le code confidentiel le plus petit.

**Exemples d’opérations**

**Exemple 1.** Le flux 0 est 720 x 480 pixels avec un rapport hauteur/largeur d’image de 16:9. Stream 1 est un 640 x 480 pixels avec un rapport hauteur/largeur d’image de 4:3.

Dans cet exemple, le flux 0 a la plus grande taille d’image. par conséquent, VMR choisit ce flux, quel que soit le mode de mélange RVB ou le mode de mixage YUB. Le pair est de 32:27 (16:9/720:480), ce qui signifie que l’image doit être étirée horizontalement par ce rapport pour produire les proportions de l’image de 16:9 correctes.

Pour correspondre au pair cible, le mélangeur VMR met à l’échelle le flux 1 en fonction du ratio inverse (27:32), ce qui génère une image 540 x 480. Les deux flux sont ensuite composés sur une surface. Pour afficher correctement l’image résultante, le présentateur de l’allocateur doit étirer l’image horizontalement pour correspondre aux proportions de l’image 16:9.

![exemple 1 :](images/vmr-nonsquare-mixing2.png)

**Exemple 2.** Le flux 0 est 720 x 480 pixels avec un rapport hauteur/largeur d’image de 16:9. Stream 1 est un 1024 x 768 pixels avec un rapport hauteur/largeur d’image de 4:3.

Si VMR-9 utilise le mode de mixage YUV, il sélectionne toujours Stream 0. Par conséquent, il étire le flux 1 sur 540 x 480 pixels, pour qu’il corresponde au pair du flux 0.

Si VMR-9 utilise le mode de mixage RGB, il sélectionne Stream 1 comme cible, car ce flux a la plus grande taille d’image. Il étend le flux 0 à une taille d’image de 1024 x 576 pixels. Notez que dans ce cas, l’image composite a un-à-un de 1:1, par conséquent, l’Allocator-Presenter ne doit pas corriger les pixels non carrés. (Il se peut que vous deviez toujours étirer la vidéo pour tenir compte du rectangle de destination.)

**Utilisation du mode de mélange non carré**

Le mode de mélange non carré est recommandé si l’une des conditions suivantes est remplie :

-   Votre application n’envoie jamais plus d’un flux vidéo à VMR-9.
-   Votre application restitue des fichiers de DVD, de télévision ou MS-DVR. Vous devez également utiliser le mode de mixage YUV dans ce cas, si le matériel graphique le prend en charge.

Si votre application mélange plusieurs flux vidéo qui peuvent avoir des tailles d’image ou des proportions de pixels variables, le mode de mélange de carrés par défaut est recommandé.

Pour configurer le mode de mixage non carré, le graphique de filtre doit être arrêté et toutes les broches d’entrée déconnectées sur VMR-9. Appelez ensuite [**IVMRMixerControl9 :: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) avec l' \_ indicateur MixerPref9 NonSquareMixing :


```C++
DWORD dwPrefs;
pMixControl->GetMixingPrefs(&dwPrefs);  
dwPrefs |= MixerPref9_NonSquareMixing;
pMixControl->SetMixingPrefs(dwPrefs);
```



> [!Note]  
> Si vous combinez l' \_ indicateur MixerPref9 NonSquareMixing avec l' \_ indicateur MixerPref9 ARADJUSTXORY, VMR-9 ignore l' \_ indicateur MixerPref9 ARAdjustXorY.

 

Si votre application utilise un allocateur-présentateur personnalisé avec le mode de mélange non carré, sachez que l’image composite peut avoir un PAR-défaut non carré. L’Allocator-Presenter doit mettre l’image à l’échelle d’un carré (1:1) PAR.

**Images bitmap statiques**

Si vous utilisez l’interface [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) pour fusionner une image bitmap statique sur la vidéo, vous devez considérer que l’image bitmap est un second flux vidéo pour les besoins du mode de mixage VMR.

VMR traite la bitmap comme ayant le même titre que la cible. Elle n’ajuste pas l’image bitmap pour qu’elle s’ajuste aux proportions de pixels de la cible. Dans la configuration par défaut de VMR, la cible a une valeur de 1:1 PAR, qui correspond à la plupart des bitmaps. En mode de mélange non carré, la cible peut avoir des pixels non carrés. Pour vous assurer que la bitmap est correctement affichée, l’application doit fournir une image dont le PAR correspond au pair cible.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du mode de mixage VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



