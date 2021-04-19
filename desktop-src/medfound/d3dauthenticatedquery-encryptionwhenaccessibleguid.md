---
description: Retourne l’un des types de chiffrement qui peuvent être utilisés pour chiffrer le contenu avant qu’il ne soit accessible au processeur ou au bus.
ms.assetid: 263c6f00-8bc9-4e9c-8b98-fb8f87c6c008
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b5755a2707ec9d7440cda9b4692eed36ac6deff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514765"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguid"></a><span data-ttu-id="eeae3-103">D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID</span><span class="sxs-lookup"><span data-stu-id="eeae3-103">D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID</span></span>

<span data-ttu-id="eeae3-104">Retourne l’un des types de chiffrement qui peuvent être utilisés pour chiffrer le contenu avant qu’il ne soit accessible au processeur ou au bus.</span><span class="sxs-lookup"><span data-stu-id="eeae3-104">Returns one of the encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="eeae3-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eeae3-105">Requirement</span></span> | <span data-ttu-id="eeae3-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="eeae3-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeae3-107">GUID de la requête</span><span class="sxs-lookup"><span data-stu-id="eeae3-107">Query GUID</span></span>  | <span data-ttu-id="eeae3-108">**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**</span><span class="sxs-lookup"><span data-stu-id="eeae3-108">**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**</span></span>                                                                            |
| <span data-ttu-id="eeae3-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="eeae3-109">Input data</span></span>  | [<span data-ttu-id="eeae3-110">**\_Entrée D3DAUTHENTICATEDCHANNEL QUERYEVICTIONENCRYPTIONGUID \_**</span><span class="sxs-lookup"><span data-stu-id="eeae3-110">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_INPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)   |
| <span data-ttu-id="eeae3-111">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="eeae3-111">Return data</span></span> | [<span data-ttu-id="eeae3-112">**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID \_**</span><span class="sxs-lookup"><span data-stu-id="eeae3-112">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguid-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="eeae3-113">Notes</span><span class="sxs-lookup"><span data-stu-id="eeae3-113">Remarks</span></span>

<span data-ttu-id="eeae3-114">Les types de canaux suivants prennent en charge cette requête :</span><span class="sxs-lookup"><span data-stu-id="eeae3-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="eeae3-115">**\_Matériel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="eeae3-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="eeae3-116">**\_Logiciel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="eeae3-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="eeae3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eeae3-117">Requirements</span></span>



| <span data-ttu-id="eeae3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eeae3-118">Requirement</span></span> | <span data-ttu-id="eeae3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="eeae3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eeae3-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eeae3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eeae3-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eeae3-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="eeae3-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eeae3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eeae3-123">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eeae3-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="eeae3-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="eeae3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeae3-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="eeae3-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeae3-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eeae3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeae3-127">Requêtes protection du contenu</span><span class="sxs-lookup"><span data-stu-id="eeae3-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="eeae3-128">protection du contenu basé sur GPU</span><span class="sxs-lookup"><span data-stu-id="eeae3-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="eeae3-129">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="eeae3-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




