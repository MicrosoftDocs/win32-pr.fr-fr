---
title: firstbit (SM5-ASM)
description: Recherche le premier bit défini dans un nombre, soit à partir de LSB, soit à l’octet MSB.
ms.assetid: E3066676-5218-470A-944A-7B221E1BF64D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b88fa9291ce64fcc8c94510bd09bed31e7b7f96
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313747"
---
# <a name="firstbit-sm5---asm"></a>firstbit (SM5-ASM)

Recherche le premier bit défini dans un nombre, soit à partir de LSB, soit à l’octet MSB.



| firstbit { \_ Hi \|\_Lo|\_Chi} dest \[ . Mask \] , src0 \[ . Swizzle\] |
|-------------------------------------------------------------|



 



| Élément                                                            | Description                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[dans \] la position entière du premier bit défini dans *src0* à partir de LSB pour FIRSTBIT \_ Lo ou MSB pour firstbit \_ Hi.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] l’entier d’entrée.<br/>                                                                                                  |



 

## <a name="remarks"></a>Notes

Cette opération retourne la position entière du premier bit défini dans l’entrée 32 bits à partir de LSB pour firstbit \_ Lo ou MSB pour firstbit \_ Hi. Par exemple \_ , firstbit Lo sur 0x00000001 retourne 0. firstbit \_ Hi sur 0x10000000 retourne 3.

firstbit \_ Chi (s pour signed) retourne le premier 0 de l’MSB si le nombre est négatif ; sinon, il retourne les 1 premiers du MSB.

Toutes les variantes de l’instruction retournent ~ 0 (0xFFFFFFFF dans le registre 32 bits) si aucune correspondance n’est trouvée.

Utilisez cette instruction pour énumérer rapidement les bits Set dans un champ de bits ou pour trouver la puissance la plus grande de 2 dans un nombre.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="mimimum-shader-model"></a>Modèle de nuanceur minimal

Cette instruction est prise en charge dans les modèles de nuanceur suivants :



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | non        |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





