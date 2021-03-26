---
title: Load (objet texture HLSL DirectX)
description: Lit les données Texel sans aucun filtrage ni échantillonnage.
ms.assetid: a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 08d3964788a238492ff7d5189544603b35808465
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/05/2021
ms.locfileid: "104108379"
---
# <a name="load-directx-hlsl-texture-object"></a>Load (objet texture HLSL DirectX)

Lit les données Texel sans aucun filtrage ni échantillonnage.



<table>
<tbody>
<tr class="odd">
<td>RET Object. Load (<dl> Emplacement typeX,<br />
[typeX SampleIndex,]<br />
[décalage typeX]<br />
</dl>);</td>
</tr>
</tbody>
</table>

typeX indique qu’il existe quatre types possibles : **int**, **Int2**, **Int3** ou **INT4**.

 

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Dessin*
</dt> <dd>

Un type d' [objet texture](dx-graphics-hlsl-to-type.md) (à l’exception de TextureCube ou TextureCubeArray).

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Emplacement*
</dt> <dd>

\[dans \] les coordonnées de texture, le dernier composant spécifie le niveau de mipmap. Cette méthode utilise un système de coordonnées de base 0 et non un système UV 0.0-1.0. Le type d’argument est dépendant du type de texture-objet.



| Type d'objet                                  | Type de paramètre |
|----------------------------------------------|----------------|
| Buffer                                       | int            |
| Texture1D, Texture2DMS                       | int2           |
| Texture1DArray, texture 2D, Texture2DMSArray | int3           |
| Texture2DArray, Texture3D                    | int4           |



 

Par exemple, pour accéder à une texture 2D, fournissez des coordonnées UV pour les deux premiers composants et un niveau mipmap pour le troisième composant.

> [!Note]  
> Lorsqu’une ou plusieurs des coordonnées de l' *emplacement* dépassent les dimensions de niveau mipmap u, v ou w de la texture, la fonction **Load** retourne zéro dans tous les composants. Direct3D garantit de retourner zéro pour toute ressource qui est accessible à partir de limites.

 

</dd> <dt>

<span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*
</dt> <dd>

\[dans \] un index d’échantillonnage facultatif.



| Type de texture                                                                                                   | Type de paramètre |
|----------------------------------------------------------------------------------------------------------------|----------------|
| Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, TextureCube, TextureCubeArray | non pris en charge  |
| Texture2DMS, Texture2DMSArray ¹                                                                                 | int            |



 

> [!Note]  
> *SampleIndex* est disponible uniquement pour les textures à plusieurs échantillons.

 

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Décalage*
</dt> <dd>

\[dans \] un offset facultatif appliqué aux coordonnées de texture avant l’échantillonnage. Le type de décalage est dépendant du type de texture-objet et doit être statique.



| Type de texture                                             | Type de paramètre |
|----------------------------------------------------------|----------------|
| Texture1D, Texture1DArray                                | int            |
| Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray | int2           |
| Texture3D, Texture2DArray                                | int3           |



 

> [!Note]  
> Si vous utilisez *offset* avec des textures à échantillons multiples, vous devez également spécifier *SampleIndex*.

 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Le type de retour correspond au type dans la déclaration de l' *objet* . Par exemple, un objet Texture2D qui a été déclaré comme « Texture2d <uint4> myTexture ; » a une valeur de retour de type **uint4**.

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1 ¹ | PS \_ 4 \_ 0 | PS \_ 4 \_ 1 ¹ | GS \_ 4 \_ 0 | GS \_ 4 \_ 1 ¹ |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

-   Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.

## <a name="example"></a>Exemple

Cet exemple de code partiel provient du fichier Paint. fx dans l' [exemple AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).


```
// Object Declarations
Buffer<float4> g_ParticleBuffer;

// Shader body calling the intrinsic function
float4 PSPaint(PSQuadIn input) : SV_Target
{       
    ... 
    for( int i=g_ParticleStart; i<g_NumParticles; i+=g_ParticleStep )
    {
        ... 
        // load the particle
        float4 particlePos = g_ParticleBuffer.Load( i*4 );
        float4 particleColor = g_ParticleBuffer.Load( (i*4) + 2 );
        ...     
    }
    ...
}   
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Texture-objet](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 




