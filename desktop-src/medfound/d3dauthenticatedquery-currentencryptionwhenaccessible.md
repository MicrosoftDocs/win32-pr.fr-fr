---
description: Retourne le type de chiffrement appliqué avant que le contenu soit accessible au processeur ou au bus.
ms.assetid: 89526bb2-1316-4730-b599-3690b1838c3e
title: D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a8b3374e6d50a50d32b60113318e5d1099083226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201159"
---
# <a name="d3dauthenticatedquery_currentencryptionwhenaccessible"></a><span data-ttu-id="bc77e-103">D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE</span><span class="sxs-lookup"><span data-stu-id="bc77e-103">D3DAUTHENTICATEDQUERY\_CURRENTENCRYPTIONWHENACCESSIBLE</span></span>

<span data-ttu-id="bc77e-104">Retourne le type de chiffrement appliqué avant que le contenu soit accessible au processeur ou au bus.</span><span class="sxs-lookup"><span data-stu-id="bc77e-104">Returns the encryption type that is applied before content becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="bc77e-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc77e-105">Requirement</span></span> | <span data-ttu-id="bc77e-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc77e-106">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc77e-107">GUID de la requête</span><span class="sxs-lookup"><span data-stu-id="bc77e-107">Query GUID</span></span>  | <span data-ttu-id="bc77e-108">**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**</span><span class="sxs-lookup"><span data-stu-id="bc77e-108">**D3DAUTHENTICATEDQUERY\_CURRENTENCRYPTIONWHENACCESSIBLE**</span></span>                                                                                   |
| <span data-ttu-id="bc77e-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="bc77e-109">Input data</span></span>  | [<span data-ttu-id="bc77e-110">**\_Entrée de requête D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="bc77e-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                         |
| <span data-ttu-id="bc77e-111">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="bc77e-111">Return data</span></span> | [<span data-ttu-id="bc77e-112">**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYUNCOMPRESSEDENCRYPTIONLEVEL \_**</span><span class="sxs-lookup"><span data-stu-id="bc77e-112">**D3DAUTHENTICATEDCHANNEL\_QUERYUNCOMPRESSEDENCRYPTIONLEVEL\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="bc77e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bc77e-113">Remarks</span></span>

<span data-ttu-id="bc77e-114">Les types de canaux suivants prennent en charge cette requête :</span><span class="sxs-lookup"><span data-stu-id="bc77e-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="bc77e-115">**\_Matériel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="bc77e-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="bc77e-116">**\_Logiciel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="bc77e-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="bc77e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc77e-117">Requirements</span></span>



| <span data-ttu-id="bc77e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc77e-118">Requirement</span></span> | <span data-ttu-id="bc77e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc77e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc77e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc77e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bc77e-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc77e-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bc77e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc77e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bc77e-123">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc77e-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bc77e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="bc77e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc77e-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc77e-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc77e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc77e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc77e-127">Requêtes protection du contenu</span><span class="sxs-lookup"><span data-stu-id="bc77e-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="bc77e-128">protection du contenu basé sur GPU</span><span class="sxs-lookup"><span data-stu-id="bc77e-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="bc77e-129">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="bc77e-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




