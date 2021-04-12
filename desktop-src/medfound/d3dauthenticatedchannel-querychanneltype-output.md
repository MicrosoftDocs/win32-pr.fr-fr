---
description: Contient la réponse à une \_ requête D3DAUTHENTICATEDQUERY CHANNELTYPE.
ms.assetid: 547f7f26-2b9d-48b1-97cc-84a2202c3900
title: Structure D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a3120669da69f13359f49d8b8c38ed7d3e211a8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393291"
---
# <a name="d3dauthenticatedchannel_querychanneltype_output-structure"></a><span data-ttu-id="5357b-103">\_Structure de \_ sortie D3DAUTHENTICATEDCHANNEL QUERYCHANNELTYPE</span><span class="sxs-lookup"><span data-stu-id="5357b-103">D3DAUTHENTICATEDCHANNEL\_QUERYCHANNELTYPE\_OUTPUT structure</span></span>

<span data-ttu-id="5357b-104">Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) .</span><span class="sxs-lookup"><span data-stu-id="5357b-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) query.</span></span>

<span data-ttu-id="5357b-105">Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="5357b-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="5357b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5357b-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  D3DAUTHENTICATEDCHANNELTYPE          ChannelType;
} D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="5357b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="5357b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5357b-108">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="5357b-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="5357b-109">Une structure de [**\_ \_ sortie de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) contenant un code d’Authentification de message (Mac) et d’autres données.</span><span class="sxs-lookup"><span data-stu-id="5357b-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="5357b-110">**ChannelType**</span><span class="sxs-lookup"><span data-stu-id="5357b-110">**ChannelType**</span></span>
</dt> <dd>

<span data-ttu-id="5357b-111">Valeur [**D3DAUTHENTICATEDCHANNELTYPE**](d3dauthenticatedchanneltype.md) qui spécifie le type de canal.</span><span class="sxs-lookup"><span data-stu-id="5357b-111">A [**D3DAUTHENTICATEDCHANNELTYPE**](d3dauthenticatedchanneltype.md) value that specifies the channel type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5357b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5357b-112">Requirements</span></span>



| <span data-ttu-id="5357b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5357b-113">Requirement</span></span> | <span data-ttu-id="5357b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="5357b-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5357b-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5357b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5357b-116">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5357b-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5357b-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5357b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5357b-118">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5357b-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5357b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="5357b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="5357b-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5357b-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5357b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5357b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5357b-122">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="5357b-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="5357b-123">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="5357b-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




