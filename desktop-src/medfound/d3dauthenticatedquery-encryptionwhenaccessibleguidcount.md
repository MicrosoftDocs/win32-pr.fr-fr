---
description: Retourne le nombre de types de chiffrement qui peuvent être utilisés pour chiffrer le contenu avant qu’il ne soit accessible au processeur ou au bus.
ms.assetid: 442b80f5-8467-427d-a01e-5d22f6ddafea
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9cd281836436c1d11fe07f7a43ecceebc8e3b12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749300"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguidcount"></a><span data-ttu-id="30bdc-103">D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT</span><span class="sxs-lookup"><span data-stu-id="30bdc-103">D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT</span></span>

<span data-ttu-id="30bdc-104">Retourne le nombre de types de chiffrement qui peuvent être utilisés pour chiffrer le contenu avant qu’il ne soit accessible au processeur ou au bus.</span><span class="sxs-lookup"><span data-stu-id="30bdc-104">Returns the number of encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="30bdc-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30bdc-105">Requirement</span></span> | <span data-ttu-id="30bdc-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="30bdc-106">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30bdc-107">GUID de la requête</span><span class="sxs-lookup"><span data-stu-id="30bdc-107">Query GUID</span></span>  | <span data-ttu-id="30bdc-108">**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**</span><span class="sxs-lookup"><span data-stu-id="30bdc-108">**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**</span></span>                                                                                 |
| <span data-ttu-id="30bdc-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="30bdc-109">Input data</span></span>  | [<span data-ttu-id="30bdc-110">**\_Entrée de requête D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="30bdc-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                         |
| <span data-ttu-id="30bdc-111">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="30bdc-111">Return data</span></span> | [<span data-ttu-id="30bdc-112">**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUIDCOUNT \_**</span><span class="sxs-lookup"><span data-stu-id="30bdc-112">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUIDCOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="30bdc-113">Notes</span><span class="sxs-lookup"><span data-stu-id="30bdc-113">Remarks</span></span>

<span data-ttu-id="30bdc-114">Les types de canaux suivants prennent en charge cette requête :</span><span class="sxs-lookup"><span data-stu-id="30bdc-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="30bdc-115">**\_Matériel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="30bdc-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="30bdc-116">**\_Logiciel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="30bdc-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="30bdc-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30bdc-117">Requirements</span></span>



| <span data-ttu-id="30bdc-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30bdc-118">Requirement</span></span> | <span data-ttu-id="30bdc-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="30bdc-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30bdc-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30bdc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="30bdc-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30bdc-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="30bdc-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30bdc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="30bdc-123">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30bdc-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="30bdc-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="30bdc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="30bdc-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="30bdc-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30bdc-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30bdc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30bdc-127">Requêtes protection du contenu</span><span class="sxs-lookup"><span data-stu-id="30bdc-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="30bdc-128">protection du contenu basé sur GPU</span><span class="sxs-lookup"><span data-stu-id="30bdc-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="30bdc-129">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="30bdc-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




