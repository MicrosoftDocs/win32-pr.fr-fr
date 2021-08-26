---
description: Les API de présentation sont un ensemble de méthodes qui contrôlent l’état de l’appareil qui affecte ce que l’utilisateur voit sur le moniteur. Ces méthodes incluent la définition de modes d’affichage et de méthodes une fois par image qui sont utilisées pour présenter les images à l’utilisateur.
ms.assetid: fb2ddc0d-50ac-48aa-8a5c-f232b0f8e7aa
title: Présentation de la présentation d’une scène (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9abf584bad1bfbbde2bbfa2e9281acf3ad2173403507e06bbdc2abc5f5edd1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846549"
---
# <a name="introduction-to-presenting-a-scene-direct3d-9"></a>Présentation de la présentation d’une scène (Direct3D 9)

Les API de présentation sont un ensemble de méthodes qui contrôlent l’état de l’appareil qui affecte ce que l’utilisateur voit sur le moniteur. Ces méthodes incluent la définition de modes d’affichage et de méthodes une fois par image qui sont utilisées pour présenter les images à l’utilisateur.

-   [**IDirect3DDevice9 ::P renvoyé**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
-   [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
-   [**IDirect3DDevice9::GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
-   [**IDirect3DDevice9::SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
-   [**IDirect3DDevice9::GetRasterStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)

Vous devez connaître les termes suivants pour comprendre les API de présentation.

-   mémoire tampon d’avant. Rectangle de mémoire qui est traduit par la carte graphique et affiché sur le moniteur ou un autre périphérique de sortie.
-   mémoire tampon d’arrière-plan. Surface dont le contenu peut être promu au tampon d’avant.
-   chaîne de permutation. Collection de mémoires tampons d’arrière-plan qui peuvent être présentées en série au tampon d’avant. En règle générale, une chaîne de permutation plein écran présente les images suivantes avec l’interface de pilote de périphérique (DDI) de basculement, et une chaîne de permutation avec fenêtres présente des images avec l’interface DDI blitting.

Direct3D 9 ayant une chaîne de permutation en tant que propriété de l’appareil, il y a toujours au moins une chaîne de permutation par appareil. L’interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) a un ensemble de méthodes qui manipulent la chaîne de permutation implicite et sont une copie de l’interface propre à la chaîne de permutation. Les applications peuvent créer des chaînes de permutation supplémentaires ; Toutefois, cela n’est pas nécessaire pour l’application typique à fenêtre unique ou en mode plein écran.

Le tampon d’avant n’est pas directement exposé dans Direct3D 9. Par conséquent, les applications ne peuvent pas être verrouillées ou rendues dans le tampon d’avant. Pour plus d’informations, consultez [Accessing the Color front buffer (Direct3D 9)](accessing-the-color-front-buffer.md).

> [!Note]  
> DirectX 7 a fourni un certain nombre d’API de présentation qui ont été appelées ensemble. La séquence IDirectDraw7 :: SetCooperativeLevel, IDirectDraw7 :: SetDisplayMode et IDirectDraw7 :: CreateSurface en est un bon exemple. En outre, les méthodes IDirectDrawSurface7 :: Flip et IDirectDrawSurface7 :: BLT ont signalé le transport des frames rendus vers le moniteur. Direct3D 9 réduit ces groupes d’API en deux méthodes principales, les réinitialiser et les présenter. Réinitialisez subsumes SetCooperativeLevel, SetDisplayMode, CreateSurface et certains des paramètres à retourner. Présente subsumes Flip et la présentation de Blit.

 

Un appel à [**IDirect3D9 :: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) représente une réinitialisation implicite de l’appareil. L’API Direct3D 9 n’a pas de notion d’une surface primaire ; vous ne pouvez pas créer un objet qui représente la surface principale. Il est considéré comme une propriété interne de l’appareil.

Les rampes gamma sont associées à une chaîne de permutation et sont manipulées avec les méthodes [**IDirect3DDevice9 :: GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) et [**IDirect3DDevice9 :: SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Présentation d’une scène](presenting-a-scene.md)
</dt> </dl>

 

 
