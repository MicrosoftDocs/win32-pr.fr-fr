---
description: Contient la réponse à une \_ requête D3DAUTHENTICATEDQUERY OUTPUTID.
ms.assetid: 4dfd1d65-b203-456a-bc9b-527906bcf87e
title: Structure D3DAUTHENTICATEDCHANNEL_QUERYROUTPUTID_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 26686126fd2a5cb942c88ea485f753d2432499dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033809"
---
# <a name="d3dauthenticatedchannel_queryroutputid_output-structure"></a><span data-ttu-id="1b3d3-103">\_Structure de \_ sortie D3DAUTHENTICATEDCHANNEL QUERYROUTPUTID</span><span class="sxs-lookup"><span data-stu-id="1b3d3-103">D3DAUTHENTICATEDCHANNEL\_QUERYROUTPUTID\_OUTPUT structure</span></span>

<span data-ttu-id="1b3d3-104">Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md) .</span><span class="sxs-lookup"><span data-stu-id="1b3d3-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_OUTPUTID**](d3dauthenticatedquery-outputid.md) query.</span></span>

<span data-ttu-id="1b3d3-105">Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="1b3d3-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="1b3d3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b3d3-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  HANDLE DeviceHandle;
  HANDLE CryptoSessionHandle;
  UINT   OutputIDIndex;
  UINT64 OutputID;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="1b3d3-107">Membres</span><span class="sxs-lookup"><span data-stu-id="1b3d3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1b3d3-108">**Sortie de la \_ requête D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="1b3d3-108">**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="1b3d3-109">Une structure de [**\_ \_ sortie de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) contenant un code d’Authentification de message (Mac) et d’autres données.</span><span class="sxs-lookup"><span data-stu-id="1b3d3-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="1b3d3-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="1b3d3-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="1b3d3-111">Handle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1b3d3-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="1b3d3-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="1b3d3-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="1b3d3-113">Handle de la session de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="1b3d3-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="1b3d3-114">**OutputIDIndex**</span><span class="sxs-lookup"><span data-stu-id="1b3d3-114">**OutputIDIndex**</span></span>
</dt> <dd>

<span data-ttu-id="1b3d3-115">Index de l’ID de sortie donné dans le membre **OutputID** .</span><span class="sxs-lookup"><span data-stu-id="1b3d3-115">The index of the output ID given in the **OutputID** member.</span></span>

</dd> <dt>

<span data-ttu-id="1b3d3-116">**OutputID**</span><span class="sxs-lookup"><span data-stu-id="1b3d3-116">**OutputID**</span></span>
</dt> <dd>

<span data-ttu-id="1b3d3-117">ID de sortie associé à l’appareil et à la session de chiffrement spécifiés.</span><span class="sxs-lookup"><span data-stu-id="1b3d3-117">An output ID that is associated with the specified device and cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b3d3-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b3d3-118">Requirements</span></span>



| <span data-ttu-id="1b3d3-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b3d3-119">Requirement</span></span> | <span data-ttu-id="1b3d3-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b3d3-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b3d3-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b3d3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1b3d3-122">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b3d3-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1b3d3-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b3d3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1b3d3-124">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b3d3-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1b3d3-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b3d3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b3d3-126"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b3d3-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b3d3-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b3d3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b3d3-128">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="1b3d3-128">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="1b3d3-129">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="1b3d3-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




