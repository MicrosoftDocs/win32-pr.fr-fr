---
description: Cette rubrique décrit la conception interne de la bibliothèque DirectXMath.
ms.assetid: 31512657-c413-9e6e-e343-1ea677a02b8c
title: Éléments internes de bibliothèque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3100a8e83a6935071722d5d1733400fa8824c62a
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128521226"
---
# <a name="library-internals"></a>Éléments internes de bibliothèque

Cette rubrique décrit la conception interne de la bibliothèque DirectXMath.

-   [Conventions d’appel](#calling-conventions)
-   [Équivalence de type de bibliothèque Graphics](#graphics-library-type-equivalence)
-   [Constantes globales dans la bibliothèque DirectXMath](#global-constants-in-the-directxmath-library)
-   [Windows SSE et SSE2](#windows-sse-versus-sse2)
-   [Variantes de routine](#routine-variants)
-   [Incohérences de la plateforme](#platform-inconsistencies)
-   [Extensions spécifiques à la plateforme](#platform-specific-extensions)
-   [Rubriques connexes](#related-topics)

## <a name="calling-conventions"></a>Conventions d’appel

Pour améliorer la portabilité et optimiser la disposition des données, vous devez utiliser les conventions d’appel appropriées pour chaque plateforme prise en charge par la bibliothèque DirectXMath. Plus précisément, lorsque vous transmettez des objets [**XMVECTOR**](xmvector-data-type.md) en tant que paramètres, qui sont définis comme alignés sur une limite de 16 octets, il existe différents jeux d’exigences appelant, en fonction de la plateforme cible :

**Pour le Windows 32 bits**

pour les Windowss 32 bits, deux conventions d’appel sont disponibles pour une transmission efficace des valeurs [ \_ \_ m128](/cpp/cpp/m128) (qui implémente [**XMVECTOR**](xmvector-data-type.md) sur cette plateforme). La norme est [ \_ \_ fastcall](/cpp/cpp/fastcall), qui peut passer les trois premières valeurs [ \_ \_ M128](/cpp/cpp/m128) (instances **XMVECTOR** ) comme arguments à une fonction dans un registre *SSE/SSE2* . [ \_ \_ fastcall](/cpp/cpp/fastcall) passe les arguments restants via la pile.

les nouveaux compilateurs de Microsoft Visual Studio prennent en charge une nouvelle convention d’appel, \_ \_ vectorcall, qui peut passer jusqu’à six valeurs [ \_ \_ m128](/cpp/cpp/m128) (instances [**XMVECTOR**](xmvector-data-type.md) ) comme arguments d’une fonction dans un registre *SSE/SSE2* . Il peut également passer des agrégats vectoriels hétérogènes (également appelés [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)) via des registres *SSE/SSE2* s’il y a suffisamment d’espace.

**Pour les éditions 64 bits de Windows**

pour les Windowss 64 bits, deux conventions d’appel sont disponibles pour une transmission efficace des valeurs de [ \_ \_ m128](/cpp/cpp/m128) . La norme est [ \_ \_ fastcall](/cpp/cpp/fastcall), qui passe toutes les valeurs [ \_ \_ M128](/cpp/cpp/m128) sur la pile.

les nouveaux compilateurs de Visual Studio prennent en charge la \_ \_ convention d’appel vectorcall, qui peut passer jusqu’à six valeurs [ \_ \_ m128](/cpp/cpp/m128) (instances [**XMVECTOR**](xmvector-data-type.md) ) comme arguments à une fonction dans un registre *SSE/SSE2* . Il peut également passer des agrégats vectoriels hétérogènes (également appelés [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)) via des registres *SSE/SSE2* s’il y a suffisamment d’espace.

**pour Windows sur ARM**

le Windows sur ARM & ARM64 prend en charge le passage des quatre premières \_ \_ valeurs n128 (instances [**XMVECTOR**](xmvector-data-type.md) ) dans le registre.

**Solution DirectXMath**

Les alias **FXMVECTOR**, **GXMVECTOR**, **HXMVECTOR** et **CXMVECTOR** prennent en charge les conventions suivantes :

-   Utilisez l’alias **FXMVECTOR** pour transmettre les trois premières instances de [**XMVECTOR**](xmvector-data-type.md) utilisées comme arguments à une fonction.
-   Utilisez l’alias **GXMVECTOR** pour transmettre la quatrième instance d’un [**XMVECTOR**](xmvector-data-type.md) utilisé comme argument à une fonction.
-   Utilisez l’alias **HXMVECTOR** pour passer les 5e et 6ème instances d’un [**XMVECTOR**](xmvector-data-type.md) utilisé comme argument d’une fonction. Pour plus d’informations sur les considérations supplémentaires, consultez la \_ \_ documentation vectorcall.
-   Utilisez l’alias **CXMVECTOR** pour passer toutes les autres instances de [**XMVECTOR**](xmvector-data-type.md) utilisées comme arguments.

> [!Note]  
> Pour les paramètres de sortie, utilisez toujours XMVECTOR \* ou XMVECTOR& et ignorez-les en ce qui concerne les règles précédentes pour les paramètres d’entrée.

 

En raison des limitations de \_ \_ vectorcall, nous vous recommandons de ne pas utiliser **GXMVECTOR** ou **HXMVECTOR** pour les constructeurs C++. Utilisez simplement **FXMVECTOR** pour les trois premières valeurs [**XMVECTOR**](xmvector-data-type.md) , puis utilisez **CXMVECTOR** pour le reste.

Les alias **FXMMATRIX** et **CXMMATRIX** aident à tirer parti de l’argument HVA passant avec \_ \_ vectorcall.

-   Utilisez l’alias **FXMMATRIX** pour passer le premier [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) en tant qu’argument à la fonction. Cela suppose que vous n’avez pas plus de deux arguments **FXMVECTOR** ou plus de deux arguments float, double ou **FXMVECTOR** pour le « Right » de la matrice. Pour plus d’informations sur les considérations supplémentaires, consultez la \_ \_ documentation vectorcall.
-   Utilisez l’alias **CXMMATRIX** dans le cas contraire.

En raison des limitations de \_ \_ vectorcall, nous vous recommandons de ne jamais utiliser **FXMMATRIX** pour les constructeurs C++. Utilisez simplement **CXMMATRIX**.

Outre les alias de type, vous devez également utiliser l' \_ annotation XM CALLCONV pour vous assurer que la fonction utilise la Convention d’appel appropriée ( \_ \_ fastcall et \_ \_ vectorcall) en fonction de votre compilateur et de votre architecture. En raison des limitations de \_ \_ vectorcall, nous vous recommandons de ne pas utiliser XM \_ CALLCONV pour les constructeurs C++.

Voici des exemples de déclarations qui illustrent cette Convention :


```C++
XMMATRIX XM_CALLCONV XMMatrixLookAtLH(FXMVECTOR EyePosition, FXMVECTOR FocusPosition, FXMVECTOR UpDirection);

XMMATRIX XM_CALLCONV XMMatrixTransformation2D(FXMVECTOR ScalingOrigin,  float ScalingOrientation, FXMVECTOR Scaling, FXMVECTOR RotationOrigin, float Rotation, GXMVECTOR Translation);

void XM_CALLCONV XMVectorSinCos(XMVECTOR* pSin, XMVECTOR* pCos, FXMVECTOR V);

XMVECTOR XM_CALLCONV XMVectorHermiteV(FXMVECTOR Position0, FXMVECTOR Tangent0, FXMVECTOR Position1, GXMVECTOR Tangent1, HXMVECTOR T);

XMMATRIX(FXMVECTOR R0, FXMVECTOR R1, FXMVECTOR R2, CXMVECTOR R3)

XMVECTOR XM_CALLCONV XMVector2Transform(FXMVECTOR V, FXMMATRIX M);

XMMATRIX XM_CALLCONV XMMatrixMultiplyTranspose(FXMMATRIX M1, CXMMATRIX M2);
```



Pour prendre en charge ces conventions d’appel, ces alias de type sont définis comme suit (les paramètres doivent être passés par valeur pour que le compilateur les prenne en compte pour la réussite de l’inscription) :

**pour les applications Windows bits 32**

Quand vous utilisez \_ \_ fastcall :


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR& GXMVECTOR;
typedef const XMVECTOR& HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



Quand vous utilisez \_ \_ vectorcall :


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR  HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX  FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



**pour les applications Windows natives 64 bits**

Quand vous utilisez \_ \_ fastcall :


```C++
typedef const XMVECTOR& FXMVECTOR;
typedef const XMVECTOR& GXMVECTOR;
typedef const XMVECTOR& HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



Quand vous utilisez \_ \_ vectorcall :


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR  HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX  FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



**Windows sur ARM**


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



> [!Note]  
> Alors que toutes les fonctions sont déclarées inline et, dans de nombreux cas, le compilateur n’a pas besoin d’utiliser des conventions d’appel pour ces fonctions. dans certains cas, le compilateur peut décider qu’il est plus efficace de ne pas incorporer la fonction. dans ce cas, nous souhaitons que la meilleure Convention d’appel soit possible pour chaque plateforme.

 

## <a name="graphics-library-type-equivalence"></a>Équivalence de type de bibliothèque Graphics

pour prendre en charge l’utilisation de la bibliothèque DirectXMath, de nombreux types et structures de bibliothèque DirectXMath sont équivalents aux implémentations Windows des types **D3DDECLTYPE** et **D3DFORMAT** , ainsi qu’aux types de [**\_ FORMAT DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) .

| DirectXMath                      | D3DDECLTYPE                                                                           | D3DFORMAT                                                     | \_format dxgi                                                                                                                                                                                            |
|----------------------------------|---------------------------------------------------------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XMBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2)       |                                                                                       |                                                               | \_Format dxgi \_ R8G8 \_ Saint-                                                                                                                                                                                |
| [**XMBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4)       | D3DDECLTYPE \_ BYTE4 (Xbox uniquement)                                                        | D3DFMT \_ x8x8x8x8                                              | \_Format dxgi \_ x8x8x8x8 \_ Saint-                                                                                                                                                                            |
| [**XMBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2)     |                                                                                       | D3DFMT \_ V8U8                                                  | \_Format dxgi \_ R8G8 \_ ronfler                                                                                                                                                                               |
| [**XMBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4)     | D3DDECLTYPE \_ BYTE4N (Xbox uniquement)                                                       | D3DFMT \_ x8x8x8x8                                              | \_Format dxgi \_ x8x8x8x8 \_ ronfler                                                                                                                                                                           |
| [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor)       | D3DDECLTYPE \_ D3DCOLOR                                                                 | D3DFMT \_ A8R8G8B8                                              | DXGI \_ format \_ B8G8R8A8 \_ UNORM (DXGI 1.1 +)                                                                                                                                                               |
| [**XMDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4)         | D3DDECLTYPE \_ DEC4 (Xbox uniquement)                                                         | D3DDECLTYPE \_ DEC3 (Xbox uniquement)                                 |                                                                                                                                                                                                         |
| [**XMDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4)       | D3DDECLTYPE \_ DEC4N (Xbox uniquement)                                                        | D3DDECLTYPE \_ DEC3N (Xbox uniquement)                                |                                                                                                                                                                                                         |
| [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2)     | D3DDECLTYPE \_ FLOAT2                                                                   | D3DFMT \_ G32R32F                                               | DXGI \_ format \_ R32G32 \_ float                                                                                                                                                                             |
| [**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85))   | D3DDECLTYPE \_ FLOAT2                                                                   | D3DFMT \_ G32R32F                                               | DXGI \_ format \_ R32G32 \_ float                                                                                                                                                                             |
| [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3)     | D3DDECLTYPE \_ FLOAT3                                                                   |                                                               | DXGI \_ format \_ R32G32B32 \_ float                                                                                                                                                                          |
| [**XMFLOAT3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a)   | D3DDECLTYPE \_ FLOAT3                                                                   |                                                               | DXGI \_ format \_ R32G32B32 \_ float                                                                                                                                                                          |
| [**XMFLOAT3PK**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) |                                                                                       |                                                               | DXGI \_ format \_ R11G11B10 \_ float                                                                                                                                                                          |
| [**XMFLOAT3SE**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) |                                                                                       |                                                               | DXGI \_ format \_ R9G9B9E5 \_ SHAREDEXP                                                                                                                                                                       |
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4)     | D3DDECLTYPE \_ float4                                                                   | D3DFMT \_ A32B32G32R32F                                         | DXGI \_ format \_ R32G32B32A32 \_ float                                                                                                                                                                       |
| [**XMFLOAT4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a)   | D3DDECLTYPE \_ float4                                                                   | D3DFMT \_ A32B32G32R32F                                         | DXGI \_ format \_ R32G32B32A32 \_ float                                                                                                                                                                       |
| [**XMHALF2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2)       | D3DDECLTYPE \_ FLOAT16 \_ 2                                                               | D3DFMT \_ G16R16F                                               | DXGI \_ format \_ R16G16 \_ float                                                                                                                                                                             |
| [**XMHALF4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4)       | D3DDECLTYPE \_ FLOAT16 \_ 4                                                               | D3DFMT \_ A16B16G16R16F                                         | DXGI \_ format \_ R16G16B16A16 \_ float                                                                                                                                                                       |
| [**XMINT2**](/windows/win32/api/directxmath/ns-directxmath-xmint2)         |                                                                                       |                                                               | \_Format dxgi \_ R32G32 \_ Saint-                                                                                                                                                                              |
| [**XMINT3**](/windows/win32/api/directxmath/ns-directxmath-xmint3)         |                                                                                       |                                                               | \_Format dxgi \_ R32G32B32 \_ Saint-                                                                                                                                                                           |
| [**XMINT4**](/windows/win32/api/directxmath/ns-directxmath-xmint4)         |                                                                                       |                                                               | \_Format dxgi \_ R32G32B32A32 \_ Saint-                                                                                                                                                                        |
| [**XMSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2)     | D3DDECLTYPE \_ SHORT2                                                                   | D3DFMT \_ V16U16                                                | \_Format dxgi \_ R16G16 \_ Saint-                                                                                                                                                                              |
| [**XMSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2)   | D3DDECLTYPE \_ SHORT2N                                                                  | D3DFMT \_ V16U16                                                | \_Format dxgi \_ R16G16 \_ ronfler                                                                                                                                                                             |
| [**XMSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4)     | D3DDECLTYPE \_ SHORT4                                                                   | D3DFMT \_ x16x16x16x16                                          | \_Format dxgi \_ R16G16B16A16 \_ Saint-                                                                                                                                                                        |
| [**XMSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4)   | D3DDECLTYPE \_ SHORT4N                                                                  | D3DFMT \_ x16x16x16x16                                          | \_Format dxgi \_ R16G16B16A16 \_ ronfler                                                                                                                                                                       |
| [**XMUBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2)     |                                                                                       |                                                               | DXGI \_ format \_ R8G8 \_ uint                                                                                                                                                                                |
| [**XMUBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2)   |                                                                                       | D3DFMT \_ A8P8, D3DFMT \_ A8L8                                    | DXGI \_ format \_ R8G8 \_ UNORM                                                                                                                                                                               |
| [**XMUINT2**](/windows/win32/api/directxmath/ns-directxmath-xmuint2)       |                                                                                       |                                                               | DXGI \_ format \_ R32G32 \_ uint                                                                                                                                                                              |
| [**XMUINT3**](/windows/win32/api/directxmath/ns-directxmath-xmuint3)       |                                                                                       |                                                               | DXGI \_ format \_ R32G32B32 \_ uint                                                                                                                                                                           |
| [**XMUINT4**](/windows/win32/api/directxmath/ns-directxmath-xmuint4)       |                                                                                       |                                                               | DXGI \_ format \_ R32G32B32A32 \_ uint                                                                                                                                                                        |
| [**XMU555**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555)         |                                                                                       | D3DFMT \_ X1R5G5B5, D3DFMT \_ A1R5G5B5                            | DXGI \_ format \_ B5G5R5A1 \_ UNORM                                                                                                                                                                           |
| [**XMU565**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565)         |                                                                                       | D3DFMT \_ R5G6B5                                                | DXGI \_ format \_ B5G6R5 \_ UNORM                                                                                                                                                                             |
| [**XMUBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4)     | D3DDECLTYPE \_ UBYTE4                                                                   | D3DFMT \_ x8x8x8x8                                              | DXGI \_ format \_ x8x8x8x8 \_ uint                                                                                                                                                                            |
| [**XMUBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4)   | D3DDECLTYPE \_ UBYTE4N                                                                  | D3DFMT \_ x8x8x8x8                                              | DXGI \_ format \_ x8x8x8x8 \_ UNORM<br/> DXGI \_ format \_ R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM (utilisez [**XMLoadUDecN4 \_**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmloadudecn4_xr) XR et [**XMStoreUDecN4 \_**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmstoreudecn4_xr)XR.)<br/> |
| [**XMUDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4)       | D3DDECLTYPE \_ UDEC4 (Xbox uniquement)<br/> D3DDECLTYPE \_ UDEC3 (Xbox uniquement)<br/>   | D3DFMT \_ A2R10G10B10<br/> D3DFMT \_ A2B10G10R10<br/> | DXGI \_ format \_ R10G10B10A2 \_ uint                                                                                                                                                                         |
| [**XMUDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4)     | D3DDECLTYPE \_ UDEC4N (Xbox uniquement)<br/> D3DDECLTYPE \_ UDEC3N (Xbox uniquement)<br/> | D3DFMT \_ A2R10G10B10<br/> D3DFMT \_ A2B10G10R10<br/> | DXGI \_ format \_ R10G10B10A2 \_ UNORM                                                                                                                                                                        |
| [**XMUNIBBLE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) |                                                                                       | D3DFMT \_ A4R4G4B4, D3DFMT \_ X4R4G4B4                            | DXGI \_ format \_ B4G4R4A4 \_ UNORM (DXGI 1.2 +)                                                                                                                                                               |
| [**XMUSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2)   | D3DDECLTYPE \_ USHORT2                                                                  | D3DFMT \_ G16R16                                                | DXGI \_ format \_ R16G16 \_ uint                                                                                                                                                                              |
| [**XMUSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | D3DDECLTYPE \_ USHORT2N                                                                 | D3DFMT \_ G16R16                                                | DXGI \_ format \_ R16G16 \_ UNORM                                                                                                                                                                             |
| [**XMUSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4)   | D3DDECLTYPE \_ USHORT4 (Xbox uniquement)                                                      | D3DFMT \_ x16x16x16x16                                          | DXGI \_ format \_ R16G16B16A16 \_ uint                                                                                                                                                                        |
| [**XMUSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | D3DDECLTYPE \_ USHORT4N                                                                 | D3DFMT \_ x16x16x16x16                                          | DXGI \_ format \_ R16G16B16A16 \_ UNORM                                                                                                                                                                       |



 

## <a name="global-constants-in-the-directxmath-library"></a>Constantes globales dans la bibliothèque DirectXMath

Pour réduire la taille du segment de données, la bibliothèque DirectXMath utilise la macro [XMGLOBALCONST](xmglobalconst.md) pour utiliser un certain nombre de constantes internes globales dans son implémentation. Par Convention, ces constantes globales internes sont précédées de **g \_ XM**. En règle générale, il s’agit de l’un des types suivants : [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORF32**](xmvectorf32-data-type.md)ou **XMVECTORI32**.

Ces constantes globales internes sont sujettes à modification dans les futures révisions de la bibliothèque DirectXMath. Utilisez des fonctions publiques qui encapsulent les constantes si possible plutôt que d’utiliser directement les valeurs globales de **g \_ XM** . Vous pouvez également déclarer vos propres constantes globales à l’aide de [XMGLOBALCONST](xmglobalconst.md).

## <a name="windows-sse-versus-sse2"></a>Windows SSE et SSE2

Le jeu d’instructions SSE ne prend en charge que les vecteurs à virgule flottante simple précision. DirectXMath doit utiliser le jeu d’instructions SSE2 pour fournir la prise en charge des vecteurs entiers. SSE2 est pris en charge par tous les processeurs Intel depuis l’introduction du Pentium 4, de tous les processeurs AMD K8 et versions ultérieures, ainsi que de tous les processeurs compatibles x64.

> [!Note]  
> Windows 8 pour x86 ou version ultérieure nécessite la prise en charge de SSE2. toutes les versions de Windows x64 requièrent la prise en charge de SSE2. Windows sur arm/ARM64 nécessite un \_ néon arm.

 

## <a name="routine-variants"></a>Variantes de routine

Il existe plusieurs variantes de fonctions DirectXMath qui facilitent votre travail :

-   Fonctions de comparaison pour créer un branchement conditionnel complexe basé sur un plus petit nombre d’opérations de comparaison de vecteurs. Le nom de ces fonctions se termine par « R », par exemple XMVector3InBoundsR. Les fonctions retournent un enregistrement de comparaison en tant que valeur de retour UINT ou en tant que paramètre de sortie UINT. Vous pouvez utiliser les macros **XMComparision \*** pour tester la valeur.
-   Fonctions batch pour effectuer des opérations de style batch sur des tableaux de vecteurs plus grands. Le nom de ces fonctions se termine par « Stream », par exemple [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream). Les fonctions opèrent sur un tableau d’entrées et génèrent un tableau de sorties. En règle générale, ils prennent un Stride d’entrée et de sortie.
-   Fonctions d’estimation qui implémentent une estimation plus rapide au lieu d’un résultat plus lent et plus précis. Le nom de ces fonctions se termine par « est », par exemple [**XMVector3NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalizeest). L’impact sur la qualité et les performances de l’estimation varie d’une plateforme à l’autres, mais nous vous recommandons d’utiliser des variantes d’estimation pour le code dépendant des performances.

## <a name="platform-inconsistencies"></a>Incohérences de la plateforme

La bibliothèque DirectXMath est destinée à être utilisée dans des applications graphiques et des jeux sensibles aux performances. Par conséquent, l’implémentation est conçue pour une vitesse optimale de traitement normal sur toutes les plateformes prises en charge. Les résultats aux conditions limites, en particulier celles qui génèrent des spéciaux à virgule flottante, sont susceptibles de varier de la cible à la cible. ce comportement dépend également d’autres paramètres d’exécution, tels que le mot de contrôle x87 pour la cible non intrinsèque Windows 32 bits ou le mot de contrôle SSE pour Windows 32 bits et 64 bits. En outre, il y aura des différences au sein des conditions limites entre les différents fournisseurs d’UC.

N’utilisez pas DirectXMath dans la science ou d’autres applications où la précision numérique est primordiale. En outre, cette limitation est reflétée dans l’absence de prise en charge des calculs double ou de précision étendue.

> [!Note]  
> Les \_ \_ \_ \_ chemins de code scalaires de non-fonctions XM ne sont généralement pas écrits pour la conformité, et non pour les performances. Leurs résultats de conditions limites varient également.

 

## <a name="platform-specific-extensions"></a>Extensions spécifiques à la plateforme

la bibliothèque DirectXMath est conçue pour simplifier la programmation de C++ SIMD qui offre une excellente prise en charge des plateformes x86, x64 et Windows RT à l’aide d’instructions intrinsèques largement prises en charge (SSE2 et ARM-néon).

Dans certains cas, toutefois, lorsque des instructions spécifiques à la plateforme peuvent s’avérer bénéfiques. En raison de la façon dont DirectXMath est implémenté, dans de nombreux cas, il est facile d’utiliser des types DirectXMath directement dans les instructions d’intrinsèques standard prises en charge par le compilateur, et d’utiliser DirectXMath comme chemin de secours pour les plateformes qui ne prennent pas en charge l’instruction étendue.

Par exemple, voici un exemple simplifié de l’utilisation de l’instruction SSE 4,1 point-Product. Notez que vous devez protéger explicitement le chemin d’accès du code pour éviter de générer des exceptions d’instruction non valides au moment de l’exécution. Assurez-vous que les chemins de code sont suffisamment importants pour justifier le coût supplémentaire de la branche, la complexité de la gestion de plusieurs chemins de code, etc.


```
#include <Windows.h>
#include <stdio.h>

#include <DirectXMath.h>

#include <intrin.h>
#include <smmintrin.h>

using namespace DirectX;

bool g_bSSE41 = false;

void DetectCPUFeatures()
{
#ifndef _M_ARM
   // See __cpuid documentation on MSDN for more information

   int CPUInfo[4] = {-1};
#if defined(__clang__) || defined(__GNUC__)
   __cpuid(0, CPUInfo[0], CPUInfo[1], CPUInfo[2], CPUInfo[3]);
#else
   __cpuid(CPUInfo, 0);
#endif

   if ( CPUInfo[0] >= 1 )
   {
#if defined(__clang__) || defined(__GNUC__)
        __cpuid(1, CPUInfo[0], CPUInfo[1], CPUInfo[2], CPUInfo[3]);
#else
        __cpuid(CPUInfo, 1);
#endif

       if ( CPUInfo[2] & 0x80000 )
           g_bSSE41 = true;
   }
#endif
}

int main()
{
   if ( !XMVerifyCPUSupport() )
       return -1;

   DetectCPUFeatures();

   ...

   XMVECTORF32 v1 = { 1.f, 2.f, 3.f, 4.f };
   XMVECTORF32 v2 = { 5.f, 6.f, 7.f, 8.f };

   XMVECTOR r2, r3, r4;

   if ( g_bSSE41 )
   {
#ifndef _M_ARM
       r2 = _mm_dp_ps( v1, v2, 0x3f );
       r3 = _mm_dp_ps( v1, v2, 0x7f );
       r4 = _mm_dp_ps( v1, v2, 0xff );
#endif
   }
   else
   {
       r2 = XMVector2Dot( v1, v2 );
       r3 = XMVector3Dot( v1, v2 );
       r4 = XMVector4Dot( v1, v2 );
   }

   ...

   return 0;
}
```



Pour plus d’informations sur les extensions spécifiques à une plateforme, consultez :

<dl>

[DirectXMath : SSE, SSE2 et ARM-néon](https://walbourn.github.io/directxmath-sse-sse2-and-arm-neon/)  
[DirectXMath : SSE3 et SSSE3](https://walbourn.github.io/directxmath-sse3-and-ssse3/)  
[DirectXMath : SSE 4.1 et SSE 4.2](https://walbourn.github.io/directxmath-sse4-1-and-sse4-2/)  
[DirectXMath : AVX](https://walbourn.github.io/directxmath-avx/)  
[DirectXMath : F16C et FMA](https://walbourn.github.io/directxmath-f16c-and-fma/)  
[DirectXMath : AVX2](https://walbourn.github.io/directxmath-avx2/)  
[DirectXMath : ARM64](https://walbourn.github.io/directxmath-arm64/)  
</dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>
