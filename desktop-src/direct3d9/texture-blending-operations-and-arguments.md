---
description: Les applications associent une phase de fusion à chaque texture dans le jeu de textures actuelles. Direct3D évalue chaque étape de fusion dans l’ordre, en commençant par la première texture du jeu et en finissant par le huitième.
ms.assetid: 3b7faefd-30be-4f74-b0f7-621d65130286
title: Opérations et arguments de fusion de texture (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d242092de5919267d30a9b8ff4e7bd2324f0bc3120649d3bb1a423b3462be77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797771"
---
# <a name="texture-blending-operations-and-arguments-direct3d-9"></a>Opérations et arguments de fusion de texture (Direct3D 9)

Les applications associent une phase de fusion à chaque texture dans le jeu de textures actuelles. Direct3D évalue chaque étape de fusion dans l’ordre, en commençant par la première texture du jeu et en finissant par le huitième.

Direct3D applique les informations de chaque texture de l’ensemble des textures actuelles à la phase de fusion qui lui est associée. Les applications contrôlent les informations d’une étape de texture qui sont utilisées en appelant [**IDirect3DDevice9 :: SetTextureStageState**](/windows/desktop/api). Vous pouvez définir des opérations distinctes pour la couleur et les canaux alpha, et chaque opération utilise deux arguments. Spécifiez les opérations de canal de couleur à l’aide de l' \_ État D3DTSS COLOROP stage. spécifiez des opérations alpha à l’aide de D3DTSS \_ ALPHAOP. Les deux États d’étape utilisent des valeurs du type énuméré [**D3DTEXTUREOP**](./d3dtextureop.md) .

Les arguments de fusion de texture utilisent les \_ membres D3DTSS COLORARG1, D3DTSS \_ COLORARG2, D3DTSS \_ ALPHARG1 et D3DTSS ALPHARG2 \_ du type énuméré [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) . Les valeurs d’argument correspondantes sont identifiées à l’aide de [D3DTA](d3dta.md).

> [!Note]  
> Vous pouvez désactiver une étape de texture, ainsi que toutes les étapes suivantes de fusion de texture dans le cascade, en définissant l’opération de couleur pour cette étape sur D3DTOP \_ Désactiver. La désactivation de l’opération de couleur désactive efficacement également l’opération alpha. Les opérations alpha ne peuvent pas être désactivées lorsque les opérations de couleur sont activées. La définition de l’opération alpha sur D3DTOP \_ désactive lorsque la fusion de couleurs est activée entraîne un comportement indéfini.

 

Pour déterminer les opérations de fusion de texture prises en charge d’un appareil, interrogez le membre TextureCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fusion de texture](texture-blending.md)
</dt> </dl>

 

 
