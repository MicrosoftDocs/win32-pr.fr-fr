---
description: Paramètre de compression de l’harmonique sphérique (SH).
ms.assetid: 214d6efb-419d-4eea-8360-322885c26bc3
title: Énumération D3DXSHCOMPRESSQUALITYTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHCOMPRESSQUALITYTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: d61c70317505442ca4911a13dac8566f9bd7c6fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211743"
---
# <a name="d3dxshcompressqualitytype-enumeration"></a><span data-ttu-id="5b26a-103">Énumération D3DXSHCOMPRESSQUALITYTYPE</span><span class="sxs-lookup"><span data-stu-id="5b26a-103">D3DXSHCOMPRESSQUALITYTYPE enumeration</span></span>

<span data-ttu-id="5b26a-104">Paramètre de compression de l’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="5b26a-104">Spherical harmonic (SH) compression setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b26a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b26a-105">Syntax</span></span>


```C++
typedef enum D3DXSHCOMPRESSQUALITYTYPE { 
  D3DXSHCQUAL_FASTLOWQUALITY   = 1,
  D3DXSHCQUAL_SLOWHIGHQUALITY  = 2,
  D3DXSHCQUAL_FORCE_DWORD      = 0x7fffffff
} D3DXSHCOMPRESSQUALITYTYPE, *LPD3DXSHCOMPRESSQUALITYTYPE;
```



## <a name="constants"></a><span data-ttu-id="5b26a-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="5b26a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5b26a-107"><span id="D3DXSHCQUAL_FASTLOWQUALITY"></span><span id="d3dxshcqual_fastlowquality"></span>**D3DXSHCQUAL \_ FASTLOWQUALITY**</span><span class="sxs-lookup"><span data-stu-id="5b26a-107"><span id="D3DXSHCQUAL_FASTLOWQUALITY"></span><span id="d3dxshcqual_fastlowquality"></span>**D3DXSHCQUAL\_FASTLOWQUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="5b26a-108">La compression des données est de faible qualité, mais elle est rapide à compresser.</span><span class="sxs-lookup"><span data-stu-id="5b26a-108">The data compression is low quality, but is fast to compress.</span></span>

</dd> <dt>

<span data-ttu-id="5b26a-109"><span id="D3DXSHCQUAL_SLOWHIGHQUALITY"></span><span id="d3dxshcqual_slowhighquality"></span>**D3DXSHCQUAL \_ SLOWHIGHQUALITY**</span><span class="sxs-lookup"><span data-stu-id="5b26a-109"><span id="D3DXSHCQUAL_SLOWHIGHQUALITY"></span><span id="d3dxshcqual_slowhighquality"></span>**D3DXSHCQUAL\_SLOWHIGHQUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="5b26a-110">La compression des données est de haute qualité, mais elle est lente à compresser.</span><span class="sxs-lookup"><span data-stu-id="5b26a-110">The data compression is high quality, but is slow to compress.</span></span>

</dd> <dt>

<span data-ttu-id="5b26a-111"><span id="D3DXSHCQUAL_FORCE_DWORD"></span><span id="d3dxshcqual_force_dword"></span>**D3DXSHCQUAL \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="5b26a-111"><span id="D3DXSHCQUAL_FORCE_DWORD"></span><span id="d3dxshcqual_force_dword"></span>**D3DXSHCQUAL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="5b26a-112">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="5b26a-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="5b26a-113">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5b26a-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="5b26a-114">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5b26a-114">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b26a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b26a-115">Requirements</span></span>



| <span data-ttu-id="5b26a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b26a-116">Requirement</span></span> | <span data-ttu-id="5b26a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b26a-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b26a-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b26a-118">Header</span></span><br/> | <dl> <span data-ttu-id="5b26a-119"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b26a-119"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b26a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b26a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b26a-121">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="5b26a-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




