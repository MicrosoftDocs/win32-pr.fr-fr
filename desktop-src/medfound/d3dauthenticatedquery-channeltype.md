---
description: Retourne le type de canal authentifié.
ms.assetid: eec4b117-a9f2-479d-99d7-e5d4053cf6b4
title: D3DAUTHENTICATEDQUERY_CHANNELTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CHANNELTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 58ac84a0caca5a5709c74adbca567633e12daa10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515951"
---
# <a name="d3dauthenticatedquery_channeltype"></a><span data-ttu-id="570f7-103">D3DAUTHENTICATEDQUERY \_ CHANNELTYPE</span><span class="sxs-lookup"><span data-stu-id="570f7-103">D3DAUTHENTICATEDQUERY\_CHANNELTYPE</span></span>

<span data-ttu-id="570f7-104">Retourne le type de canal authentifié.</span><span class="sxs-lookup"><span data-stu-id="570f7-104">Returns the type of authenticated channel.</span></span>



| <span data-ttu-id="570f7-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="570f7-105">Requirement</span></span> | <span data-ttu-id="570f7-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="570f7-106">Value</span></span> |
|-------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="570f7-107">GUID de la requête</span><span class="sxs-lookup"><span data-stu-id="570f7-107">Query GUID</span></span>  | <span data-ttu-id="570f7-108">**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**</span><span class="sxs-lookup"><span data-stu-id="570f7-108">**D3DAUTHENTICATEDQUERY\_CHANNELTYPE**</span></span>                                                                       |
| <span data-ttu-id="570f7-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="570f7-109">Input data</span></span>  | [<span data-ttu-id="570f7-110">**\_Entrée de requête D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="570f7-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                         |
| <span data-ttu-id="570f7-111">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="570f7-111">Return data</span></span> | [<span data-ttu-id="570f7-112">**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYCHANNELTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="570f7-112">**D3DAUTHENTICATEDCHANNEL\_QUERYCHANNELTYPE\_OUTPUT**</span></span>](d3dauthenticatedchannel-querychanneltype-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="570f7-113">Notes</span><span class="sxs-lookup"><span data-stu-id="570f7-113">Remarks</span></span>

<span data-ttu-id="570f7-114">Cette requête est valide pour tous les types de canaux.</span><span class="sxs-lookup"><span data-stu-id="570f7-114">This query is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="570f7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="570f7-115">Requirements</span></span>



| <span data-ttu-id="570f7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="570f7-116">Requirement</span></span> | <span data-ttu-id="570f7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="570f7-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="570f7-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="570f7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="570f7-119">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="570f7-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="570f7-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="570f7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="570f7-121">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="570f7-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="570f7-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="570f7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="570f7-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="570f7-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="570f7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="570f7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="570f7-125">Requêtes protection du contenu</span><span class="sxs-lookup"><span data-stu-id="570f7-125">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="570f7-126">protection du contenu basé sur GPU</span><span class="sxs-lookup"><span data-stu-id="570f7-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="570f7-127">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="570f7-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




