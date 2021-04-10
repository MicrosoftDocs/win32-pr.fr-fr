---
description: Retourne le niveau de protection actuel de l’appareil.
ms.assetid: 335d21e8-2a98-4824-a60d-1969a40e8d24
title: D3DAUTHENTICATEDQUERY_PROTECTION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_PROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 85147d764d5b6580305723e9b05b127b116a660e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201156"
---
# <a name="d3dauthenticatedquery_protection"></a><span data-ttu-id="e4b07-103">\_Protection D3DAUTHENTICATEDQUERY</span><span class="sxs-lookup"><span data-stu-id="e4b07-103">D3DAUTHENTICATEDQUERY\_PROTECTION</span></span>

<span data-ttu-id="e4b07-104">Retourne le niveau de protection actuel de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e4b07-104">Returns the current protection level for the device.</span></span>



| <span data-ttu-id="e4b07-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4b07-105">Requirement</span></span> | <span data-ttu-id="e4b07-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4b07-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b07-107">GUID de la requête</span><span class="sxs-lookup"><span data-stu-id="e4b07-107">Query GUID</span></span>  | <span data-ttu-id="e4b07-108">**\_Protection D3DAUTHENTICATEDQUERY**</span><span class="sxs-lookup"><span data-stu-id="e4b07-108">**D3DAUTHENTICATEDQUERY\_PROTECTION**</span></span>                                                                      |
| <span data-ttu-id="e4b07-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="e4b07-109">Input data</span></span>  | [<span data-ttu-id="e4b07-110">**\_Entrée de requête D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="e4b07-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                       |
| <span data-ttu-id="e4b07-111">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="e4b07-111">Return data</span></span> | [<span data-ttu-id="e4b07-112">**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYPROTECTION \_**</span><span class="sxs-lookup"><span data-stu-id="e4b07-112">**D3DAUTHENTICATEDCHANNEL\_QUERYPROTECTION\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryprotection-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="e4b07-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e4b07-113">Remarks</span></span>

<span data-ttu-id="e4b07-114">Cette requête est valide pour tous les types de canaux.</span><span class="sxs-lookup"><span data-stu-id="e4b07-114">This query is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4b07-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4b07-115">Requirements</span></span>



| <span data-ttu-id="e4b07-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4b07-116">Requirement</span></span> | <span data-ttu-id="e4b07-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4b07-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b07-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4b07-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e4b07-119">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4b07-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e4b07-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4b07-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e4b07-121">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4b07-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e4b07-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4b07-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4b07-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4b07-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4b07-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4b07-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b07-125">Requêtes protection du contenu</span><span class="sxs-lookup"><span data-stu-id="e4b07-125">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="e4b07-126">protection du contenu basé sur GPU</span><span class="sxs-lookup"><span data-stu-id="e4b07-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="e4b07-127">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="e4b07-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




