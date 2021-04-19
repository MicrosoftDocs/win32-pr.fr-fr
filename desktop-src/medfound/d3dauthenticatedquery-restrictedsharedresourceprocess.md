---
description: Retourne des informations sur un processus autorisé à ouvrir des ressources partagées avec un accès restreint.
ms.assetid: 669d9623-3a96-4661-9dae-3f283a990fe8
title: D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 74bb829510fee4425648412f58d4f7cea74b1f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515186"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocess"></a><span data-ttu-id="ac2e9-103">D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS</span><span class="sxs-lookup"><span data-stu-id="ac2e9-103">D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS</span></span>

<span data-ttu-id="ac2e9-104">Retourne des informations sur un processus autorisé à ouvrir des ressources partagées avec un accès restreint.</span><span class="sxs-lookup"><span data-stu-id="ac2e9-104">Returns information about a process that is allowed to open shared resources with restricted access.</span></span>



| <span data-ttu-id="ac2e9-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac2e9-105">Requirement</span></span> | <span data-ttu-id="ac2e9-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac2e9-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac2e9-107">GUID de la requête</span><span class="sxs-lookup"><span data-stu-id="ac2e9-107">Query GUID</span></span>  | <span data-ttu-id="ac2e9-108">**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**</span><span class="sxs-lookup"><span data-stu-id="ac2e9-108">**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS**</span></span>                                                                                           |
| <span data-ttu-id="ac2e9-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="ac2e9-109">Input data</span></span>  | [<span data-ttu-id="ac2e9-110">**\_Entrée D3DAUTHENTICATEDCHANNEL QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_**</span><span class="sxs-lookup"><span data-stu-id="ac2e9-110">**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_INPUT**</span></span>](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-input.md)   |
| <span data-ttu-id="ac2e9-111">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="ac2e9-111">Return data</span></span> | [<span data-ttu-id="ac2e9-112">**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_**</span><span class="sxs-lookup"><span data-stu-id="ac2e9-112">**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="ac2e9-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ac2e9-113">Remarks</span></span>

<span data-ttu-id="ac2e9-114">Les types de canaux suivants prennent en charge cette requête :</span><span class="sxs-lookup"><span data-stu-id="ac2e9-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="ac2e9-115">**D3DAUTHENTICATEDCHANNEL \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="ac2e9-115">**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
-   <span data-ttu-id="ac2e9-116">**\_Logiciel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="ac2e9-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="ac2e9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac2e9-117">Requirements</span></span>



| <span data-ttu-id="ac2e9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac2e9-118">Requirement</span></span> | <span data-ttu-id="ac2e9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac2e9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac2e9-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac2e9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ac2e9-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac2e9-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ac2e9-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac2e9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ac2e9-123">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac2e9-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ac2e9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="ac2e9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac2e9-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac2e9-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac2e9-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac2e9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac2e9-127">Requêtes protection du contenu</span><span class="sxs-lookup"><span data-stu-id="ac2e9-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="ac2e9-128">protection du contenu basé sur GPU</span><span class="sxs-lookup"><span data-stu-id="ac2e9-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="ac2e9-129">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="ac2e9-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




