---
description: D3DXMath est une bibliothèque d’assistance mathématique pour les applications Direct3D.
ms.assetid: 3067d47f-9b1d-2051-fa24-2094418ea272
title: Utilisation de D3DXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d463129a453a2b319dd72790bd4546dd90f63a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863481"
---
# <a name="working-with-d3dxmath"></a>Utilisation de D3DXMath

D3DXMath est une bibliothèque d’assistance mathématique pour les applications Direct3D. D3DXMath est à long terme, est inclus dans D3DX 9 et D3DX 10, et les dates renvoient également aux versions antérieures de DirectX.

> [!Note]  
> La bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8. nous vous recommandons donc vivement d’effectuer la migration vers DirectXMath au lieu d’utiliser D3DXMath.

 

DirectXMath partage une grande partie des mêmes fonctionnalités dans D3DXMath, et D3DXMath en interne comprend un certain nombre d’optimisations spécifiques au processeur. La principale différence réside dans le fait que D3DXMath est hébergé dans le D3DX9 \* . Dll et D3DX10 \* . Les dll et très peu de fonctions sont Inline. La Convention d’appel de la bibliothèque DirectXMath est explicitement SIMD, tandis que D3DXMath doit effectuer des conversions de charge et de stockage pour implémenter l’optimisation SIMD.

## <a name="mixing-directxmath-and-d3dxmath"></a>Combinaison de DirectXMath et de D3DXMath

D3DX11 ne contient pas D3DXMath et, en général, nous vous recommandons d’utiliser DirectXMath à la place. Toutefois, vous êtes libre de continuer à créer des liens vers D3DX9 et/ou D3DX10 dans votre application. par conséquent, vous pouvez continuer à utiliser D3DXMath ou utiliser D3DXMath et DirectXMath dans votre application en même temps.

Il est en général sécurisé d’effectuer un cast d’un XMVECTOR \* en une fonction qui prend D3DXVECTOR4 \* ou d’effectuer un cast d’un XMMATRIX \* en une fonction qui prend D3DXMATRIX \* . L’inverse n’est cependant pas sécurisé, car XMVECTOR et XMMATRIX doivent être alignés sur 16 octets, tandis que D3DXVECTOR4 et D3DXMATRIX n’ont pas cette exigence. Si vous ne respectez pas cette exigence, vous risquez d’obtenir des exceptions d’alignement non valides au moment de l’exécution.

Il est possible de convertir en toute sécurité un XMVECTOR \* en une fonction qui prend D3DXVECTOR2 \* ou D3DXVECTOR3 \* , mais pas l’inverse. Les deux problèmes d’alignement et le fait que D3DXVECTOR2 et D3DXVECTOR3 sont des structures plus petites rendent cela une opération risquée.

> [!Note]  
> D3DX (et par conséquent D3DXMath) est considéré comme hérité et n’est pas disponible pour les applications du Windows Store qui s’exécutent sur Windows 8 et qui n’est pas inclus dans le kit de développement logiciel (SDK) Windows 8 pour les applications de bureau.

 

## <a name="using-directxmath-with-direct3d"></a>Utilisation de DirectXMath avec Direct3D

DirectXMath et D3DXMath sont facultatifs lorsque vous travaillez avec Direct3D. Direct3D 9 a défini D3DMATRIX et D3DCOLOR dans le cadre de l’API Direct3D pour la prise en charge du pipeline de fonction fixe (désormais hérité). D3DXMath dans D3DX9 étend ces types Direct3D 9 avec les opérations mathématiques graphiques courantes. Pour Direct3D 10. x et Direct3D 11, l’API utilise uniquement le pipeline programmable, de sorte qu’il n’existe aucune structure spécifique à l’API pour les matrices ou les valeurs de couleur. Lorsque les API plus récentes requièrent une valeur de couleur, elles prennent un tableau explicite de valeurs float ou une mémoire tampon générique de données constantes interprétées par le nuanceur HLSL. Le langage HLSL lui-même peut prendre en charge des formats de matrices de lignes majeures ou de colonnes majeures, de sorte que la disposition dépend entièrement de vous (pour plus d’informations, consultez l’article sur le langage HLSL). Si vous utilisez des formats de matrices principaux dans vos nuanceurs, vous devez transposer les données de la matrice DirectXMath au [fur et à](../direct3dhlsl/dx-graphics-hlsl-per-component-math.md)mesure. Bien que facultative, les bibliothèques DirectXMath et D3DXMath fournissent des fonctionnalités graphiques communes et sont donc extrêmement pratiques lors de la programmation Direct3D.

