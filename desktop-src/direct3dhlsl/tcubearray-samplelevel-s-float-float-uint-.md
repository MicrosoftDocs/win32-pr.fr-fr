---
title: 'SampleLevel :: SampleLevel (S, float, float, uint), fonction'
description: 'Échantillonne une texture sur le niveau de mipmap spécifié et retourne l’état de l’opération. | SampleLevel :: SampleLevel (S, float, float, uint), fonction'
ms.assetid: 3794D17F-BC70-4D3A-9F2C-ADF900983D2C
keywords:
- SampleLevel fonction HLSL
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6eb4e4f6d3320bcac06c973ef28e8af0934f3a55da9045f01141157240434fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118284297"
---
# <a name="samplelevelsamplelevelsfloatfloatuint-function"></a>SampleLevel :: SampleLevel (S, float, float, uint), fonction

Échantillonne une texture sur le niveau de mipmap spécifié et retourne l’état de l’opération.

## <a name="syntax"></a>Syntaxe


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  out uint         Status
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

 \[ Dans\]
</dt> <dd>

Type : **SamplerState**

État de l' [échantillonneur](dx-graphics-hlsl-sampler.md). Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.

</dd> <dt>

*Emplacement* \[ dans\]
</dt> <dd>

Type : **float**

Coordonnées de texture. Le type d’argument est dépendant du type de texture-objet.



| Type de Texture-Object                    | Type de paramètre |
|----------------------------------------|----------------|
| Texture1D                              | float          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*LOD* \[ dans\]
</dt> <dd>

Type : **float**

\[dans \] un nombre qui spécifie le niveau de mipmap. Si la valeur est ≤ 0, le mipmap niveau 0 (mappage le plus grand) est utilisé. La valeur fractionnaire (si fournie) est utilisée pour interpoler entre deux niveaux de mipmap.

</dd> <dt>

*État* \[ à\]
</dt> <dd>

Type : **uint**

État de l'opération. Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features). Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes SampleLevel](texturecubearray-samplelevel.md)
</dt> <dt>

[**TextureCubeArray**](texturecubearray.md)
</dt> </dl>

 

 
