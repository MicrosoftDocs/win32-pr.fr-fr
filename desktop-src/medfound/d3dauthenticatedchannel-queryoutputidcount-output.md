---
description: Contient la réponse à une \_ requête D3DAUTHENTICATEDQUERY OUTPUTIDCOUNT.
ms.assetid: 8b9fa0dc-bbe5-4382-8acc-59aeadfca825
title: Structure D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 86a840de2b36b7089b31d15e8375c17a0610b77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484089"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_output-structure"></a><span data-ttu-id="83bd6-103">\_Structure de \_ sortie D3DAUTHENTICATEDCHANNEL QUERYOUTPUTIDCOUNT</span><span class="sxs-lookup"><span data-stu-id="83bd6-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="83bd6-104">Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) .</span><span class="sxs-lookup"><span data-stu-id="83bd6-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) query.</span></span>

<span data-ttu-id="83bd6-105">Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="83bd6-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="83bd6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83bd6-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DeviceHandle;
  HANDLE                               CryptoSessionHandle;
  UINT                                 NumOutputIDs;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="83bd6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="83bd6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="83bd6-108">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="83bd6-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="83bd6-109">Une structure de [**\_ \_ sortie de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) contenant un code d’Authentification de message (Mac) et d’autres données.</span><span class="sxs-lookup"><span data-stu-id="83bd6-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="83bd6-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="83bd6-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="83bd6-111">Handle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="83bd6-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="83bd6-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="83bd6-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="83bd6-113">Handle de la session de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="83bd6-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="83bd6-114">**NumOutputIDs**</span><span class="sxs-lookup"><span data-stu-id="83bd6-114">**NumOutputIDs**</span></span>
</dt> <dd>

<span data-ttu-id="83bd6-115">Nombre d’ID de sortie associés à l’appareil et à la session de chiffrement spécifiés.</span><span class="sxs-lookup"><span data-stu-id="83bd6-115">The number of output IDs associated with the specified device and cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="83bd6-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83bd6-116">Requirements</span></span>



| <span data-ttu-id="83bd6-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83bd6-117">Requirement</span></span> | <span data-ttu-id="83bd6-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="83bd6-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83bd6-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83bd6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="83bd6-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83bd6-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="83bd6-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83bd6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="83bd6-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83bd6-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="83bd6-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="83bd6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="83bd6-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="83bd6-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83bd6-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83bd6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83bd6-126">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="83bd6-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="83bd6-127">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="83bd6-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