Il est possible de convertir en toute sécurité un XMVECTOR \* en D3DVECTOR \* ou XMMATRIX \* en D3DMATRIX, \* car Direct3D 9 ne fait aucune supposition d’alignement sur la structure de données entrante. Il est également possible de convertir XMCOLOR en D3DCOLOR. Vous pouvez convertir une représentation 4-float de Color en XMCOLOR via XMStoreColor () pour obtenir la valeur DWORD 8:8:8:8 32 bits équivalente à D3DCOLOR.

Lorsque vous travaillez avec Direct3D 10. x ou Direct3D 11, vous utilisez généralement des types DirectXMath pour créer une structure pour chacune de vos mémoires tampons constantes, et dans ce cas, cela dépend en grande partie de votre capacité à contrôler l’alignement afin de rendre ces opérations efficaces ou d’utilisation de XMStore \* () pour convertir les données XMVECTOR et XMMATRIX en types de données corrects. Lors de l’appel d’API Direct3D 10. x ou Direct3D 11 qui requièrent un \[ \] tableau de valeurs de couleur à virgule flottante 4, vous pouvez effectuer un cast d’un XMVECTOR ou d’un \* XMFLOAT4 \* contenant les données de couleur.

## <a name="porting-from-d3dxmath"></a>Portage à partir de D3DXMath



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Type D3DXMath</th>
<th>DirectXMath équivalent</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3DXFLOAT16</td>
<td><a href="half-data-type.md"><strong>CARACTÈRES</strong></a></td>
</tr>
<tr class="even">
<td>D3DXMATRIX</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4x4"><strong>XMFLOAT4X4</strong></a></td>
</tr>
<tr class="odd">
<td>D3DXMATRIXA16</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix"><strong>XMMATRIX</strong></a> ou <a href="/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)"> <strong>XMFLOAT4X4A</strong></a></td>
</tr>
<tr class="even">
<td>D3DXQUATERNION<br/> D3DXPLANE<br/> D3DXCOLOR<br/></td>
<td><a href="xmvector-data-type.md"><strong>XMVECTOR</strong></a> est utilisé au lieu d’avoir des types uniques. vous devrez probablement utiliser un <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4"> <strong>XMFLOAT4</strong></a>
<blockquote>
[!Note]<br />
[<strong>D3DXQUATERNION :: Operator *</strong>] (.. /Direct3D9/d3dxquaternion-extensions.MD) appelle la fonction <a href="/windows/desktop/direct3d9/d3dxquaternionmultiply"><strong>D3DXQuaternionMultiply</strong></a> , qui multiplie deux quaternions. Toutefois, à moins que vous n’utilisiez explicitement la fonction <a href="/windows/desktop/api/directxmath/nf-directxmath-xmquaternionmultiply"><strong>XMQuaternionMultiply</strong></a> , vous recevez une réponse incorrecte quand vous utilisez <a href="xmvector-operator-mul.md"><strong>XMVECTOR :: Operator *</strong></a> sur un Quaternion.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>D3DXVECTOR2</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat2"><strong>XMFLOAT2</strong></a></td>
</tr>
<tr class="even">
<td>D3DXVECTOR2_16F</td>
<td><a href="/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2"><strong>XMHALF2</strong></a></td>
</tr>
<tr class="odd">
<td>D3DXVECTOR3</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat3"><strong>XMFLOAT3</strong></a></td>
</tr>
<tr class="even">
<td>D3DXVECTOR4</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4"><strong>XMFLOAT4</strong></a>(ou si vous pouvez garantir que les données sont alignées sur 16 octets, <a href="xmvector-data-type.md"><strong>XMVECTOR</strong></a> ou <a href="/previous-versions/windows/desktop/legacy/ee419609(v=vs.85)"><strong>XMFLOAT4A</strong></a> )<br/></td>
</tr>
<tr class="odd">
<td>D3DXVECTOR4_16F</td>
<td><a href="/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4"><strong>XMHALF4</strong></a></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Il n’existe aucun équivalent direct à D3DXVECTOR3 \_ 16F dans XNAMath.

 



