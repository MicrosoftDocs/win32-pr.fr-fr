---
description: Retourne l’un des identificateurs de sortie qui est associé à une session de chiffrement et un périphérique Direct3D spécifiés.
ms.assetid: 7b56055a-fb36-4e54-9bee-ab9401b09267
title: D3DAUTHENTICATEDQUERY_OUTPUTID (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: fa970ae6e7b10f553679376d7a924d1c8b67c595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749293"
---
# <a name="d3dauthenticatedquery_outputid"></a><span data-ttu-id="b8c15-103">D3DAUTHENTICATEDQUERY \_ OUTPUTID</span><span class="sxs-lookup"><span data-stu-id="b8c15-103">D3DAUTHENTICATEDQUERY\_OUTPUTID</span></span>

<span data-ttu-id="b8c15-104">Retourne l’un des identificateurs de sortie qui est associé à une session de chiffrement et un périphérique Direct3D spécifiés.</span><span class="sxs-lookup"><span data-stu-id="b8c15-104">Returns one of the output identifiers that is associated with a specified cryptographic session and Direct3D device.</span></span>



| <span data-ttu-id="b8c15-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8c15-105">Requirement</span></span> | <span data-ttu-id="b8c15-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8c15-106">Value</span></span> |
|-------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8c15-107">GUID de la requête</span><span class="sxs-lookup"><span data-stu-id="b8c15-107">Query GUID</span></span>  | <span data-ttu-id="b8c15-108">**D3DAUTHENTICATEDQUERY \_ OUTPUTID**</span><span class="sxs-lookup"><span data-stu-id="b8c15-108">**D3DAUTHENTICATEDQUERY\_OUTPUTID**</span></span>                                                                    |
| <span data-ttu-id="b8c15-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="b8c15-109">Input data</span></span>  | [<span data-ttu-id="b8c15-110">**\_Entrée D3DAUTHENTICATEDCHANNEL QUERYOUTPUTID \_**</span><span class="sxs-lookup"><span data-stu-id="b8c15-110">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_INPUT**</span></span>](d3dauthenticatedchannel-queryoutputid-input.md)   |
| <span data-ttu-id="b8c15-111">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="b8c15-111">Return data</span></span> | [<span data-ttu-id="b8c15-112">**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTID \_**</span><span class="sxs-lookup"><span data-stu-id="b8c15-112">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryoutputid-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="b8c15-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b8c15-113">Remarks</span></span>

<span data-ttu-id="b8c15-114">Les types de canaux suivants prennent en charge cette requête :</span><span class="sxs-lookup"><span data-stu-id="b8c15-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="b8c15-115">**\_Matériel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="b8c15-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="b8c15-116">**\_Logiciel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="b8c15-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="b8c15-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8c15-117">Requirements</span></span>



| <span data-ttu-id="b8c15-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8c15-118">Requirement</span></span> | <span data-ttu-id="b8c15-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8c15-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8c15-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8c15-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b8c15-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8c15-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b8c15-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8c15-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b8c15-123">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8c15-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b8c15-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8c15-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8c15-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8c15-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8c15-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8c15-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8c15-127">Requêtes protection du contenu</span><span class="sxs-lookup"><span data-stu-id="b8c15-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="b8c15-128">protection du contenu basé sur GPU</span><span class="sxs-lookup"><span data-stu-id="b8c15-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="b8c15-129">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="b8c15-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




