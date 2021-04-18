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
# <a name="windows-numerics-and-directxmath-interop-apis"></a><span data-ttu-id="0ce04-104">API d’interopérabilité numériques et DirectXMath Windows</span><span class="sxs-lookup"><span data-stu-id="0ce04-104">Windows numerics and DirectXMath interop APIs</span></span>

<span data-ttu-id="0ce04-105">Ces fonctions convertissent les types [**Windows. Foundation. Numerics**](/uwp/api/Windows.Foundation.Numerics) vers et à partir des types DirectXMath SIMD [XMVECTOR](../dxmath/xmvector-data-type.md) et [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span><span class="sxs-lookup"><span data-stu-id="0ce04-105">These functions convert [**Windows.Foundation.Numerics**](/uwp/api/Windows.Foundation.Numerics) types to and from the DirectXMath SIMD types [XMVECTOR](../dxmath/xmvector-data-type.md) and [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span>

## <a name="functions"></a><span data-ttu-id="0ce04-106">Fonctions</span><span class="sxs-lookup"><span data-stu-id="0ce04-106">Functions</span></span>

| <span data-ttu-id="0ce04-107">Nom</span><span class="sxs-lookup"><span data-stu-id="0ce04-107">Name</span></span> | <span data-ttu-id="0ce04-108">Description</span><span class="sxs-lookup"><span data-stu-id="0ce04-108">Description</span></span> |
|-|-|
| `XMVECTOR XMLoadFloat2(_In_ float2 const* pSource)` | <span data-ttu-id="0ce04-109">Charge un float2 dans un [XMVECTOR](../dxmath/xmvector-data-type.md)DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="0ce04-109">Loads a float2 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMVECTOR XMLoadFloat3(_In_ float3 const* pSource)` | <span data-ttu-id="0ce04-110">Charge un float3 dans un [XMVECTOR](../dxmath/xmvector-data-type.md)DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="0ce04-110">Loads a float3 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMVECTOR XMLoadFloat4(_In_ float4 const* pSource)` | <span data-ttu-id="0ce04-111">Charge un float4 dans un [XMVECTOR](../dxmath/xmvector-data-type.md)DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="0ce04-111">Loads a float4 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMMATRIX XMLoadFloat3x2(_In_ float3x2 const* pSource)` | <span data-ttu-id="0ce04-112">Charge un float3x2 dans un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="0ce04-112">Loads a float3x2 into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMMATRIX XMLoadFloat4x4(_In_ float4x4 const* pSource)` | <span data-ttu-id="0ce04-113">Charge un float4x4 dans un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="0ce04-113">Loads a float4x4 into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMVECTOR XMLoadPlane(_In_ plane const* pSource)` | <span data-ttu-id="0ce04-114">Charge un plan dans un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="0ce04-114">Loads a plane into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMVECTOR XMLoadQuaternion(_In_ quaternion const* pSource)` | <span data-ttu-id="0ce04-115">Charge un Quaternion dans un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="0ce04-115">Loads a quaternion into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `void XMStoreFloat2(_Out_ float2* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="0ce04-116">Stocke un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath dans un float2.</span><span class="sxs-lookup"><span data-stu-id="0ce04-116">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float2.</span></span> |
| `void XMStoreFloat3(_Out_ float3* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="0ce04-117">Stocke un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath dans un float3.</span><span class="sxs-lookup"><span data-stu-id="0ce04-117">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float3.</span></span> |
| `void XMStoreFloat4(_Out_ float4* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="0ce04-118">Stocke un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath dans un float4.</span><span class="sxs-lookup"><span data-stu-id="0ce04-118">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float4.</span></span> |
| `void XMStoreFloat3x2(_Out_ float3x2* pDestination, _In_ FXMMATRIX value)` | <span data-ttu-id="0ce04-119">Stocke un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) DirectXMath dans un float3x2.</span><span class="sxs-lookup"><span data-stu-id="0ce04-119">Stores a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) into a float3x2.</span></span> |
| `void XMStoreFloat4x4(_Out_ float4x4* pDestination, _In_ FXMMATRIX value)` | <span data-ttu-id="0ce04-120">Stocke un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) DirectXMath dans un float4x4.</span><span class="sxs-lookup"><span data-stu-id="0ce04-120">Stores a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) into a float4x4.</span></span> |
| `void XMStorePlane(_Out_ plane* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="0ce04-121">Stocke un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath dans un plan.</span><span class="sxs-lookup"><span data-stu-id="0ce04-121">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a plane.</span></span> |
| `void XMStoreQuaternion(_Out_ quaternion* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="0ce04-122">Stocke un [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath dans un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="0ce04-122">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a quaternion.</span></span> |

## <a name="requirements"></a><span data-ttu-id="0ce04-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ce04-123">Requirements</span></span>

| <span data-ttu-id="0ce04-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ce04-124">Requirement</span></span> | <span data-ttu-id="0ce04-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ce04-125">Value</span></span> |
|-|-|
| <span data-ttu-id="0ce04-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0ce04-126">Namespace</span></span> | <span data-ttu-id="0ce04-127">DirectX</span><span class="sxs-lookup"><span data-stu-id="0ce04-127">DirectX</span></span> |
| <span data-ttu-id="0ce04-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ce04-128">Header</span></span> | <dl> <span data-ttu-id="0ce04-129"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ce04-129"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="0ce04-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ce04-130">See also</span></span>

[<span data-ttu-id="0ce04-131">API windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="0ce04-131">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
