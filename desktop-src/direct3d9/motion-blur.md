---
description: Vous pouvez améliorer la vitesse perçue d’un objet dans une scène 3D en brouilleant l’objet et en laissant une trace floue des images d’objet derrière l’objet. Pour ce faire, les applications Direct3D effectuent le rendu de l’objet plusieurs fois par frame.
ms.assetid: 8b1a1f0d-5857-4ab4-828c-8ca7c17a4890
title: Flou directionnel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fccb5c00d1208041afc31d4afe1cf0c7a5425037
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521919"
---
# <a name="motion-blur-direct3d-9"></a>Flou directionnel (Direct3D 9)

Vous pouvez améliorer la vitesse perçue d’un objet dans une scène 3D en brouilleant l’objet et en laissant une trace floue des images d’objet derrière l’objet. Pour ce faire, les applications Direct3D effectuent le rendu de l’objet plusieurs fois par frame.

Rappelez-vous que les applications Direct3D affichent généralement des scènes dans une mémoire tampon hors écran. Le contenu de la mémoire tampon s’affiche à l’écran lorsque l’application appelle la méthode [**IDirect3DDevice9 ::P revois**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) . Votre application Direct3D peut restituer l’objet plusieurs fois dans une scène avant d’afficher le cadre sur l’écran.

Par programme, votre application effectue plusieurs appels à une méthode DrawPrimitive, en passant à plusieurs reprises le même objet 3D. Avant chaque appel, la position de l’objet est légèrement mise à jour, ce qui produit une série d’images d’objets floues sur la surface de rendu cible. Si l’objet a une ou plusieurs textures, votre application peut améliorer l’effet de flou directionnel en rendant la première image de l’objet avec toutes ses textures presque transparentes. À chaque rendu de l’objet, la transparence de la texture de l’objet diminue. Lorsque votre application restitue l’objet dans sa position finale, elle doit restituer les textures de l’objet sans transparence. L’exception est si vous ajoutez un flou de mouvement à un autre effet nécessitant une transparence de texture. Dans tous les cas, l’image initiale de l’objet dans le frame doit être la plus transparente. L’image finale doit être la moins transparente.

Une fois que votre application a rendu la série d’images d’objet sur la surface de rendu cible et a rendu le reste de la scène, elle doit appeler la méthode [**IDirect3DDevice9 ::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) replaced pour afficher le frame à l’écran.

Si votre application simule l’effet de l’utilisateur qui se déplace dans une scène à grande vitesse, il peut ajouter un flou directionnel à la scène entière. Dans ce cas, votre application restitue l’intégralité de la scène plusieurs fois par trame. Chaque fois que la scène est rendue, votre application doit légèrement déplacer le point de vue. Si la scène est très complexe, l’utilisateur peut voir une dégradation des performances visible lorsque l’accélération est accrue en raison du nombre croissant de rendus de scène par image.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Anticrénelage](antialiasing.md)
</dt> </dl>

 

 
