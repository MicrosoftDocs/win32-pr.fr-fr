---
description: Bien que les termes largeur et hauteur soient souvent utilisés de manière informelle, ils ont des significations très importantes et distinctement différentes. Par conséquent, vous devez comprendre les significations de chaque, et savoir comment interpréter les valeurs que Direct3D utilise pour les décrire.
ms.assetid: 2f99881b-f95d-470f-b14d-8300ad930e2a
title: Largeur et inclinaison (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50d0c8fc49b3bce984e56f7b1a727ed40fee67b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104561592"
---
# <a name="width-vs-pitch-direct3d-9"></a>Largeur et inclinaison (Direct3D 9)

Bien que les termes largeur et hauteur soient souvent utilisés de manière informelle, ils ont des significations très importantes et distinctement différentes. Par conséquent, vous devez comprendre les significations de chaque, et savoir comment interpréter les valeurs que Direct3D utilise pour les décrire.

Direct3D utilise la structure [**D3DSURFACE \_ desc**](d3dsurface-desc.md) pour transporter des informations décrivant une surface. Entre autres choses, cette structure est définie pour contenir des informations sur les dimensions d’une surface, ainsi que la façon dont ces dimensions sont représentées en mémoire. La structure utilise les membres de hauteur et de largeur pour décrire les dimensions logiques de l’aire. Les deux membres sont mesurés en pixels. Par conséquent, les valeurs de hauteur et de largeur pour une surface 640 x 480 sont les mêmes, qu’il s’agisse d’une surface de 8 bits ou d’une surface RGB de 24 bits.

Lorsque vous verrouillez une surface à l’aide de la méthode [**IDirect3DSurface9 :: LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) , la méthode remplit une structure [**\_ Rect D3DLOCKED**](d3dlocked-rect.md) qui contient le pas de la surface et un pointeur vers les bits verrouillés. La valeur du membre de pas décrit le pas à pas de la mémoire de la surface, également appelée Stride. Le pas est la distance, en octets, entre deux adresses mémoire qui représentent le début d’une ligne bitmap et le début de la ligne bitmap suivante. Étant donné que le pas est mesuré en octets plutôt qu’en pixels, une surface 640x480x8 a une valeur de pas très différente de celle d’une surface avec les mêmes dimensions mais un format de pixel différent. En outre, la valeur de tangage reflète parfois les octets réservés par Direct3D en tant que cache. il n’est donc pas possible de supposer que le pas de pas est juste la largeur multipliée par le nombre d’octets par pixel. Au lieu de cela, Visualisez la différence entre la largeur et le pas, comme indiqué dans le diagramme suivant.

![diagramme du pas et de la largeur du même tampon d’avant, de la mémoire tampon d’arrière-plan et du cache](images/pitch.png)

Dans ce diagramme, la mémoire tampon d’arrière-plan et la mémoire tampon d’arrière-plan sont toutes les deux 640x480x8 et le cache est 384x480x8.

Lorsque vous accédez directement à des surfaces, veillez à rester dans la mémoire allouée pour les dimensions de la surface et à conserver la mémoire réservée pour le cache. En outre, lorsque vous verrouillez uniquement une partie d’une surface, vous devez rester dans le rectangle que vous spécifiez lors du verrouillage de l’aire. L’échec de ces instructions aura des résultats imprévisibles. Lors du rendu direct dans la mémoire de surface, utilisez toujours le pas retourné par la méthode [**IDirect3DSurface9 :: LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) . Ne supposez pas un pas basé uniquement sur le mode d’affichage. Si votre application fonctionne sur certains adaptateurs d’affichage, mais semble déformée sur d’autres, cela peut être la cause du problème.

Pour plus d’informations, consultez [accès direct à la mémoire de surface (Direct3D 9)](accessing-surface-memory-directly.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Surfaces Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
