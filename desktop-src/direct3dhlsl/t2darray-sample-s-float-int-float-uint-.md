---
title: 'Texture2DArray :: Sample (S, float, int, float, uint), fonction'
description: 'Échantillonne une texture avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à et retourne l’état de l’opération. | Texture2DArray :: Sample (S, float, int, float, uint), fonction'
ms.assetid: 0F9DBC0D-F35D-4A7A-B8F5-1EFBF7E14615
keywords:
- Exemple de fonction HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1ab3d0f6afefe162463a70e213226d1d363901bb4398d3fcbc0d3b6baa36e588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043507"
---
# <a name="texture2darraysamplesfloatintfloatuint-function"></a>Texture2DArray :: Sample (S, float, int, float, uint), fonction

Échantillonne une texture avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à et retourne l’état de l’opération.

## <a name="syntax"></a>Syntaxe


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

 \[ Dans\]
</dt> <dd>

État de l' [échantillonneur](dx-graphics-hlsl-sampler.md). Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.

</dd> <dt>

*Emplacement* \[ dans\]
</dt> <dd>

Coordonnées de texture. Le type d’argument est dépendant du type de texture-objet.



| Type de Texture-Object                    | Type de paramètre |
|----------------------------------------|----------------|
| Texture1D                              | float          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*Décalage* \[ dans\]
</dt> <dd>

Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage. Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel. Le type d’argument est dépendant du type de texture-objet. Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).



| Type de Texture-Object           | Type de paramètre |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | int            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | non pris en charge  |



 

</dd> <dt>

*Clamp* \[ dans\]
</dt> <dd>

Valeur facultative pour fixer l’exemple de valeurs LOD à. Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.

</dd> <dt>

*État* \[ à\]
</dt> <dd>

État de l'opération. Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features). Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Exemples de méthodes](texture2darray-sample.md)
</dt> </dl>

 

 
