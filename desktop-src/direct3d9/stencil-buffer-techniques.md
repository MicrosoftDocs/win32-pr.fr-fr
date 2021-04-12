---
description: Les applications utilisent la mémoire tampon de stencil pour masquer les pixels dans une image. Le masque détermine si le pixel est dessiné ou non. Certains des effets les plus courants sont présentés ci-dessous.
ms.assetid: 984f0a98-4a74-44c3-a9d0-f5d3f12f7e4e
title: Techniques de tampon de stencil (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2dcc05475a3ddfc13e456faf60ec2d11e271a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392883"
---
# <a name="stencil-buffer-techniques-direct3d-9"></a>Techniques de tampon de stencil (Direct3D 9)

Les applications utilisent la mémoire tampon de stencil pour masquer les pixels dans une image. Le masque détermine si le pixel est dessiné ou non. Certains des effets les plus courants sont présentés ci-dessous.

-   [Composition](compositing.md)
-   [Décalque](decaling.md)
-   [Dissoudre, fondu et balayage](dissolves--fades--and-swipes.md)
-   [Plans et silhouettes](outlines-and-silhouettes.md)
-   [Stencil recto-verso](two-sided-stencil.md)

La mémoire tampon de stencil active ou désactive le dessin sur la surface de la cible de rendu pixel par pixel. À son niveau le plus fondamental, il permet aux applications de masquer les sections de l’image rendue afin qu’elles ne soient pas affichées. Les applications utilisent souvent des mémoires tampons stencil pour des effets spéciaux, tels que les dissolutions, le décalque et le mode plan.

Les informations de tampon de stencil sont incorporées dans les données de la mémoire tampon z. Votre application peut utiliser la méthode [**IDirect3D9 :: CheckDeviceFormat**](/windows/desktop/api) pour vérifier la prise en charge des stencils matériels, comme illustré dans l’exemple de code suivant.


```
// Reject devices that cannot perform 8-bit stencil buffering. 
// The following example assumes that pCaps is a valid pointer 
// to an initialized D3DCAPS9 structure. 

if( FAILED( m_pD3D->CheckDeviceFormat( pCaps->AdapterOrdinal,
                                       pCaps->DeviceType,  
                                       Format,  
                                       D3DUSAGE_DEPTHSTENCIL, 
                                       D3DRTYPE_SURFACE,
                                       D3DFMT_D24S8 ) ) )
return E_FAIL;
```



[**IDirect3D9 :: CheckDeviceFormat**](/windows/desktop/api) vous permet de choisir un appareil à créer en fonction des fonctionnalités de cet appareil. Dans ce cas, les appareils qui ne prennent pas en charge les mémoires tampons de stencil 8 bits sont rejetés. Notez qu’il ne s’agit que d’une seule utilisation possible pour **IDirect3D9 :: CheckDeviceFormat**; Pour plus d’informations, consultez Détermination de la [prise en charge matérielle (Direct3D 9)](determining-hardware-support.md).

## <a name="how-the-stencil-buffer-works"></a>Fonctionnement de la mémoire tampon de stencil

Direct3D effectue un test sur le contenu de la mémoire tampon de stencil pixel par pixel. Pour chaque pixel de la surface cible, il effectue un test à l’aide de la valeur correspondante dans la mémoire tampon du stencil, une valeur de référence du stencil et une valeur de masque du stencil. Si le test réussit, Direct3D effectue une action. Le test est effectué à l’aide des étapes suivantes.

1.  Effectue une opération and au niveau du bit de la valeur de référence du stencil avec le masque du gabarit.
2.  Effectue une opération and au niveau du bit de la valeur de mémoire tampon du stencil pour le pixel actuel avec le masque de stencil.
3.  Comparez le résultat de l’étape 1 au résultat de l’étape 2, à l’aide de la fonction de comparaison.

Ces étapes sont présentées dans l’exemple de code suivant.


```
(StencilRef & StencilMask) CompFunc (StencilBufferValue & StencilMask)
```




```
StencilBufferValue
```



est le contenu de la mémoire tampon de stencil pour le pixel actuel. Cet exemple de code utilise le symbole esperluette (&) pour représenter l’opération and au niveau du bit.


```
StencilMask
```



représente la valeur du masque de stencil, et


```
StencilRef
```



représente la valeur de référence du stencil.


```
CompFunc
```



fonction de comparaison.

Le pixel actuel est écrit dans la surface cible si le test du stencil réussit, et est ignoré dans le cas contraire. Le comportement de comparaison par défaut consiste à écrire le pixel, quel que soit le mode de fonctionnement de chaque opération de bits (D3DCMP \_ Always). Vous pouvez modifier ce comportement en modifiant la valeur de l' \_ État de rendu D3DRS STENCILFUNC, en passant un membre du type énuméré [**D3DCMPFUNC**](./d3dcmpfunc.md) pour identifier la fonction de comparaison souhaitée.

Votre application peut personnaliser le fonctionnement de la mémoire tampon de stencil. Elle peut définir la fonction de comparaison, le masque de stencil et la valeur de référence du stencil. Il peut également contrôler l’action effectuée par Direct3D lorsque le test de stencil réussit ou échoue. Pour plus d’informations, consultez état de la [mémoire tampon des stencils (Direct3D 9)](stencil-buffer-state.md).

## <a name="examples"></a>Exemples

Les exemples de code suivants illustrent la configuration de la mémoire tampon de stencil.


```
// Enable stencil testing
pDevice->SetRenderState(D3DRS_STENCILENABLE, TRUE);

// Specify the stencil comparison function
pDevice->SetRenderState(D3DRS_STENCILFUNC, D3DCMP_EQUAL);

// Set the comparison reference value
pDevice->SetRenderState(D3DRS_STENCILREF, 0);

//  Specify a stencil mask 
pDevice->SetRenderState(D3DRS_STENCILMASK, 0);
```



Par défaut, la valeur de référence du stencil est égale à zéro. Toute valeur entière est valide. Direct3D effectue une opération de bits AND de la valeur de référence du stencil et une valeur de masque de stencil avant le test du stencil.

Vous pouvez contrôler les informations de pixels qui sont écrites en fonction de la comparaison du stencil.


```
// A write mask controls what is written
pDevice->SetRenderState(D3DRS_STENCILWRITEMASK, D3DSTENCILOP_KEEP);
// Specify when to write stencil data
pDevice->SetRenderState(D3DRS_STENCILFAIL, D3DSTENCILOP_KEEP);
```



Vous pouvez écrire votre propre formule pour la valeur que vous souhaitez écrire dans la mémoire tampon du stencil, comme indiqué dans l’exemple suivant.


```
NewStencilBufferValue = (StencilBufferValue & ~StencilWriteMask) | 
                        (StencilWriteMask & StencilOp(StencilBufferValue))
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline de pixels](pixel-pipeline.md)
</dt> </dl>

 

 
