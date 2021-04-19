---
description: Contient des données d’entrée pour une \_ requête D3DAUTHENTICATEDQUERY RESTRICTEDSHAREDRESOURCEPROCESS.
ms.assetid: a1ceb394-7af9-4f05-9f58-a3103bf0150e
title: Structure D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 06c4421f048af80186077da022fdecfaea79dca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517209"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_input-structure"></a><span data-ttu-id="2f9d5-103">\_ \_ Structure d’entrée D3DAUTHENTICATEDCHANNEL QUERYRESTRICTEDSHAREDRESOURCEPROCESS</span><span class="sxs-lookup"><span data-stu-id="2f9d5-103">D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_INPUT structure</span></span>

<span data-ttu-id="2f9d5-104">Contient des données d’entrée pour une requête [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .</span><span class="sxs-lookup"><span data-stu-id="2f9d5-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) query.</span></span>

<span data-ttu-id="2f9d5-105">Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="2f9d5-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f9d5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f9d5-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  UINT                                ProcessIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT;
```



## <a name="members"></a><span data-ttu-id="2f9d5-107">Membres</span><span class="sxs-lookup"><span data-stu-id="2f9d5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2f9d5-108">**Entrée**</span><span class="sxs-lookup"><span data-stu-id="2f9d5-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="2f9d5-109">Structure [**\_ \_ d’entrée de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) qui contient le GUID de la requête et d’autres données.</span><span class="sxs-lookup"><span data-stu-id="2f9d5-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="2f9d5-110">**ProcessIndex**</span><span class="sxs-lookup"><span data-stu-id="2f9d5-110">**ProcessIndex**</span></span>
</dt> <dd>

<span data-ttu-id="2f9d5-111">Index du processus.</span><span class="sxs-lookup"><span data-stu-id="2f9d5-111">The index of the process.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f9d5-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f9d5-112">Requirements</span></span>



| <span data-ttu-id="2f9d5-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f9d5-113">Requirement</span></span> | <span data-ttu-id="2f9d5-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f9d5-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f9d5-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f9d5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2f9d5-116">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f9d5-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2f9d5-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f9d5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2f9d5-118">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f9d5-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2f9d5-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f9d5-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f9d5-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f9d5-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f9d5-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f9d5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f9d5-122">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="2f9d5-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="2f9d5-123">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="2f9d5-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




