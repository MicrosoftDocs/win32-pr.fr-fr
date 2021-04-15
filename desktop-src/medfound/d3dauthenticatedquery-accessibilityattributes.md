---
description: Retourne le type de bus d’e/s utilisé pour envoyer des données au GPU.
ms.assetid: 5a180a5c-6798-40ba-9e2c-ce1f755fcc08
title: D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5119da4e7efaf0c27db1065dacc56e3388a77474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393283"
---
# <a name="d3dauthenticatedquery_accessibilityattributes"></a><span data-ttu-id="52f43-103">D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="52f43-103">D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES</span></span>

<span data-ttu-id="52f43-104">Retourne le type de bus d’e/s utilisé pour envoyer des données au GPU.</span><span class="sxs-lookup"><span data-stu-id="52f43-104">Returns the type of I/O bus used to send data to the GPU.</span></span>



| <span data-ttu-id="52f43-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52f43-105">Requirement</span></span> | <span data-ttu-id="52f43-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="52f43-106">Value</span></span> |
|-------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52f43-107">GUID de la requête</span><span class="sxs-lookup"><span data-stu-id="52f43-107">Query GUID</span></span>  | <span data-ttu-id="52f43-108">**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**</span><span class="sxs-lookup"><span data-stu-id="52f43-108">**D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES**</span></span>                                                           |
| <span data-ttu-id="52f43-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="52f43-109">Input data</span></span>  | [<span data-ttu-id="52f43-110">**\_Entrée de requête D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="52f43-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                         |
| <span data-ttu-id="52f43-111">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="52f43-111">Return data</span></span> | [<span data-ttu-id="52f43-112">**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYINFOBUSTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="52f43-112">**D3DAUTHENTICATEDCHANNEL\_QUERYINFOBUSTYPE\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryinfobustype-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="52f43-113">Notes</span><span class="sxs-lookup"><span data-stu-id="52f43-113">Remarks</span></span>

<span data-ttu-id="52f43-114">Cette requête retourne également des informations sur la façon dont le contenu est accessible lorsqu’il est placé dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="52f43-114">This query also returns information about how accessible the content is when put into video memory.</span></span>

<span data-ttu-id="52f43-115">Les types de canaux suivants prennent en charge cette requête :</span><span class="sxs-lookup"><span data-stu-id="52f43-115">The following channel types support this query:</span></span>

-   <span data-ttu-id="52f43-116">**\_Matériel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="52f43-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="52f43-117">**\_Logiciel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="52f43-117">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="52f43-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52f43-118">Requirements</span></span>



| <span data-ttu-id="52f43-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52f43-119">Requirement</span></span> | <span data-ttu-id="52f43-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="52f43-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52f43-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52f43-121">Minimum supported client</span></span><br/> | <span data-ttu-id="52f43-122">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52f43-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="52f43-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52f43-123">Minimum supported server</span></span><br/> | <span data-ttu-id="52f43-124">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52f43-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="52f43-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="52f43-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="52f43-126"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="52f43-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52f43-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52f43-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52f43-128">Requêtes protection du contenu</span><span class="sxs-lookup"><span data-stu-id="52f43-128">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="52f43-129">protection du contenu basé sur GPU</span><span class="sxs-lookup"><span data-stu-id="52f43-129">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="52f43-130">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="52f43-130">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




