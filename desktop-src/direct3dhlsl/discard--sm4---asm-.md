---
title: ignorer (SM4-ASM)
description: Marquez de manière conditionnelle les résultats du nuanceur de pixels à ignorer lorsque la fin du programme est atteinte.
ms.assetid: 566C4A9A-B32A-4AA6-A888-70F6965B1B5A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d98365ae6d80710f15cf7204f98d810be30a13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103940563"
---
# <a name="discard-sm4---asm"></a>ignorer (SM4-ASM)

Marquez de manière conditionnelle les résultats du nuanceur de pixels à ignorer lorsque la fin du programme est atteinte.



| ignorer { \_ z \|\_NZ} src0. sélectionner le \_ composant |
|-------------------------------------------|



 



| Élément                                                            | Description                                                                                       |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[\]valeur qui détermine s’il faut ignorer le pixel actuel en cours de traitement.<br/> |



 

## <a name="remarks"></a>Notes

Cette instruction marque le pixel actuel comme terminé, tout en continuant son exécution, afin que les autres pixels s’exécutant en parallèle peuvent obtenir des dérivées si nécessaire. Même si l’exécution se poursuit, toute la sortie du nuanceur de pixels écrit avant ou après l’instruction **ignorée** .

Pour **Ignorer \_ z**, si tous les bits dans *src0. Select \_ Component* sont nuls, le pixel est ignoré.

Pour **ignorer la \_ NZ**, si des bits dans *src0. Select \_ Component* sont différent de zéro, le pixel est ignoré.

En outre, l’instruction **Discard** peut être présente à l’intérieur d’une construction de contrôle de Flow.

Plusieurs instructions **ignorées** peuvent être présentes dans un nuanceur et, si un est exécuté, le pixel est arrêté.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | Oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





