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
ms.openlocfilehash: 7e461d5b10f01f61de3fcfd721c4a6b1350c7d68
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222847"
---
# <a name="xmuint4-structure"></a><span data-ttu-id="95e42-104">XMUINT4, structure</span><span class="sxs-lookup"><span data-stu-id="95e42-104">XMUINT4 structure</span></span>

<span data-ttu-id="95e42-105">Décrit un vecteur d’entier non signé 4D.</span><span class="sxs-lookup"><span data-stu-id="95e42-105">Describes an 4D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="95e42-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95e42-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="95e42-107">Membres</span><span class="sxs-lookup"><span data-stu-id="95e42-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="95e42-108">**x**</span><span class="sxs-lookup"><span data-stu-id="95e42-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="95e42-109">composant x du vecteur.</span><span class="sxs-lookup"><span data-stu-id="95e42-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="95e42-110">**y**</span><span class="sxs-lookup"><span data-stu-id="95e42-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="95e42-111">composant y du vecteur.</span><span class="sxs-lookup"><span data-stu-id="95e42-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="95e42-112">**Lettre**</span><span class="sxs-lookup"><span data-stu-id="95e42-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="95e42-113">composant z du vecteur.</span><span class="sxs-lookup"><span data-stu-id="95e42-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="95e42-114">**w**</span><span class="sxs-lookup"><span data-stu-id="95e42-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="95e42-115">composant w du vecteur.</span><span class="sxs-lookup"><span data-stu-id="95e42-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>




## <a name="remarks"></a><span data-ttu-id="95e42-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="95e42-116">Remarks</span></span>

<span data-ttu-id="95e42-117">Cette structure est définie dans l' ``D3DX\_DXGIFormatConvert.inl`` en-tête dans le kit de développement logiciel (SDK) DirectX (juin 2010) pour une utilisation à partir de C++.</span><span class="sxs-lookup"><span data-stu-id="95e42-117">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="95e42-118">La dernière version de cet en-tête dans le package NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) ne le définit plus et s’appuie sur [DirectX :: XMUINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmuint4) dans DirectXMath à la place.</span><span class="sxs-lookup"><span data-stu-id="95e42-118">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMUINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmuint4) in DirectXMath instead.</span></span>




## <a name="requirements"></a><span data-ttu-id="95e42-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95e42-119">Requirements</span></span>



| <span data-ttu-id="95e42-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95e42-120">Requirement</span></span> | <span data-ttu-id="95e42-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="95e42-121">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95e42-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="95e42-122">Header</span></span><br/> | <dl> <span data-ttu-id="95e42-123"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="95e42-123"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95e42-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95e42-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95e42-125">Structures</span><span class="sxs-lookup"><span data-stu-id="95e42-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="95e42-126">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="95e42-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
