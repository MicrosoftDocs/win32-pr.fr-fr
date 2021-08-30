---
title: dcl_input_sv (SM4-ASM)
description: '\_SV entrée DCL \_ (SM4-ASM)'
ms.assetid: 59270148-e2eb-4525-a888-ad7e843d62a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b703677bb4e99f70443c89a8f907fa7abfaaff11
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481265"
---
# <a name="dcl_input_sv-sm4---asm"></a>\_SV entrée DCL \_ (SM4-ASM)

Déclare un registre d’entrée de nuanceur qui attend qu’une [valeur système](dx-graphics-hlsl-semantics.md) soit fournie à partir d’une étape précédente.



| \_entrée DCL \_ SV v *N \[ . Mask \]*, *systemValueName \[ , interpolationMode \]* |
|------------------------------------------------------------------------|



 




| Élément | Description | 
|------|-------------|
| <span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [. masque]</em><br /> | dans Registre de données de vertex. <br /><ul><li><em>N</em> est un entier qui identifie le numéro du Registre.</li><li><em>[. Mask]</em> est un masque de composant facultatif (. XYZW) qui spécifie les composants Register à utiliser.</li></ul> | 
| <span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemValueName</em><br /> | dans Nom de la valeur système qui est une chaîne (voir <a href="dx-graphics-hlsl-semantics.md">sémantique de valeur système</a>) sans le préfixe « SV_ ».<br /> | 
| <span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em><br /> | [in] Facultatif. Mode d’interpolation qui affecte la façon dont les valeurs sont calculées lors de la pixellisation. le mode est utilisé uniquement par un nuanceur de pixels. Ce peut être l’une des valeurs suivantes : <br /><ul><li>constant : n’effectue pas d’interpolation entre les valeurs de registre.</li><li>linéaire-interpolation linéaire entre les valeurs de registre.</li><li>linearCentroid-identique à Linear, mais au centre de gravité de l’échantillonnage.</li><li>linearNoperspective : identique à linéaire, mais sans correction de perspective.</li><li>linearNoperspectiveCentroid-identique à Linear, mais sans correction de perspective et de centre de gravité lors de l’échantillonnage multiple.</li></ul> | 




 

Un masque de composant pour une déclaration de valeur système peut être n’importe quel sous-ensemble approprié de \[ XYZW \] ; les déclarations peuvent ne pas se chevaucher (chaque déclaration doit suivre la séquence XYZW). Lorsque vous déclarez des valeurs de système scalaires (distance de découpage et distance de Culling par exemple), vous pouvez déclarer plusieurs valeurs système dans un seul registre. Dans ce cas, assurez-vous que les autres modificateurs comme les modes d’interpolation correspondent.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.

## <a name="example"></a>Exemple

Voici quelques exemples :


```
// valid
dcl_input v0.y, linear
dcl_input_sv v0.w, clipDistance
dcl_input_sv v0.z, cullDistance
```




```
// invalid declarations
dcl_input v0.y, linear
dcl_input_sv v0.x, clipDistance  // the y component was previously declared, this declaration must use 
                                 // either the z or w component

dcl_input v0.y, linearNoPerspective                  // the interpolation mode is linear-no-perspective
dcl_input_sv v0.z, renderTargetArrayIndex, constant  // the interpolation modes is constant
                                                     // the interpolation modes must match
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

 

 





