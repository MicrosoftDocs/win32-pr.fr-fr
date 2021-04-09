---
description: Une étape de fusion est un ensemble d’opérations de texture et leurs arguments qui définissent la façon dont les textures sont mélangées.
ms.assetid: 7f9e3041-a270-44a9-a8e1-bca5ea25a71e
title: Création de phases de fusion (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f5029d540433b22b1380435dd8092546917338
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110766"
---
# <a name="creating-blending-stages-direct3d-9"></a>Création de phases de fusion (Direct3D 9)

Une étape de fusion est un ensemble d’opérations de texture et leurs arguments qui définissent la façon dont les textures sont mélangées. Lors d’une phase de fusion, les applications C++ appellent la méthode [**IDirect3DDevice9 :: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) . Le premier appel spécifie l’opération qui est effectuée. Deux appels supplémentaires définissent les arguments auxquels l’opération est appliquée. L’exemple de code suivant illustre la création d’une étape de fusion.


```
// This example assumes that lpD3DDev is a valid pointer to an
// IDirect3DDevice9 interface.

// Set the operation for the first texture.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_ADD);

// Set argument 1 to the texture color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);

// Set argument 2 to the iterated diffuse color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);
```



Les données de Texel dans les textures contiennent des valeurs de couleur et alpha. Les applications peuvent définir des opérations distinctes pour les valeurs de couleur et alpha dans une phase de fusion unique. Chaque opération, couleur et alpha possède ses propres arguments. Pour plus d’informations, consultez [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).

Bien qu’il ne fasse pas partie de l’API Direct3D, vous pouvez insérer les macros suivantes dans votre application pour abréger le code requis pour créer des étapes de fusion de texture.


```
#define SetTextureColorStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_COLOROP, op);      \
    dev->SetTextureStageState( i, D3DTSS_COLORARG1, arg1 ); \
    dev->SetTextureStageState( i, D3DTSS_COLORARG2, arg2 );

#define SetTextureAlphaStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_ALPHAOP, op);      \
    dev->SetTextureStageState( i, D3DTSS_ALPHAARG1, arg1 );  \
    dev->SetTextureStageState( i  D3DTSS_ALPHAARG2, arg2 );
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fusion de texture](texture-blending.md)
</dt> </dl>

 

 
