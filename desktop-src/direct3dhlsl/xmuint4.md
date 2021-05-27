---
title: XMUINT4, structure
description: Décrit un vecteur d’entier non signé 4D.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- XMUINT4 structure HLSL
topic_type:
- apiref
api_name:
- XMUINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e424b4e5fd1c97f5aec01571d887b54dbb143b7
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549894"
---
# <a name="xmuint4-structure"></a><span data-ttu-id="d7f8d-104">XMUINT4, structure</span><span class="sxs-lookup"><span data-stu-id="d7f8d-104">XMUINT4 structure</span></span>

<span data-ttu-id="d7f8d-105">Décrit un vecteur d’entier non signé 4D.</span><span class="sxs-lookup"><span data-stu-id="d7f8d-105">Describes an 4D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f8d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7f8d-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT4 {
  UINT x;
  UINT {
    UINT {
      UINT w;
    }z;
  }y;
} XMUINT4;
```



## <a name="members"></a><span data-ttu-id="d7f8d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d7f8d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d7f8d-108">**x**</span><span class="sxs-lookup"><span data-stu-id="d7f8d-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="d7f8d-109">composant x du vecteur.</span><span class="sxs-lookup"><span data-stu-id="d7f8d-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="d7f8d-110">**y**</span><span class="sxs-lookup"><span data-stu-id="d7f8d-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="d7f8d-111">composant y du vecteur.</span><span class="sxs-lookup"><span data-stu-id="d7f8d-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="d7f8d-112">**Lettre**</span><span class="sxs-lookup"><span data-stu-id="d7f8d-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="d7f8d-113">composant z du vecteur.</span><span class="sxs-lookup"><span data-stu-id="d7f8d-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="d7f8d-114">**w**</span><span class="sxs-lookup"><span data-stu-id="d7f8d-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="d7f8d-115">composant w du vecteur.</span><span class="sxs-lookup"><span data-stu-id="d7f8d-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>




## <a name="remarks"></a><span data-ttu-id="d7f8d-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="d7f8d-116">Remarks</span></span>

<span data-ttu-id="d7f8d-117">Cette structure est définie dans l' ``D3DX\_DXGIFormatConvert.inl`` en-tête dans le kit de développement logiciel (SDK) DirectX (juin 2010) pour une utilisation à partir de C++.</span><span class="sxs-lookup"><span data-stu-id="d7f8d-117">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="d7f8d-118">La dernière version de cet en-tête dans le package NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) ne le définit plus et s’appuie sur [DirectX :: XMUINT4](/windows/win32/api/directxmath/ns-directxmath-xmuint4) dans DirectXMath à la place.</span><span class="sxs-lookup"><span data-stu-id="d7f8d-118">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMUINT4](/windows/win32/api/directxmath/ns-directxmath-xmuint4) in DirectXMath instead.</span></span>




## <a name="requirements"></a><span data-ttu-id="d7f8d-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d7f8d-119">Requirements</span></span>



| <span data-ttu-id="d7f8d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7f8d-120">Requirement</span></span> | <span data-ttu-id="d7f8d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7f8d-121">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f8d-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7f8d-122">Header</span></span><br/> | <dl> <span data-ttu-id="d7f8d-123"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="d7f8d-123"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7f8d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7f8d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f8d-125">Structures</span><span class="sxs-lookup"><span data-stu-id="d7f8d-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="d7f8d-126">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="d7f8d-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>