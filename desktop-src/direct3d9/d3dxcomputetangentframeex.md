---
description: Effectue des calculs de trame tangente sur une maille. Les vecteurs tangente, Binormal et éventuellement normaux sont générés. Les singularités sont gérées en fonction des besoins en regroupant les bords et en fractionnant les vertex.
ms.assetid: 15cc46bc-6db6-4e1d-a95e-cd60d2666600
title: D3DXComputeTangentFrameEx, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrameEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d091b7ca243e4833cd6aa36a409fca32069e52a267ec3f588b338777ed34338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988669"
---
# <a name="d3dxcomputetangentframeex-function"></a>D3DXComputeTangentFrameEx fonction)

Effectue des calculs de trame tangente sur une maille. Les vecteurs tangente, Binormal et éventuellement normaux sont générés. Les singularités sont gérées en fonction des besoins en regroupant les bords et en fractionnant les vertex.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXComputeTangentFrameEx(
  _In_        ID3DXMesh   *pMesh,
  _In_        DWORD       dwTextureInSemantic,
  _In_        DWORD       dwTextureInIndex,
  _In_        DWORD       dwUPartialOutSemantic,
  _In_        DWORD       dwUPartialOutIndex,
  _In_        DWORD       dwVPartialOutSemantic,
  _In_        DWORD       dwVPartialOutIndex,
  _In_        DWORD       dwNormalOutSemantic,
  _In_        DWORD       dwNormalOutIndex,
  _In_        DWORD       dwOptions,
  _In_  const DWORD       *pdwAdjacency,
  _In_        FLOAT       fPartialEdgeThreshold,
  _In_        FLOAT       fSingularPointThreshold,
  _In_        FLOAT       fNormalEdgeThreshold,
  _Out_       ID3DXMesh   **ppMeshOut,
  _Out_       ID3DXBuffer **ppVertexMapping
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMesh* \[ dans\]
</dt> <dd>

Type : **[ **ID3DXMesh**](id3dxmesh.md)\***

Pointeur vers un objet de maillage [**ID3DXMesh**](id3dxmesh.md) d’entrée.

</dd> <dt>

*dwTextureInSemantic* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Spécifie la sémantique d’entrée de la coordonnée de texture. Si D3DX \_ default, la fonction suppose qu’il n’y a pas de coordonnées de texture, et la fonction échoue à moins que le calcul de vecteur normal soit spécifié.

</dd> <dt>

*dwTextureInIndex* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Si un maillage a plusieurs coordonnées de texture, spécifie la coordonnée de texture à utiliser pour les calculs de frame de tangente. Si la valeur est zéro, le maillage n’a qu’une seule coordonnée de texture.

</dd> <dt>

*dwUPartialOutSemantic* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Spécifie la sémantique de sortie pour le type, généralement D3DDECLUSAGE \_ tangente, qui décrit où la coordonnée partielle par rapport à la coordonnée de la texture U sera stockée. Si \_ la valeur par défaut est D3DX, cette dérivée partielle n’est pas stockée.

</dd> <dt>

*dwUPartialOutIndex* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Spécifie l’index sémantique auquel stocker le dérivée partiel par rapport à la coordonnée de texture U.

</dd> <dt>

*dwVPartialOutSemantic* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Spécifie le type [**D3DDECLUSAGE**](./d3ddeclusage.md) , généralement D3DDECLUSAGE \_ binormal, qui décrit l’emplacement de stockage de la partie dérivée partielle par rapport à la coordonnée de texture V. Si \_ la valeur par défaut est D3DX, cette dérivée partielle n’est pas stockée.

</dd> <dt>

*dwVPartialOutIndex* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Spécifie l’index sémantique au niveau duquel stocker la dérivée partielle par rapport à la coordonnée de texture V.

</dd> <dt>

*dwNormalOutSemantic* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Spécifie la sémantique normale de sortie, généralement D3DDECLUSAGE \_ normal, qui décrit où le vecteur normal à chaque vertex sera stocké. Si \_ la valeur par défaut est D3DX, ce vecteur normal n’est pas stocké.

</dd> <dt>

*dwNormalOutIndex* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Spécifie l’index sémantique à partir duquel stocker le vecteur normal à chaque vertex.

</dd> <dt>

*dwOptions* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’un ou de plusieurs indicateurs [**D3DXTANGENT**](./d3dxtangent.md) qui spécifient des options de calcul de frame tangent. Si la **valeur est null**, les options suivantes sont spécifiées :



| Description                                                                                              | [**D3DXTANGENT**](./d3dxtangent.md) Valeur de l’indicateur                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| Pondérez la longueur du vecteur normal par l’angle, en radians, sous-tendus par les deux bords quittant le sommet. | & ! (D3DXTANGENT \_ POIDS \_ par \_ zone \| D3DXTANGENT \_ poids \_ égal)                |
| Calculez les coordonnées Cartésienles orthogonales à partir des coordonnées de texture (u, v). Consultez la section Notes.                   | & ! (D3DXTANGENT \_ ORTHOGONALiser \_ à partir de \_ U \| D3DXTANGENT \_ orthogonale \_ à partir de \_ V) |
| Les textures ne sont pas encapsulées dans les directions u ou v                                                     | & ! (D3DXTANGENT \_ ENVELOPPE \_ UV)                                                      |
| Les dérivés partiels en ce qui concerne les coordonnées de texture sont normalisés.                                  | & ! (D3DXTANGENT \_ ne pas \_ normaliser les \_ partiels)                                     |
| Les vertex sont triés dans le sens inverse des aiguilles d’une passe autour de chaque triangle.                               | & ! (D3DXTANGENT \_ PV de vent \_ )                                                      |
| Utilisez des vecteurs normaux par vertex déjà présents dans le maillage d’entrée.                                         | & ! (D3DXTANGENT \_ CALCULER les \_ normales)                                            |



 

Si \_ la génération \_ de D3DXTANGENT sur \_ place n’est pas définie, le maillage d’entrée est cloné. La maille d’origine doit donc disposer d’un espace suffisant pour stocker le vecteur normal calculé et les données dérivées partielles.

</dd> <dt>

*pdwAdjacency* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque face de la maille. Le nombre d’octets dans ce tableau doit être au moins égal à 3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).

