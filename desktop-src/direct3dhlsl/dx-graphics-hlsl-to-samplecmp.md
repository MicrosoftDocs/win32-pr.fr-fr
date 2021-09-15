---
title: SampleCmp (objet texture HLSL DirectX)
description: Échantillonne une texture et compare un composant unique à la valeur de comparaison spécifiée.
ms.assetid: e21894c4-e8c5-4c3d-92c1-727964f8fd94
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6991bead4bfc42451c26fe5476b4c114626eb7e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524640"
---
# <a name="samplecmp-directx-hlsl-texture-object"></a>SampleCmp (objet texture HLSL DirectX)

Échantillonne une texture et compare un composant unique à la valeur de comparaison spécifiée.

<table>
<tbody>
<tr class="odd">
<td>float Object. SampleCmp ( <dl> SamplerComparisonState S,<br />
Emplacement flottant,<br />
float CompareValue,<br />
[décalage int]<br />
</dl>);</td>
</tr>
</tbody>
</table>
 

La comparaison est une comparaison à un seul composant entre le premier composant stocké dans la texture et la valeur de comparaison transmise dans la méthode.

Cette méthode peut être appelée uniquement à partir d’un nuanceur de pixels ; elle n’est pas prise en charge dans un nuanceur de sommets ou de géométrie.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Dessin*
</dt> <dd>

Tout type d' [objet texture](dx-graphics-hlsl-to-type.md) (à l’exception de Texture2DMS, Texture2DMSArray ou Texture3D).

</dd> <dt>

<span id="S"></span><span id="s"></span>*X*
</dt> <dd>

\[dans \] un état de comparaison d’échantillonneur, qui est l’état de l’échantillonneur plus un état de comparaison (une fonction de comparaison et un filtre de comparaison). Pour plus d’informations et pour obtenir un exemple, consultez [type d’échantillonneur](dx-graphics-hlsl-sampler.md) .

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Emplacement*
</dt> <dd>

\[dans \] les coordonnées de texture. Le type d’argument est dépendant du type de texture-objet.

| Type de Texture-Object          | Type de paramètre |
|------------------------------|----------------|
| Texture1D                    | float          |
| Texture1DArray, Texture2D    | float2         |
| Texture2DArray ¹, TextureCube | float3         |
| TextureCubeArray ¹            | float4         |

</dd> <dt>

<span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*
</dt> <dd>

Valeur à virgule flottante à utiliser comme valeur de comparaison.

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Décalage*
</dt> <dd>

\[dans \] un décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; le décalage est appliqué à l’emplacement avant l’échantillonnage. Les décalages de texture doivent être statiques. Le type d’argument est dépendant du type de texture-objet. Pour plus d’informations, consultez [application de décalages de coordonnées de texture](dx-graphics-hlsl-to-sample.md).

| Type de Texture-Object            | Type de paramètre |
|--------------------------------|----------------|
| Texture1D, Texture1DArray      | int            |
| Texture2D, Texture2DArray ¹     | int2           |
| TextureCube, TextureCubeArray ¹ | Non pris en charge  |

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur à virgule flottante dans la plage \[ 0.. 1 \] .

Pour chaque élément Texel récupéré (en fonction de la configuration de l’échantillonneur du mode filtre), **SampleCmp** effectue une comparaison de la valeur z (le troisième composant de l’entrée) du nuanceur à la valeur Texel (1 si la comparaison réussit ; sinon, 0). **SampleCmp** fusionne ensuite ces résultats 0 et 1 pour chaque Texel ensemble comme dans le filtrage de texture normal (et non en moyenne) et retourne la \[ valeur 0.. 1 obtenue \] au nuanceur.

## <a name="remarks"></a>Notes

Le filtrage de comparaison fournit une opération de filtrage de base qui est utile pour le filtrage en pourcentage plus profond.

Lors de l’utilisation de cette méthode sur une ressource à virgule flottante (au lieu d’un format normalisé normalisé ou non signé), la valeur de comparaison n’est pas automatiquement ancrée entre 0,0 et 1,0. Par conséquent, une fixation manuelle de la valeur de comparaison peut être nécessaire pour les techniques d’occultation courantes.

Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats différents en fonction de l’implémentation matérielle ou des paramètres du pilote.

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.

| vs \_ 4 \_ 0 | vs \_ 4 \_ 1 ² | PS \_ 4 \_ 0 | PS \_ 4 \_ 1 ² | GS \_ 4 \_ 0 | GS \_ 4 \_ 1 ² |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | x ¹       | x         |          |           |

1.  Texture2DArray et TextureCubeArray sont disponibles dans le modèle de nuanceur 4,1 ou version ultérieure.
2.  Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.

> [!NOTE]  
> **SampleCmp** est également disponible dans PS 4 \_ 0 \_ Level \_ 9 \_ 1 et 4 \_ 0 \_ Level \_ 9 \_ 3 lorsque vous utilisez les techniques décrites dans implémentation de [mémoires tampons secondaires pour la fonctionnalité Direct3D de niveau 9](/previous-versions/windows/apps/jj262110(v=win.10)).

## <a name="related-topics"></a>Rubriques connexes

[Texture-objet](dx-graphics-hlsl-to-type.md)
