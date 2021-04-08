---
description: Contient des données d’entrée pour une \_ requête D3DAUTHENTICATEDQUERY OUTPUTIDCOUNT.
ms.assetid: cc68b39f-4645-46a6-a752-549b070cf23b
title: Structure D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 93f58bcd05efb8c173986186d631c713195d8363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111815"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_input-structure"></a><span data-ttu-id="fd0af-103">\_ \_ Structure d’entrée D3DAUTHENTICATEDCHANNEL QUERYOUTPUTIDCOUNT</span><span class="sxs-lookup"><span data-stu-id="fd0af-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_INPUT structure</span></span>

<span data-ttu-id="fd0af-104">Contient des données d’entrée pour une requête [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) .</span><span class="sxs-lookup"><span data-stu-id="fd0af-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) query.</span></span>

<span data-ttu-id="fd0af-105">Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="fd0af-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd0af-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd0af-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DeviceHandle;
  HANDLE                              CryptoSessionHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT;
```



## <a name="members"></a><span data-ttu-id="fd0af-107">Membres</span><span class="sxs-lookup"><span data-stu-id="fd0af-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="fd0af-108">**Entrée**</span><span class="sxs-lookup"><span data-stu-id="fd0af-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="fd0af-109">Structure [**\_ \_ d’entrée de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) qui contient le GUID de la requête et d’autres données.</span><span class="sxs-lookup"><span data-stu-id="fd0af-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="fd0af-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="fd0af-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="fd0af-111">Handle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fd0af-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="fd0af-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="fd0af-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="fd0af-113">Handle de la session de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="fd0af-113">A handle to the cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd0af-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd0af-114">Requirements</span></span>



| <span data-ttu-id="fd0af-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd0af-115">Requirement</span></span> | <span data-ttu-id="fd0af-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd0af-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd0af-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd0af-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fd0af-118">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd0af-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fd0af-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd0af-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fd0af-120">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd0af-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fd0af-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd0af-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd0af-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd0af-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd0af-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd0af-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd0af-124">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="fd0af-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="fd0af-125">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="fd0af-125">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




