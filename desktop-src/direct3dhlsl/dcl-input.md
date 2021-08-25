---
title: dcl_input (SM4-ASM)
description: '\_entrée DCL (SM4-ASM)'
ms.assetid: 13456f2a-ee6c-42da-a9fe-670ab0fcbddf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8214287a4afb4c683a94e213cdfed133c03219e2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467006"
---
# <a name="dcl_input-sm4---asm"></a>\_entrée DCL (SM4-ASM)

Déclare un registre d’entrée de nuanceur.



| \_entrée DCL v *N \[ . Mask \] \[ , interpolationMode \]* |
|-------------------------------------------------|



 




| Élément | Description | 
|------|-------------|
| <span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [. masque]</em><br /> | dans Registre de données de vertex. <br /><ul><li><em>N</em> est un entier qui identifie le numéro du Registre.</li><li><em>[. Mask]</em> est un masque de composant facultatif (. XYZW) qui spécifie les composants Register à utiliser.</li></ul> | 
| <span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em><br /> | [in] Facultatif. Mode d’interpolation, qui est respecté uniquement sur les registres d’entrée de nuanceur de pixels. Ce peut être l’une des valeurs suivantes : <br /><ul><li>constant : n’effectue pas d’interpolation entre les valeurs de registre.</li><li>linéaire-interpolation linéaire entre les valeurs de registre.</li><li>linearCentroid-identique à Linear, mais au centre de gravité de l’échantillonnage.</li><li>linearNoperspective : identique à linéaire, mais sans correction de perspective.</li><li>linearNoperspectiveCentroid-identique à Linear, centre de gravité de l’échantillonnage, sans correction de perspective.</li></ul> | 




 

### <a name="interpolation-notes"></a>Remarques sur l’interpolation

Par défaut, les attributs de vertex sont interpolés à partir d’un centre de pixels lors de l’exécution de l’anticrénelage multiéchantillonne. Si un centre de pixels n’est pas couvert, un attribut est extrapolé à un centre de pixels avant l’interpolation.

Pour un pixel qui n’est pas entièrement couvert ou un attribut qui ne couvre pas un centre de pixels, vous pouvez spécifier un échantillonnage de centre de gravité qui force l’échantillonnage à quelque endroit que ce soit dans la zone couverte du pixel. Étant donné qu’un exemple de masque (s’il est utilisé) est appliqué avant le calcul du centre de gravité, tout emplacement d’échantillonnage masqué par l’exemple de masque ne peut pas être choisi comme emplacement de centre de gravité.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Pour identifier l’entrée en tant que valeur système, utilisez l' [ \_ entrée DCL \_ (SM4-ASM)](dcl-input-sv.md).

Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.

## <a name="example"></a>Exemple

Voici quelques exemples.


```
dcl_input v3.xyz

dcl_input v0.x, linearCentroid
```



## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | Oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