</dd> <dt>

*fPartialEdgeThreshold* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Spécifie le cosinus maximal de l’angle à partir duquel deux dérivés partiels sont considérés comme incompatibles entre eux. Si le produit scalaire de la direction des deux dérivés partiels dans les triangles contigus est inférieur ou égal à ce seuil, les vertex partagés entre ces triangles seront fractionnés.

</dd> <dt>

*fSingularPointThreshold* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Spécifie l’amplitude maximale d’une dérivée partielle à laquelle un vertex sera considéré comme singulier. Comme plusieurs triangles sont des incidents sur un point qui ont des images tangentes proches, mais qui s’annulent complètement l’un de l’autre (par exemple, en haut d’une sphère), la grandeur de la dérivée partielle diminue. Si la magnitude est inférieure ou égale à ce seuil, le vertex est fractionné pour chaque triangle qui le contient.

</dd> <dt>

*fNormalEdgeThreshold* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Semblable à fPartialEdgeThreshold, spécifie le cosinus maximal de l’angle entre deux normales qui est un seuil au-delà duquel les vertex partagés entre triangles seront fractionnés. Si le produit scalaire des deux normales est inférieur au seuil, les vertex partagés sont fractionnés, formant ainsi un bord fixe entre les triangles voisins. Si le produit scalaire dépasse le seuil, les normales des triangles voisins seront interpolées.

</dd> <dt>

*ppMeshOut* \[ à\]
</dt> <dd>

Type : **[ **ID3DXMesh**](id3dxmesh.md)\*\***

Adresse d’un pointeur vers un objet de maillage [**ID3DXMesh**](id3dxmesh.md) de sortie qui reçoit les données de vecteur tangente, Binormal et normal calculées.

</dd> <dt>

*ppVertexMapping* \[ à\]
</dt> <dd>

Type : **[ **ID3DXBuffer**](id3dxbuffer.md)\*\***

Adresse d’un pointeur vers un objet de mémoire tampon [**ID3DXBuffer**](id3dxbuffer.md) de sortie qui reçoit un mappage de nouveaux vertex calculés par cette méthode aux vertex d’origine. La mémoire tampon est un tableau de DWORDs, dont la taille de tableau est définie en tant que nombre de vertex dans ppMeshOut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est S \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Une version simplifiée de cette fonction est disponible en tant que [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md).

Le vecteur normal calculé à chaque vertex est toujours normalisé pour avoir une longueur d’unité.

La solution la plus robuste pour calculer les coordonnées Cartésienles orthogonales consiste à ne pas définir d’indicateurs D3DXTANGENT \_ \_ de manière orthogonale à partir de \_ vous et D3DXTANGENT \_ à orthogonaliser \_ à partir de \_ v, afin que les coordonnées orthogonales soient calculées à partir des coordonnées de texture que vous et v. Toutefois, dans ce cas, si u ou v est égal à zéro, la fonction calcule les coordonnées orthogonales à l’aide \_ de D3DXTANGENT orthogonale \_ de \_ v ou de D3DXTANGENT \_ orthogonale \_ à partir de \_ u, respectivement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md)
</dt> </dl>

 

 
