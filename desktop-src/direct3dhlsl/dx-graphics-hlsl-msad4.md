---
title: msad4
description: Compare une valeur de référence de 4 octets et une valeur source de 8 octets et accumule un vecteur de 4 sommes. Chaque somme correspond à la somme masquée de différences absolues d’un alignement d’octets différent entre la valeur de référence et la valeur source.
ms.assetid: 6497F9AE-4524-44C2-A1C6-2A4ACB30FA9C
keywords:
- HLSL msad4
topic_type:
- apiref
api_name:
- msad4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 552db3afd07677777b47e939d659c0f6e333e496
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295035"
---
# <a name="msad4"></a>msad4

Compare une valeur de référence de 4 octets et une valeur source de 8 octets et accumule un vecteur de 4 sommes. Chaque somme correspond à la somme masquée de différences absolues d’un alignement d’octets différent entre la valeur de référence et la valeur source.



| uint4 result = msad4 (référence uint, source uint2, uint4 cumuler); |
|------------------------------------------------------------------|



 

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="reference"></span><span id="REFERENCE"></span>*faire*
</dt> <dd>

\[dans \] le tableau de référence de 4 octets dans une valeur **uint** .

</dd> <dt>

<span id="source"></span><span id="SOURCE"></span>*code*
</dt> <dd>

\[dans \] le tableau source de 8 octets dans deux valeurs **uint2** .

</dd> <dt>

<span id="accum"></span><span id="ACCUM"></span>*cumuleur*
</dt> <dd>

\[dans \] un vecteur de 4 valeurs. **msad4** ajoute ce vecteur à la somme masquée de différences absolues des différents alignements d’octets entre la valeur de référence et la valeur source.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Vecteur de 4 sommes. Chaque somme correspond à la somme masquée de différences absolues d’alignements d’octets différents entre la valeur de référence et la valeur source. **msad4** n’inclut pas de différence dans la somme si cette différence est masquée (autrement dit, l’octet de référence est 0).

## <a name="remarks"></a>Notes

Pour utiliser l’intrinsèque **msad4** dans le code de votre nuanceur, appelez la méthode [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) avec la [**\_ fonctionnalité d3d11 \_ d3d11 \_ options**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) pour vérifier que l’appareil Direct3D prend en charge l’option de fonctionnalité [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) . L’intrinsèque **msad4** requiert un pilote d’affichage WDDM 1,2, et tous les pilotes d’affichage WDDM 1,2 doivent prendre en charge **msad4**. Si votre application crée un appareil de rendu avec le [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 ou 11,1 et que la cible de compilation est Shader Model 5 ou version ultérieure, le code source HLSL peut utiliser l’intrinsèque **msad4** .

Les valeurs de retour sont uniquement précises jusqu’à 65535. Si vous appelez l’intrinsèque **msad4** avec des entrées qui peuvent entraîner des valeurs de retour supérieures à 65535, **msad4** produit des résultats non définis.

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                | Prise en charge |
|-------------------------------------------------------------|-----------|
| [Shader Model 5 ou version ultérieure](d3d11-graphics-reference-sm5.md) | Oui       |



 

## <a name="examples"></a>Exemples

Voici un exemple de calcul des résultats pour **msad4**:


```
reference = 0xA100B2C3;
source.x = 0xD7B0C372
source.y = 0x4F57C2A3
accum = {1,2,3,4}
result.x alignment source: 0xD7B0C372
result.x = accum.x + |0xD7   0xA1| + 0 (masked) + |0xC3   0xB2| + |0x72   0xC3| = 1 + 54 + 0 + 17 + 81 = 153
result.y alignment source: 0xA3D7B0C3
result.y = accum.y + |0xA3   0xA1| + 0 (masked) + |0xB0   0xB2| + |0xC3   0xC3| = 2 + 2 + 0 + 2 + 0 = 6
result.z alignment source: 0xC2A3D7B0
result.z = accum.z + |0xC2   0xA1| + 0 (masked) + |0xD7   0xB2| + |0xB0   0xC3| = 3 + 33 + 0 + 37 + 19 = 92
result.w alignment source: 0x57C2A3D7
result.w = accum.w + |0x57   0xA1| + 0 (masked) + |0xA3   0xB2| + |0xD7   0xC3| = 4 + 74 + 0 + 15 + 20 = 113
result = {153,6,92,113}
```



Voici un exemple de la façon dont vous pouvez utiliser **msad4** pour rechercher un modèle de référence dans une mémoire tampon :


```
uint4 accum = {0,0,0,0};
for(uint i=0;i<REF_SIZE;i++)
    accum = msad4(
        buf_ref[i], 
        uint2(buf_src[DTid.x+i], buf_src[DTid.x+i+1]), 
        accum);
buf_accum[DTid.x] = accum;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>           |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

