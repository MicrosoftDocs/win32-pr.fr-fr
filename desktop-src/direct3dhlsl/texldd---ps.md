---
title: texldd-PS
description: Échantillonne une texture avec d’autres entrées de dégradé.
ms.assetid: 6d6b3180-d82e-4be4-929b-e5a6431bec38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72f3c4aaf9ac7e6beaad1343c024aa28bd2a85ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104381982"
---
# <a name="texldd---ps"></a>texldd-PS

Échantillonne une texture avec d’autres entrées de dégradé.

## <a name="syntax"></a>Syntaxe



| texldd, DST, src0, src1, src2, src3 |
|-------------------------------------|



 

Où :

-   l’heure d’été est un registre de destination.
-   src0 est un registre source qui fournit les coordonnées de texture pour l’échantillon de texture. Consultez [Registre de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).
-   src1 identifie le ou les registres de l’échantillonneur \# de source, où \# spécifie le numéro d’échantillonnage de texture à échantillonner. L’échantillonneur s’est associé à une texture et à un état de contrôle défini par l’énumération [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (par exemple, D3DSAMP \_ MINFILTER).
-   src2 est un registre de source d’entrée qui spécifie le dégradé x.
-   src3 est un registre de source d’entrée qui spécifie le dégradé y.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldd                |      |      |      |      |      | x \* | x     | x    | x     |



 

\* Cette instruction est uniquement prise en charge par PS \_ 2 \_ a. Elle n’est pas prise en charge par PS \_ 2 \_ b. Pour plus d’informations sur les profils, consultez [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile).

Cette instruction échantillonne une texture à l’aide des coordonnées de texture sur src0, l’échantillonneur spécifié par src1 et les dégradés DSX et DSY provenant de src2 et src3. Les valeurs de gradient x et y sont utilisées pour sélectionner le niveau de mipmap approprié de la texture pour l’échantillonnage.

Toutes les sources prennent en charge des Swizzles arbitraires.

Tous les masques d’écriture sont valides sur la destination.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 