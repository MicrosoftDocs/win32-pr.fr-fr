---
title: API d’interopérabilité numériques et DirectXMath Windows (Windowsnumerics. h)
description: Ces fonctions convertissent les types Windows. Foundation. Numerics vers et à partir des types DirectXMath SIMD XMVECTOR et XMMATRIX.
ms.assetid: 05851054-196E-4955-B9C5-85C2E33EF488
keywords:
- API d’interopérabilité numériques et DirectXMath Windows
topic_type:
- apiref
api_name:
- WWindows numerics and DirectXMath interop APIs
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e39057c92eeed87c3f429acb56f0afa2468ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533226"
---
# <a name="windows-numerics-and-directxmath-interop-apis"></a>API d’interopérabilité numériques et DirectXMath Windows

Ces fonctions convertissent les types [**Windows. Foundation. Numerics**](/uwp/api/Windows.Foundation.Numerics) vers et à partir des types DirectXMath SIMD [XMVECTOR](../dxmath/xmvector-data-type.md) et [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).

## <a name="functions"></a>Fonctions

| Nom | Description |
|-|-|
| `XMVECTOR XMLoadFloat2(_In_ float2 const* pSource)` | Charge un float2 dans un [XMVECTOR](../dxmath/xmvector-data-type.md)DirectXMath. |
| `XMVECTOR XMLoadFloat3(_In_ float3 const* pSource)` | Charge un float3 dans un [XMVECTOR](../dxmath/xmvector-data-type.md)DirectXMath. |
| `XMVECTOR XMLoadFloat4(_In_ float4 const* pSource)` | Charge un float4 dans un [XMVECTOR](../dxmath/xmvector-data-type.md)DirectXMath. |
| `XMMATRIX XMLoadFloat3x2(_In_ float3x2 const* pSource)` | Charge un float3x2 dans un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)DirectXMath. |
| `XMMATRIX XMLoadFloat4x4(_In_ float4x4 const* pSource)` | Charge un float4x4 dans un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)DirectXMath. |
| `XMVECTOR XMLoadPlane(_In_ plane const* pSource)` | Charge un plan dans un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)DirectXMath. |
| `XMVECTOR XMLoadQuaternion(_In_ quaternion const* pSource)` | Charge un Quaternion dans un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)DirectXMath. |
| `void XMStoreFloat2(_Out_ float2* pDestination, _In_ FXMVECTOR value)` | Stocke un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath dans un float2. |
| `void XMStoreFloat3(_Out_ float3* pDestination, _In_ FXMVECTOR value)` | Stocke un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath dans un float3. |
| `void XMStoreFloat4(_Out_ float4* pDestination, _In_ FXMVECTOR value)` | Stocke un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath dans un float4. |
| `void XMStoreFloat3x2(_Out_ float3x2* pDestination, _In_ FXMMATRIX value)` | Stocke un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) DirectXMath dans un float3x2. |
| `void XMStoreFloat4x4(_Out_ float4x4* pDestination, _In_ FXMMATRIX value)` | Stocke un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) DirectXMath dans un float4x4. |
| `void XMStorePlane(_Out_ plane* pDestination, _In_ FXMVECTOR value)` | Stocke un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath dans un plan. |
| `void XMStoreQuaternion(_Out_ quaternion* pDestination, _In_ FXMVECTOR value)` | Stocke un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath dans un Quaternion. |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| Espace de noms | DirectX |
| En-tête | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[API windowsnumerics. h](windowsnumerics-h-apis-portal.md)
