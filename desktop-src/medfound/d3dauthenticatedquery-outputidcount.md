---
description: Retourne le nombre d’identificateurs de sortie associés à une session de chiffrement et un périphérique Direct3D spécifiés.
ms.assetid: a5b17250-6a40-40a9-93b6-3b98b56b09d6
title: D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 624b9ca0ee96f71fb9d3cb655aa9c10030a40efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749292"
---
# <a name="d3dauthenticatedquery_outputidcount"></a><span data-ttu-id="984c6-103">D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT</span><span class="sxs-lookup"><span data-stu-id="984c6-103">D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT</span></span>

<span data-ttu-id="984c6-104">Retourne le nombre d’identificateurs de sortie associés à une session de chiffrement et un périphérique Direct3D spécifiés.</span><span class="sxs-lookup"><span data-stu-id="984c6-104">Returns the number of output identifiers associated with a specified cryptographic session and Direct3D device.</span></span>



| <span data-ttu-id="984c6-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="984c6-105">Requirement</span></span> | <span data-ttu-id="984c6-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="984c6-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="984c6-107">GUID de la requête</span><span class="sxs-lookup"><span data-stu-id="984c6-107">Query GUID</span></span>  | <span data-ttu-id="984c6-108">**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**</span><span class="sxs-lookup"><span data-stu-id="984c6-108">**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**</span></span>                                                                         |
| <span data-ttu-id="984c6-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="984c6-109">Input data</span></span>  | [<span data-ttu-id="984c6-110">**\_Entrée D3DAUTHENTICATEDCHANNEL QUERYOUTPUTIDCOUNT \_**</span><span class="sxs-lookup"><span data-stu-id="984c6-110">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_INPUT**</span></span>](d3dauthenticatedchannel-queryoutputidcount-input.md)   |
| <span data-ttu-id="984c6-111">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="984c6-111">Return data</span></span> | [<span data-ttu-id="984c6-112">**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_**</span><span class="sxs-lookup"><span data-stu-id="984c6-112">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryoutputidcount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="984c6-113">Notes</span><span class="sxs-lookup"><span data-stu-id="984c6-113">Remarks</span></span>

<span data-ttu-id="984c6-114">Les types de canaux suivants prennent en charge cette requête :</span><span class="sxs-lookup"><span data-stu-id="984c6-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="984c6-115">**\_Matériel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="984c6-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="984c6-116">**\_Logiciel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="984c6-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="984c6-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="984c6-117">Requirements</span></span>



| <span data-ttu-id="984c6-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="984c6-118">Requirement</span></span> | <span data-ttu-id="984c6-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="984c6-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="984c6-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="984c6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="984c6-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="984c6-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="984c6-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="984c6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="984c6-123">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="984c6-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="984c6-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="984c6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="984c6-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="984c6-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="984c6-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="984c6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="984c6-127">Requêtes protection du contenu</span><span class="sxs-lookup"><span data-stu-id="984c6-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="984c6-128">protection du contenu basé sur GPU</span><span class="sxs-lookup"><span data-stu-id="984c6-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="984c6-129">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="984c6-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




