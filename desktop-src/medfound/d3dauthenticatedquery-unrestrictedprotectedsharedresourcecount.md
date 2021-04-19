---
description: Retourne le nombre de ressources partagées protégées qui peuvent être ouvertes par n’importe quel processus sans restrictions.
ms.assetid: afbd7bb9-de71-4992-919e-e1517228dc69
title: D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b2d834927d21c59ed5c70dcf3a001d100340405d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517208"
---
# <a name="d3dauthenticatedquery_unrestrictedprotectedsharedresourcecount"></a><span data-ttu-id="e1782-103">D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT</span><span class="sxs-lookup"><span data-stu-id="e1782-103">D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT</span></span>

<span data-ttu-id="e1782-104">Retourne le nombre de ressources partagées protégées qui peuvent être ouvertes par n’importe quel processus sans restrictions.</span><span class="sxs-lookup"><span data-stu-id="e1782-104">Returns the number of protected shared resources that can be opened by any process without restrictions.</span></span>



| <span data-ttu-id="e1782-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1782-105">Requirement</span></span> | <span data-ttu-id="e1782-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1782-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1782-107">GUID de la requête</span><span class="sxs-lookup"><span data-stu-id="e1782-107">Query GUID</span></span>  | <span data-ttu-id="e1782-108">**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**</span><span class="sxs-lookup"><span data-stu-id="e1782-108">**D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**</span></span>                                                                                                    |
| <span data-ttu-id="e1782-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="e1782-109">Input data</span></span>  | [<span data-ttu-id="e1782-110">**\_Entrée de requête D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="e1782-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                                                   |
| <span data-ttu-id="e1782-111">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="e1782-111">Return data</span></span> | [<span data-ttu-id="e1782-112">**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT \_**</span><span class="sxs-lookup"><span data-stu-id="e1782-112">**D3DAUTHENTICATEDCHANNEL\_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="e1782-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e1782-113">Remarks</span></span>

<span data-ttu-id="e1782-114">Le seul type de canal qui prend en charge cette requête est **D3DAUTHENTICATEDCHANNEL \_ Driver \_ Software**.</span><span class="sxs-lookup"><span data-stu-id="e1782-114">The only channel type that supports this query is **D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1782-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1782-115">Requirements</span></span>



| <span data-ttu-id="e1782-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1782-116">Requirement</span></span> | <span data-ttu-id="e1782-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1782-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1782-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1782-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e1782-119">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1782-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e1782-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1782-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e1782-121">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1782-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e1782-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1782-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1782-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1782-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1782-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1782-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1782-125">Requêtes protection du contenu</span><span class="sxs-lookup"><span data-stu-id="e1782-125">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="e1782-126">protection du contenu basé sur GPU</span><span class="sxs-lookup"><span data-stu-id="e1782-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="e1782-127">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="e1782-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