| D3DXMath macro) | DirectXMath équivalent                            |
|----------------|---------------------------------------------------|
| D3DX \_ pi       | [XM \_ pi](ovw-xnamath-reference-constants.md)     |
| D3DX \_ 1BYPI    | [XM \_ 1DIVPI](ovw-xnamath-reference-constants.md) |
| D3DXToRadian   | [**XMConvertToRadians**](/windows/desktop/api/DirectXMath/nf-directxmath-xmconverttoradians)  |
| D3DXToDegree   | [**XMConvertToDegrees**](/windows/desktop/api/DirectXMath/nf-directxmath-xmconverttodegrees)  |



 



| D3DXMath fonction)                  | DirectXMath équivalent                                                                                                                                                                                                                           |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXBoxBoundProbe                  | [**BoundingBox :: intersections (XMVECTOR, XMVECTOR, float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_float_))                                                                                                                                                          |
| D3DXComputeBoundingBox             | [**BoundingBox :: CreateFromPoints**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-createfrompoints)                                                                                                                                                                          |
| D3DXComputeBoundingSphere          | [**BoundingSphere::CreateFromPoints**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-createfrompoints)                                                                                                                                                                      |
| D3DXSphereBoundProbe               | [**BoundingSphere :: croisements (XMVECTOR, XMVECTOR, float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-intersects(fxmvector_fxmvector_float_))                                                                                                                                                    |
| D3DXIntersectTriFunction           | [**TriangleTests :: croisements**](ovw-xnamath-triangletests.md)                                                                                                                                                                                   |
| D3DXFloat32To16Array               | [**XMConvertFloatToHalfStream**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmconvertfloattohalfstream)                                                                                                                                                                                 |
| D3DXFloat16To32Array               | [**XMConvertHalfToFloatStream**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmconverthalftofloatstream)                                                                                                                                                                                 |
| D3DXVec2Length                     | [**XMVector2Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector2length) ou [ **XMVector2LengthEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector2lengthest)                                                                                                                                                   |
| D3DXVec2LengthSq                   | [**XMVector2LengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmvector2lengthsq)                                                                                                                                                                                                   |
| D3DXVec2Dot                        | [**XMVector2Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector2dot)                                                                                                                                                                                                             |
| D3DXVec2CCW                        | [**XMVector2Cross**](/windows/win32/api/directxmath/nf-directxmath-xmvector2cross)                                                                                                                                                                                                         |
| D3DXVec2Add                        | [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXVec2Subtract                   | [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXVec2Minimize                   | [**XMVectorMin**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)                                                                                                                                                                                                               |
| D3DXVec2Maximize                   | [**XMVectorMax**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)                                                                                                                                                                                                               |
| D3DXVec2Scale                      | [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXVec2Lerp                       | [**XMVectorLerp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp) ou [ **XMVectorLerpV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXVec2Normalize                  | [**XMVector2Normalize**](/windows/win32/api/directxmath/nf-directxmath-xmvector2normalize) ou [ **XMVector2NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector2normalizeest)                                                                                                                                       |
| D3DXVec2Hermite                    | [**XMVectorHermite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermite) ou [ **XMVectorHermiteV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermitev)                                                                                                                                                       |
| D3DXVec2CatmullRom                 | [**XMVectorCatmullRom**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullrom) ou [ **XMVectorCatmullRomV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullromv)                                                                                                                                           |
| D3DXVec2BaryCentric                | [**XMVectorBaryCentric**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentric) ou [ **XMVectorBaryCentricV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentricv)                                                                                                                                       |
| D3DXVec2Transform                  | [**XMVector2Transform**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transform)                                                                                                                                                                                                 |
| D3DXVec2TransformCoord             | [**XMVector2TransformCoord**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformcoord)                                                                                                                                                                                       |
| D3DXVec2TransformNormal            | [**XMVector2TransformNormal**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformnormal)                                                                                                                                                                                     |
| D3DXVec2TransformArray             | [**XMVector2TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                                                                                                                                                     |
| D3DXVec2TransformCoordArray        | [**XMVector2TransformCoordStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformcoordstream)                                                                                                                                                                           |
| D3DXVec2TransformNormalArray       | [**XMVector2TransformNormalStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformnormalstream)                                                                                                                                                                         |
| D3DXVec3Length                     | [**XMVector3Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector3length) ou [ **XMVector3LengthEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3lengthest)                                                                                                                                                   |
| D3DXVec3LengthSq                   | [**XMVector3LengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmvector3lengthsq)                                                                                                                                                                                                   |
| D3DXVec3Dot                        | [**XMVector3Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector3dot)                                                                                                                                                                                                             |
| D3DXVec3Cross                      | [**XMVector3Cross**](/windows/win32/api/directxmath/nf-directxmath-xmvector3cross)                                                                                                                                                                                                         |
| D3DXVec3Add                        | [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXVec3Subtract                   | [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXVec3Minimize                   | [**XMVectorMin**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)                                                                                                                                                                                                               |
| D3DXVec3Maximize                   | [**XMVectorMax**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)                                                                                                                                                                                                               |
| D3DXVec3Scale                      | [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXVec3Lerp                       | [**XMVectorLerp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp) ou [ **XMVectorLerpV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXVec3Normalize                  | [**XMVector3Normalize**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalize) ou [ **XMVector3NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalizeest)                                                                                                                                       |
| D3DXVec3Hermite                    | [**XMVectorHermite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermite) ou [ **XMVectorHermiteV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermitev)                                                                                                                                                       |
| D3DXVec3CatmullRom                 | [**XMVectorCatmullRom**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullrom) ou [ **XMVectorCatmullRomV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullromv)                                                                                                                                           |
| D3DXVec3BaryCentric                | [**XMVectorBaryCentric**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentric) ou [ **XMVectorBaryCentricV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentricv)                                                                                                                                       |
| D3DXVec3Transform                  | [**XMVector3Transform**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transform)                                                                                                                                                                                                 |
| D3DXVec3TransformCoord             | [**XMVector3TransformCoord**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoord)                                                                                                                                                                                       |
| D3DXVec3TransformNormal            | [**XMVector3TransformNormal**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormal)                                                                                                                                                                                     |
| D3DXVec3TransformArray             | [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                                                                                                                                                     |
| D3DXVec3TransformCoordArray        | [**XMVector3TransformCoordStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoordstream)                                                                                                                                                                           |
| D3DXVec3TransformNormalArray       | [**XMVector3TransformNormalStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormalstream)                                                                                                                                                                         |
| D3DXVec3Project                    | [**XMVector3Project**](/windows/win32/api/directxmath/nf-directxmath-xmvector3project)                                                                                                                                                                                                     |
| D3DXVec3Unproject                  | [**XMVector3Unproject**](/windows/win32/api/directxmath/nf-directxmath-xmvector3unproject)                                                                                                                                                                                                 |
| D3DXVec3ProjectArray               | [**XMVector3ProjectStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3projectstream)                                                                                                                                                                                         |
| D3DXVec3UnprojectArray             | [**XMVector3UnprojectStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3unprojectstream)                                                                                                                                                                                     |
| D3DXVec4Length                     | [**XMVector4Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector4length) ou [ **XMVector4LengthEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector4lengthest)                                                                                                                                                   |
| D3DXVec4LengthSq                   | [**XMVector4LengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmvector4lengthsq)                                                                                                                                                                                                   |
| D3DXVec4Dot                        | [**XMVector4Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector4dot)                                                                                                                                                                                                             |
| D3DXVec4Add                        | [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXVec4Subtract                   | [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXVec4Minimize                   | [**XMVectorMin**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)                                                                                                                                                                                                               |
| D3DXVec4Maximize                   | [**XMVectorMax**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)                                                                                                                                                                                                               |
| D3DXVec4Scale                      | [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXVec4Lerp                       | [**XMVectorLerp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp) ou [ **XMVectorLerpV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXVec4Cross                      | [**XMVector4Cross**](/windows/win32/api/directxmath/nf-directxmath-xmvector4cross)                                                                                                                                                                                                         |
| D3DXVec4Normalize                  | [**XMVector4Normalize**](/windows/win32/api/directxmath/nf-directxmath-xmvector4normalize) ou [ **XMVector4NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector4normalizeest)                                                                                                                                       |
| D3DXVec4Hermite                    | [**XMVectorHermite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermite) ou [ **XMVectorHermiteV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermitev)                                                                                                                                                       |
| D3DXVec4CatmullRom                 | [**XMVectorCatmullRom**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullrom) ou [ **XMVectorCatmullRomV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullromv)                                                                                                                                           |
| D3DXVec4BaryCentric                | [**XMVectorBaryCentric**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentric) ou [ **XMVectorBaryCentricV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentricv)                                                                                                                                       |
| D3DXVec4Transform                  | [**XMVector4Transform**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transform)                                                                                                                                                                                                 |
| D3DXVec4TransformArray             | [**XMVector4TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transformstream)                                                                                                                                                                                     |
| D3DXMatrixIdentity                 | [**XMMatrixIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixidentity)                                                                                                                                                                                                     |
| D3DXMatrixDeterminant              | [**XMMatrixDeterminant**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdeterminant)                                                                                                                                                                                               |
| D3DXMatrixDecompose                | [**XMMatrixDecompose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdecompose)                                                                                                                                                                                                   |
| D3DXMatrixTranspose                | [**XMMatrixTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranspose)                                                                                                                                                                                                   |
| D3DXMatrixMultiply                 | [**XMMatrixMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiply)                                                                                                                                                                                                     |
| D3DXMatrixMultiplyTranspose        | [**XMMatrixMultiplyTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiplytranspose)                                                                                                                                                                                   |
| D3DXMatrixInverse                  | [**XMMatrixInverse**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixinverse)                                                                                                                                                                                                       |
| D3DXMatrixScaling                  | [**XMMatrixScaling**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscaling)                                                                                                                                                                                                       |
| D3DXMatrixTranslation              | [**XMMatrixTranslation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslation)                                                                                                                                                                                               |
| D3DXMatrixRotationX                | [**XMMatrixRotationX**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationx)                                                                                                                                                                                                   |
| D3DXMatrixRotationY                | [**XMMatrixRotationY**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationy)                                                                                                                                                                                                   |
| D3DXMatrixRotationZ                | [**XMMatrixRotationZ**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationz)                                                                                                                                                                                                   |
| D3DXMatrixRotationAxis             | [**XMMatrixRotationAxis**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationaxis)                                                                                                                                                                                             |
| D3DXMatrixRotationQuaternion       | [**XMMatrixRotationQuaternion**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationquaternion)                                                                                                                                                                                 |
| D3DXMatrixRotationYawPitchRoll     | [**XMMatrixRotationRollPitchYaw**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyaw) (Notez que l’ordre des paramètres est différent : D3DXMatrixRotationYawPitchRoll prend le lacet, le tangage, le rouleau, le **XMMatrixRotationRollPitchYaw** prend le pas, le lacet, le rouleau)                 |
| D3DXMatrixTransformation           | [**XMMatrixTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation)                                                                                                                                                                                         |
| D3DXMatrixTransformation2D         | [**XMMatrixTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation2d)                                                                                                                                                                                     |
| D3DXMatrixAffineTransformation     | [**XMMatrixAffineTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation)                                                                                                                                                                             |
| D3DXMatrixAffineTransformation2D   | [**XMMatrixAffineTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation2d)                                                                                                                                                                         |
| D3DXMatrixLookAtRH                 | [**XMMatrixLookAtRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatrh)                                                                                                                                                                                                     |
| D3DXMatrixLookAtLH                 | [**XMMatrixLookAtLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatlh)                                                                                                                                                                                                     |
| D3DXMatrixPerspectiveRH            | [**XMMatrixPerspectiveRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiverh)                                                                                                                                                                                           |
| D3DXMatrixPerspectiveLH            | [**XMMatrixPerspectiveLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivelh)                                                                                                                                                                                           |
| D3DXMatrixPerspectiveFovRH         | [**XMMatrixPerspectiveFovRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovrh)                                                                                                                                                                                     |
| D3DXMatrixPerspectiveFovLH         | [**XMMatrixPerspectiveFovLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovlh)                                                                                                                                                                                     |
| D3DXMatrixPerspectiveOffCenterRH   | [**XMMatrixPerspectiveOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterrh)                                                                                                                                                                         |
| D3DXMatrixPerspectiveOffCenterLH   | [**XMMatrixPerspectiveOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterlh)                                                                                                                                                                         |
| D3DXMatrixOrthoRH                  | [**XMMatrixOrthographicRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicrh)                                                                                                                                                                                         |
| D3DXMatrixOrthoLH                  | [**XMMatrixOrthographicLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographiclh)                                                                                                                                                                                         |
| D3DXMatrixOrthoOffCenterRH         | [**XMMatrixOrthographicOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterrh)                                                                                                                                                                       |
| D3DXMatrixOrthoOffCenterLH         | [**XMMatrixOrthographicOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterlh)                                                                                                                                                                       |
| D3DXMatrixShadow                   | [**XMMatrixShadow**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixshadow)                                                                                                                                                                                                         |
| D3DXMatrixReflect                  | [**XMMatrixReflect**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixreflect)                                                                                                                                                                                                       |
| D3DXQuaternionLength               | [**XMQuaternionLength**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionlength)                                                                                                                                                                                                 |
| D3DXQuaternionLengthSq             | [**XMQuaternionLengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionlengthsq)                                                                                                                                                                                             |
| D3DXQuaternionDot                  | [**XMQuaternionDot**](/windows/win32/api/directxmath/nf-directxmath-xmquaterniondot)                                                                                                                                                                                                       |
| D3DXQuaternionIdentity             | [**XMQuaternionIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionidentity)                                                                                                                                                                                             |
| D3DXQuaternionIsIdentity           | [**XMQuaternionIsIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionisidentity)                                                                                                                                                                                         |
| D3DXQuaternionConjugate            | [**XMQuaternionConjugate**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionconjugate)                                                                                                                                                                                           |
| D3DXQuaternionToAxisAngle          | [**XMQuaternionToAxisAngle**](/windows/win32/api/directxmath/nf-directxmath-xmquaterniontoaxisangle)                                                                                                                                                                                       |
| D3DXQuaternionRotationMatrix       | [**XMQuaternionRotationMatrix**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationmatrix)                                                                                                                                                                                 |
| D3DXQuaternionRotationAxis         | [**XMQuaternionRotationAxis**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationaxis)                                                                                                                                                                                     |
| D3DXQuaternionRotationYawPitchRoll | [**XMQuaternionRotationRollPitchYaw**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationrollpitchyaw) (Notez que l’ordre des paramètres est différent : D3DXQuaternionRotationYawPitchRoll prend le lacet, le tangage, le rouleau, le **XMQuaternionRotationRollPitchYaw** prend le pas, le lacet, le rouleau) |
| D3DXQuaternionMultiply             | [**XMQuaternionMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionmultiply)                                                                                                                                                                                             |
| D3DXQuaternionNormalize            | [**XMQuaternionNormalize**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionnormalize) ou [ **XMQuaternionNormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionnormalizeest)                                                                                                                           |
| D3DXQuaternionInverse              | [**XMQuaternionInverse**](/windows/win32/api/directxmath/nf-directxmath-xmquaternioninverse)                                                                                                                                                                                               |
| D3DXQuaternionLn                   | [**XMQuaternionLn**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionln)                                                                                                                                                                                                         |
| D3DXQuaternionExp                  | [**XMQuaternionExp**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionexp)                                                                                                                                                                                                       |
| D3DXQuaternionSlerp                | [**XMQuaternionSlerp**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionslerp) ou [ **XMQuaternionSlerpV**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionslerpv)                                                                                                                                               |
| D3DXQuaternionSquad                | [**XMQuaternionSquad**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquad) ou [ **XMQuaternionSquadV**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquadv)                                                                                                                                               |
| D3DXQuaternionSquadSetup           | [**XMQuaternionSquadSetup**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquadsetup)                                                                                                                                                                                         |
| D3DXQuaternionBaryCentric          | [**XMQuaternionBaryCentric**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionbarycentric) ou [ **XMQuaternionBaryCentricV**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionbarycentricv)                                                                                                                       |
| D3DXPlaneDot                       | [**XMPlaneDot**](/windows/win32/api/directxmath/nf-directxmath-xmplanedot)                                                                                                                                                                                                                 |
| D3DXPlaneDotCoord                  | [**XMPlaneDotCoord**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotcoord)                                                                                                                                                                                                       |
| D3DXPlaneDotNormal                 | [**XMPlaneDotNormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotnormal)                                                                                                                                                                                                     |
| D3DXPlaneScale                     | [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXPlaneNormalize                 | [**XMPlaneNormalize**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalize) ou [ **XMPlaneNormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalizeest)                                                                                                                                               |
| D3DXPlaneIntersectLine             | [**XMPlaneIntersectLine**](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectline)                                                                                                                                                                                             |
| D3DXPlaneFromPointNormal           | [**XMPlaneFromPointNormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompointnormal)                                                                                                                                                                                         |
| D3DXPlaneFromPoints                | [**XMPlaneFromPoints**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompoints)                                                                                                                                                                                                   |
| D3DXPlaneTransform                 | [**XMPlaneTransform**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransform)                                                                                                                                                                                                     |
| D3DXPlaneTransformArray            | [**XMPlaneTransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransformstream)                                                                                                                                                                                         |
| D3DXColorNegative                  | [**XMColorNegative**](/windows/win32/api/directxmath/nf-directxmath-xmcolornegative)                                                                                                                                                                                                       |
| D3DXColorAdd                       | [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXColorSubtract                  | [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXColorScale                     | [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXColorModulate                  | [**XMColorModulate**](/windows/win32/api/directxmath/nf-directxmath-xmcolormodulate)                                                                                                                                                                                                       |
| D3DXColorLerp                      | [**XMVectorLerp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp) ou [ **XMVectorLerpV**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXColorAdjustSaturation          | [**XMColorAdjustSaturation**](/windows/win32/api/directxmath/nf-directxmath-xmcoloradjustsaturation)                                                                                                                                                                                       |
| D3DXColorAdjustContrast            | [**XMColorAdjustContrast**](/windows/win32/api/directxmath/nf-directxmath-xmcoloradjustcontrast)                                                                                                                                                                                           |
| D3DXFresnelTerm                    | [**XMFresnelTerm**](/windows/win32/api/directxmath/nf-directxmath-xmfresnelterm)                                                                                                                                                                                                           |



 

> [!Note]  
> Les fonctions d' [harmoniques sphériques](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) pour DirectXMath sont disponibles séparément. Il n’y a aucun DirectXMath équivalent à **ID3DXMatrixStack**.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
