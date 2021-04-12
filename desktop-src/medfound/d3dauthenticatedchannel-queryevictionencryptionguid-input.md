---
description: Contient des données d’entrée pour une \_ requête D3DAUTHENTICATEDQUERY ENCRYPTIONWHENACCESSIBLEGUID.
ms.assetid: 0e24e393-3f63-4c6f-aca1-f73ced3490ba
title: Structure D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1c4500d27577883f46d00580dcc7e306b4008cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393287"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguid_input-structure"></a><span data-ttu-id="535a4-103">\_ \_ Structure d’entrée D3DAUTHENTICATEDCHANNEL QUERYEVICTIONENCRYPTIONGUID</span><span class="sxs-lookup"><span data-stu-id="535a4-103">D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_INPUT structure</span></span>

<span data-ttu-id="535a4-104">Contient des données d’entrée pour une requête [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .</span><span class="sxs-lookup"><span data-stu-id="535a4-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) query.</span></span>

<span data-ttu-id="535a4-105">Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="535a4-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="535a4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="535a4-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  UINT                                EncryptionGuidIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT;
```



## <a name="members"></a><span data-ttu-id="535a4-107">Membres</span><span class="sxs-lookup"><span data-stu-id="535a4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="535a4-108">**Entrée**</span><span class="sxs-lookup"><span data-stu-id="535a4-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="535a4-109">Structure [**\_ \_ d’entrée de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) qui contient le GUID de la requête et d’autres données.</span><span class="sxs-lookup"><span data-stu-id="535a4-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="535a4-110">**EncryptionGuidIndex**</span><span class="sxs-lookup"><span data-stu-id="535a4-110">**EncryptionGuidIndex**</span></span>
</dt> <dd>

<span data-ttu-id="535a4-111">Index du GUID de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="535a4-111">The index of the encryption GUID.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="535a4-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="535a4-112">Requirements</span></span>



| <span data-ttu-id="535a4-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="535a4-113">Requirement</span></span> | <span data-ttu-id="535a4-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="535a4-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="535a4-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="535a4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="535a4-116">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="535a4-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="535a4-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="535a4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="535a4-118">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="535a4-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="535a4-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="535a4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="535a4-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="535a4-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="535a4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="535a4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="535a4-122">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="535a4-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="535a4-123">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="535a4-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




