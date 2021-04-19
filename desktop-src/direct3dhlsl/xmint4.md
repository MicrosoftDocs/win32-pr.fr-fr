---
title: XMINT4, structure
description: Décrit un vecteur d’entiers 4D.
ms.assetid: 1f21727d-fcb4-4514-b30e-d8ef0e36c256
keywords:
- XMINT4 structure HLSL
topic_type:
- apiref
api_name:
- XMINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d532f3a2a2332874f7b7c22f17992c22984e3f86
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222837"
---
# <a name="xmint4-structure"></a><span data-ttu-id="34ee8-104">XMINT4, structure</span><span class="sxs-lookup"><span data-stu-id="34ee8-104">XMINT4 structure</span></span>

<span data-ttu-id="34ee8-105">Décrit un vecteur d’entiers 4D.</span><span class="sxs-lookup"><span data-stu-id="34ee8-105">Describes an 4D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="34ee8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34ee8-106">Syntax</span></span>


``` syntax
typedef struct _XMINT4 {
  INT x;
  INT {
    INT {
      INT w;
    }z;
  }y;
} XMINT4;
```



## <a name="members"></a><span data-ttu-id="34ee8-107">Membres</span><span class="sxs-lookup"><span data-stu-id="34ee8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="34ee8-108">**x**</span><span class="sxs-lookup"><span data-stu-id="34ee8-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="34ee8-109">composant x du vecteur.</span><span class="sxs-lookup"><span data-stu-id="34ee8-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="34ee8-110">**y**</span><span class="sxs-lookup"><span data-stu-id="34ee8-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="34ee8-111">composant y du vecteur.</span><span class="sxs-lookup"><span data-stu-id="34ee8-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="34ee8-112">**Lettre**</span><span class="sxs-lookup"><span data-stu-id="34ee8-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="34ee8-113">composant z du vecteur.</span><span class="sxs-lookup"><span data-stu-id="34ee8-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="34ee8-114">**w**</span><span class="sxs-lookup"><span data-stu-id="34ee8-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="34ee8-115">composant w du vecteur.</span><span class="sxs-lookup"><span data-stu-id="34ee8-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34ee8-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34ee8-116">Requirements</span></span>



| <span data-ttu-id="34ee8-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34ee8-117">Requirement</span></span> | <span data-ttu-id="34ee8-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="34ee8-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34ee8-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="34ee8-119">Header</span></span><br/> | <dl> <span data-ttu-id="34ee8-120"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="34ee8-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="remarks"></a><span data-ttu-id="34ee8-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="34ee8-121">Remarks</span></span>

<span data-ttu-id="34ee8-122">Cette structure est définie dans l' ``D3DX\_DXGIFormatConvert.inl`` en-tête dans le kit de développement logiciel (SDK) DirectX (juin 2010) pour une utilisation à partir de C++.</span><span class="sxs-lookup"><span data-stu-id="34ee8-122">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="34ee8-123">La dernière version de cet en-tête dans le package NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) ne le définit plus et s’appuie sur [DirectX :: XMINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint4) dans DirectXMath à la place.</span><span class="sxs-lookup"><span data-stu-id="34ee8-123">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint4) in DirectXMath instead.</span></span>



## <a name="see-also"></a><span data-ttu-id="34ee8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34ee8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34ee8-125">Structures</span><span class="sxs-lookup"><span data-stu-id="34ee8-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="34ee8-126">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="34ee8-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
