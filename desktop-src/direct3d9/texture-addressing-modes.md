---
description: Votre application Direct3D peut assigner des coordonnées de texture à n’importe quel vertex de n’importe quelle primitive.
ms.assetid: 2e23bcb3-9eba-49d9-93ce-0a4fbb15f746
title: Modes d’adressage de la texture (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb1ccc45d6f3663f3e9f7e0bb1a721f594f7834db7de4541aa1dfece2954a02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984779"
---
# <a name="texture-addressing-modes-direct3d-9"></a>Modes d’adressage de la texture (Direct3D 9)

Votre application Direct3D peut assigner des coordonnées de texture à n’importe quel vertex de n’importe quelle primitive. Pour plus d’informations, consultez [coordonnées de texture (Direct3D 9)](texture-coordinates.md). En règle générale, les coordonnées de la texture u et v que vous attribuez à un vertex sont comprises entre 0,0 et 1,0 inclus. Toutefois, en assignant des coordonnées de texture en dehors de cette plage, vous pouvez créer certains effets spéciaux de texture.

Vous contrôlez ce que Direct3D utilise avec des coordonnées de texture qui se trouvent en dehors de la \[ plage 0,0, 1,0, \] en définissant le mode d’adressage de la texture. Par exemple, vous pouvez demander à votre application de définir le mode d’adressage de la texture afin qu’une texture soit affichée en mosaïque sur une primitive.

Direct3D permet aux applications d’effectuer un habillage de texture. Il est important de noter que la définition du mode d’adressage de la texture sur D3DTADDRESS \_ Wrap n’est pas identique à l’exécution d’un habillage de texture. Le fait de définir le mode d’adressage de la texture sur D3DTADDRESS \_ encapsule les résultats dans plusieurs copies de la texture source appliquée à la primitive actuelle, et l’activation de l’habillage de texture change la façon dont le système pixellise les polygones texturés. Pour plus d’informations, consultez [habillage de texture (Direct3D 9)](texture-wrapping.md).

L’activation de l’encapsulation de texture rend effectivement les coordonnées de texture en dehors de la \[ plage 0,0, 1,0 \] et le comportement de pixellisation de ces coordonnées de texture en souffrance n’est pas défini dans ce cas. Lorsque l’habillage de texture est activé, les modes d’adressage de texture ne sont pas utilisés. Veillez à ce que votre application ne spécifie pas de coordonnées de texture inférieures à 0,0 ou supérieures à 1,0 lorsque l’habillage de texture est activé.

## <a name="setting-the-addressing-mode"></a>Définition du mode d’adressage

Vous pouvez définir les modes d’adressage de texture pour des étapes de texture individuelles en appelant la méthode [**IDirect3DDevice9 :: SetSamplerState**](/windows/desktop/api) . Spécifiez l’identificateur de l’étape de texture souhaitée dans le paramètre de l' *échantillonneur* . Définissez le paramètre de *type* sur D3DSAMP \_ Address, D3DSAMP \_ ADDRESSV ou D3DSAMP \_ ADDRESSW valeurs pour mettre à jour individuellement les modes u-, v-ou w-Addressing. Le paramètre *value* détermine quel mode est défini. Il peut s’agir de n’importe quel membre du type énuméré [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) . Pour récupérer le mode d’adresse de texture actuel pour une étape de texture, appelez [**IDirect3DDevice9 :: GetSamplerState**](/windows/desktop/api), à l’aide des \_ membres D3DSAMP Address, D3DSAMP \_ ADDRESSV ou D3DSAMP ADDRESSW \_ de l’énumération [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) pour identifier le mode d’adresse sur lequel vous souhaitez obtenir des informations.

## <a name="device-limitations"></a>Limitations des appareils

Bien que le système autorise généralement des coordonnées de texture en dehors de la plage 0,0 et 1,0, les limitations matérielles affectent souvent la distance en dehors des coordonnées de texture de la plage. Un appareil de rendu communique cette limite dans le membre **MaxTextureRepeat** de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) lorsque vous récupérez les fonctionnalités de l’appareil. La valeur de ce membre décrit la plage complète des coordonnées de texture autorisées par l’appareil. Par exemple, si cette valeur est 128, les coordonnées de texture d’entrée doivent être conservées dans la plage comprise entre-128,0 et + 128,0. La transmission de vertex avec des coordonnées de texture en dehors de cette plage n’est pas valide. La même restriction s’applique aux coordonnées de texture générées suite à la génération automatique des coordonnées de texture et aux transformations de coordonnées de texture.

L’interprétation de **MaxTextureRepeat** est également affectée par le \_ bit de capacité D3DPTEXTURECAPS TEXREPEATNOTSCALEDBYSIZE. Lorsque ce bit est défini, la valeur du membre **MaxTextureRepeat** est utilisée précisément comme décrit. Toutefois, lorsque D3DPTEXTURECAPS \_ TEXREPEATNOTSCALEDBYSIZE n’est pas défini, les limitations de répétition de texture dépendent de la taille de la texture indexée par les coordonnées de texture. Dans ce cas, **MaxTextureRepeat** doit être mis à l’échelle par la taille de texture actuelle au plus grand niveau de détail pour calculer la plage de coordonnées de texture valide. Par exemple, étant donné une dimension de texture 32 et **MaxTextureRepeat** de 512, la plage de coordonnées de texture réelle valide est 512/32 = 16, donc les coordonnées de texture pour cet appareil doivent être comprises dans la plage de-16,0 à + 16,0.

Les rubriques suivantes contiennent des informations supplémentaires sur les modes d’adressage de la texture.

-   [Mode d’adressage de texture de retour à la ligne (Direct3D 9)](wrap-texture-address-mode.md)
-   [Mode d’adresse de texture miroir (Direct3D 9)](mirror-texture-address-mode.md)
-   [Mode d’adresse de texture clamp (Direct3D 9)](clamp-texture-address-mode.md)
-   [Mode d’adresse de la texture de couleur de la bordure (Direct3D 9)](border-color-texture-address-mode.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de base de la texturation](basic-texturing-concepts.md)
</dt> </dl>

 

 
