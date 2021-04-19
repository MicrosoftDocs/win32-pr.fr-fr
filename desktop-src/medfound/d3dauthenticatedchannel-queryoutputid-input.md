---
description: Contient des données d’entrée pour une \_ requête D3DAUTHENTICATEDQUERY OUTPUTID.
ms.assetid: 8864c298-be9a-4ff4-a9c5-996b62937c18
title: Structure D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7c64d43261ccc849772372110ad73169c698cd0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513957"
---
# <a name="d3dauthenticatedchannel_queryoutputid_input-structure"></a><span data-ttu-id="97010-103">\_ \_ Structure d’entrée D3DAUTHENTICATEDCHANNEL QUERYOUTPUTID</span><span class="sxs-lookup"><span data-stu-id="97010-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_INPUT structure</span></span>

<span data-ttu-id="97010-104">Contient des données d’entrée pour une requête [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md) .</span><span class="sxs-lookup"><span data-stu-id="97010-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_OUTPUTID**](d3dauthenticatedquery-outputid.md) query.</span></span>

<span data-ttu-id="97010-105">Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="97010-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="97010-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97010-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DeviceHandle;
  HANDLE                              CryptoSessionHandle;
  UINT                                OutputIDIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT;
```



## <a name="members"></a><span data-ttu-id="97010-107">Membres</span><span class="sxs-lookup"><span data-stu-id="97010-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="97010-108">**Entrée**</span><span class="sxs-lookup"><span data-stu-id="97010-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="97010-109">Structure [**\_ \_ d’entrée de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) qui contient le GUID de la requête et d’autres données.</span><span class="sxs-lookup"><span data-stu-id="97010-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="97010-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="97010-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="97010-111">Handle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="97010-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="97010-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="97010-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="97010-113">Handle de la session de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="97010-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="97010-114">**OutputIDIndex**</span><span class="sxs-lookup"><span data-stu-id="97010-114">**OutputIDIndex**</span></span>
</dt> <dd>

<span data-ttu-id="97010-115">Index de l’ID de sortie.</span><span class="sxs-lookup"><span data-stu-id="97010-115">The index of the output ID.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97010-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97010-116">Requirements</span></span>



| <span data-ttu-id="97010-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97010-117">Requirement</span></span> | <span data-ttu-id="97010-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="97010-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97010-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97010-119">Minimum supported client</span></span><br/> | <span data-ttu-id="97010-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97010-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="97010-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97010-121">Minimum supported server</span></span><br/> | <span data-ttu-id="97010-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97010-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="97010-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="97010-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="97010-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="97010-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97010-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97010-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97010-126">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="97010-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="97010-127">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="97010-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




