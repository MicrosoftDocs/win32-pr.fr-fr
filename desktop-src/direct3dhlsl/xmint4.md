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
ms.openlocfilehash: ead9e7da8d48025c456ae6e57b0ffe64cdb00f46
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549954"
---
# <a name="xmint4-structure"></a><span data-ttu-id="dd4eb-104">XMINT4, structure</span><span class="sxs-lookup"><span data-stu-id="dd4eb-104">XMINT4 structure</span></span>

<span data-ttu-id="dd4eb-105">Décrit un vecteur d’entiers 4D.</span><span class="sxs-lookup"><span data-stu-id="dd4eb-105">Describes an 4D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd4eb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd4eb-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="dd4eb-107">Membres</span><span class="sxs-lookup"><span data-stu-id="dd4eb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="dd4eb-108">**x**</span><span class="sxs-lookup"><span data-stu-id="dd4eb-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="dd4eb-109">composant x du vecteur.</span><span class="sxs-lookup"><span data-stu-id="dd4eb-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="dd4eb-110">**y**</span><span class="sxs-lookup"><span data-stu-id="dd4eb-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="dd4eb-111">composant y du vecteur.</span><span class="sxs-lookup"><span data-stu-id="dd4eb-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="dd4eb-112">**Lettre**</span><span class="sxs-lookup"><span data-stu-id="dd4eb-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="dd4eb-113">composant z du vecteur.</span><span class="sxs-lookup"><span data-stu-id="dd4eb-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="dd4eb-114">**w**</span><span class="sxs-lookup"><span data-stu-id="dd4eb-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="dd4eb-115">composant w du vecteur.</span><span class="sxs-lookup"><span data-stu-id="dd4eb-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd4eb-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dd4eb-116">Requirements</span></span>



| <span data-ttu-id="dd4eb-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd4eb-117">Requirement</span></span> | <span data-ttu-id="dd4eb-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd4eb-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd4eb-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd4eb-119">Header</span></span><br/> | <dl> <span data-ttu-id="dd4eb-120"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="dd4eb-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="remarks"></a><span data-ttu-id="dd4eb-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="dd4eb-121">Remarks</span></span>

<span data-ttu-id="dd4eb-122">Cette structure est définie dans l' ``D3DX\_DXGIFormatConvert.inl`` en-tête dans le kit de développement logiciel (SDK) DirectX (juin 2010) pour une utilisation à partir de C++.</span><span class="sxs-lookup"><span data-stu-id="dd4eb-122">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="dd4eb-123">La dernière version de cet en-tête dans le package NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) ne le définit plus et s’appuie sur [DirectX :: XMINT4](/windows/win32/api/directxmath/ns-directxmath-xmint4) dans DirectXMath à la place.</span><span class="sxs-lookup"><span data-stu-id="dd4eb-123">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT4](/windows/win32/api/directxmath/ns-directxmath-xmint4) in DirectXMath instead.</span></span>



## <a name="see-also"></a><span data-ttu-id="dd4eb-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd4eb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd4eb-125">Structures</span><span class="sxs-lookup"><span data-stu-id="dd4eb-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="dd4eb-126">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="dd4eb-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>