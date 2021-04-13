---
description: Contient un vecteur d’initialisation (IV) pour le chiffrement par bloc du mode de chiffrement par blocs 128 Advanced Encryption Standard bits (AES-CTR).
ms.assetid: 2ee738c2-d56c-4a50-94b8-b7180918aa8c
title: Structure D3DAES_CTR_IV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAES_CTR_IV
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6e0d543fb0e57ae34f181e7ff0f40a1a1f8222b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317993"
---
# <a name="d3daes_ctr_iv-structure"></a><span data-ttu-id="69090-103">Structure D3DAESs \_ \_ CS</span><span class="sxs-lookup"><span data-stu-id="69090-103">D3DAES\_CTR\_IV structure</span></span>

<span data-ttu-id="69090-104">Contient un vecteur d’initialisation (IV) pour le chiffrement par bloc du mode de chiffrement par blocs 128 Advanced Encryption Standard bits (AES-CTR).</span><span class="sxs-lookup"><span data-stu-id="69090-104">Contains an initialization vector (IV) for 128-bit Advanced Encryption Standard CTR mode (AES-CTR) block cipher encryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="69090-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69090-105">Syntax</span></span>


```C++
typedef struct _D3DAES_CTR_IV {
  UINT64 IV;
  UINT64 Count;
} D3DAES_CTR_IV;
```



## <a name="members"></a><span data-ttu-id="69090-106">Membres</span><span class="sxs-lookup"><span data-stu-id="69090-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="69090-107">**IV**</span><span class="sxs-lookup"><span data-stu-id="69090-107">**IV**</span></span>
</dt> <dd>

<span data-ttu-id="69090-108">IV, au format Big-endian.</span><span class="sxs-lookup"><span data-stu-id="69090-108">The IV, in big-endian format.</span></span>

</dd> <dt>

<span data-ttu-id="69090-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="69090-109">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="69090-110">Nombre de blocs, au format Big-endian.</span><span class="sxs-lookup"><span data-stu-id="69090-110">The block count, in big-endian format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69090-111">Notes</span><span class="sxs-lookup"><span data-stu-id="69090-111">Remarks</span></span>

<span data-ttu-id="69090-112">La structure **D3DAES \_ CTR \_ IV** et la structure [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) sont équivalentes.</span><span class="sxs-lookup"><span data-stu-id="69090-112">The **D3DAES\_CTR\_IV** structure and the [**DXVA2\_AES\_CTR\_IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) structure are equivalent.</span></span>

<span data-ttu-id="69090-113">Pour plus d’informations, voir [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).</span><span class="sxs-lookup"><span data-stu-id="69090-113">For details, see [**DXVA2\_AES\_CTR\_IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).</span></span>

## <a name="requirements"></a><span data-ttu-id="69090-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69090-114">Requirements</span></span>



| <span data-ttu-id="69090-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69090-115">Requirement</span></span> | <span data-ttu-id="69090-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="69090-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69090-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69090-117">Minimum supported client</span></span><br/> | <span data-ttu-id="69090-118">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69090-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="69090-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69090-119">Minimum supported server</span></span><br/> | <span data-ttu-id="69090-120">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69090-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="69090-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="69090-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="69090-122"><dt>D3d9types. h (inclure d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69090-122"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69090-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69090-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69090-124">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="69090-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




