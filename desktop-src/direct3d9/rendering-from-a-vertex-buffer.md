---
description: 'Le rendu des données de vertex à partir d’une mémoire tampon de vertex requiert quelques étapes. Tout d’abord, vous devez définir la source du flux en appelant la méthode IDirect3DDevice9 :: SetStreamSource, comme indiqué dans l’exemple suivant.'
ms.assetid: a0435a3d-e1dd-4365-904d-8e5713e379ce
title: Rendu à partir d’une mémoire tampon de vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cebb68c5395a827a9aee4ea1f8465257c436bb7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108454"
---
# <a name="rendering-from-a-vertex-buffer-direct3d-9"></a>Rendu à partir d’une mémoire tampon de vertex (Direct3D 9)

Le rendu des données de vertex à partir d’une mémoire tampon de vertex requiert quelques étapes. Tout d’abord, vous devez définir la source du flux en appelant la méthode [**IDirect3DDevice9 :: SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) , comme indiqué dans l’exemple suivant.


```
d3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
```



Le premier paramètre de [**IDirect3DDevice9 :: SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) indique à Direct3D la source du flux de données de l’appareil. Le deuxième paramètre est la mémoire tampon de vertex à lier au flux de données. Le troisième paramètre est le décalage entre le début du flux et le début des données du vertex, en octets. Le quatrième paramètre correspond au Stride du composant, en octets. Dans l’exemple de code ci-dessus, la taille d’un CUSTOMVERTEX est utilisée pour le Stride du composant.

L’étape suivante consiste à informer Direct3D du nuanceur de sommets à utiliser en appelant la méthode [**IDirect3DDevice9 :: SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) . L’exemple de code suivant définit un code de Commission sur le prix final pour le nuanceur de sommets. Cela informe Direct3D des types de vertex qu’il traite.


```
d3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
```



Après la définition de la source de flux et du nuanceur de sommets, toute méthode de dessin utilisera la mémoire tampon de vertex. L’exemple de code ci-dessous montre comment restituer des vertex à partir d’une mémoire tampon de vertex avec la méthode [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .


```
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 1 );
```



Le deuxième paramètre que [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) accepte est l’index du premier vecteur dans la mémoire tampon de vertex à charger.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons de vertex](vertex-buffers.md)
</dt> <dt>

[Rendu à partir de mémoires tampons de vertex et d’index (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> </dl>

 

 
