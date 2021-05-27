---
title: XMUINT2, structure
description: Décrit un vecteur d’entier non signé 2D.
ms.assetid: 8622eca1-fc8f-4129-a375-142b4f4018b0
keywords:
- XMUINT2 structure HLSL
topic_type:
- apiref
api_name:
- XMUINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71168d08b8a91e09429a6f4e004c48c699635414
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549564"
---
# <a name="xmuint2-structure"></a><span data-ttu-id="9d1d5-104">XMUINT2, structure</span><span class="sxs-lookup"><span data-stu-id="9d1d5-104">XMUINT2 structure</span></span>

<span data-ttu-id="9d1d5-105">Décrit un vecteur d’entier non signé 2D.</span><span class="sxs-lookup"><span data-stu-id="9d1d5-105">Describes an 2D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d1d5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d1d5-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT2 {
  UINT x;
  UINT y;
} XMUINT2;
```



## <a name="members"></a><span data-ttu-id="9d1d5-107">Membres</span><span class="sxs-lookup"><span data-stu-id="9d1d5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9d1d5-108">**x**</span><span class="sxs-lookup"><span data-stu-id="9d1d5-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="9d1d5-109">composant x du vecteur.</span><span class="sxs-lookup"><span data-stu-id="9d1d5-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="9d1d5-110">**y**</span><span class="sxs-lookup"><span data-stu-id="9d1d5-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="9d1d5-111">composant y du vecteur.</span><span class="sxs-lookup"><span data-stu-id="9d1d5-111">y-component of the vector.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="9d1d5-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="9d1d5-112">Remarks</span></span>

<span data-ttu-id="9d1d5-113">Cette structure est définie dans l' ``D3DX\_DXGIFormatConvert.inl`` en-tête dans le kit de développement logiciel (SDK) DirectX (juin 2010) pour une utilisation à partir de C++.</span><span class="sxs-lookup"><span data-stu-id="9d1d5-113">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="9d1d5-114">La dernière version de cet en-tête dans le package NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) ne le définit plus et s’appuie sur [DirectX :: XMUINT2](/windows/win32/api/directxmath/ns-directxmath-xmuint2) dans DirectXMath à la place.</span><span class="sxs-lookup"><span data-stu-id="9d1d5-114">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMUINT2](/windows/win32/api/directxmath/ns-directxmath-xmuint2) in DirectXMath instead.</span></span>



## <a name="requirements"></a><span data-ttu-id="9d1d5-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9d1d5-115">Requirements</span></span>



| <span data-ttu-id="9d1d5-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d1d5-116">Requirement</span></span> | <span data-ttu-id="9d1d5-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d1d5-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d1d5-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d1d5-118">Header</span></span><br/> | <dl> <span data-ttu-id="9d1d5-119"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="9d1d5-119"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d1d5-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d1d5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d1d5-121">Structures</span><span class="sxs-lookup"><span data-stu-id="9d1d5-121">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="9d1d5-122">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="9d1d5-122">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>