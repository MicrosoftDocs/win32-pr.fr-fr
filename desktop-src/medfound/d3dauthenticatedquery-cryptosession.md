---
description: Retourne les descripteurs de la session de chiffrement et du périphérique Direct3D associés à un périphérique de décodage DirectX Video Acceleration 2 (DXVA-2) spécifié.
ms.assetid: 90b3bcf3-2988-48de-8acd-62e385d4fdf0
title: D3DAUTHENTICATEDQUERY_CRYPTOSESSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: e824514c3fef4e3e036b8f2973d3a958c4e135ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201158"
---
# <a name="d3dauthenticatedquery_cryptosession"></a><span data-ttu-id="d1599-103">D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION</span><span class="sxs-lookup"><span data-stu-id="d1599-103">D3DAUTHENTICATEDQUERY\_CRYPTOSESSION</span></span>

<span data-ttu-id="d1599-104">Retourne les descripteurs de la session de chiffrement et du périphérique Direct3D associés à un périphérique de décodage DirectX Video Acceleration 2 (DXVA-2) spécifié.</span><span class="sxs-lookup"><span data-stu-id="d1599-104">Returns handles to the cryptographic session and Direct3D device that are associated with a specified DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>



| <span data-ttu-id="d1599-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1599-105">Requirement</span></span> | <span data-ttu-id="d1599-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1599-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1599-107">GUID de la requête</span><span class="sxs-lookup"><span data-stu-id="d1599-107">Query GUID</span></span>  | <span data-ttu-id="d1599-108">**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**</span><span class="sxs-lookup"><span data-stu-id="d1599-108">**D3DAUTHENTICATEDQUERY\_CRYPTOSESSION**</span></span>                                                                         |
| <span data-ttu-id="d1599-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="d1599-109">Input data</span></span>  | [<span data-ttu-id="d1599-110">**\_Entrée de requête D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="d1599-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                             |
| <span data-ttu-id="d1599-111">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="d1599-111">Return data</span></span> | [<span data-ttu-id="d1599-112">**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYCRYPTOSESSION \_**</span><span class="sxs-lookup"><span data-stu-id="d1599-112">**D3DAUTHENTICATEDCHANNEL\_QUERYCRYPTOSESSION\_OUTPUT**</span></span>](d3dauthenticatedchannel-querycryptosession-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="d1599-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d1599-113">Remarks</span></span>

<span data-ttu-id="d1599-114">Les types de canaux suivants prennent en charge cette requête :</span><span class="sxs-lookup"><span data-stu-id="d1599-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="d1599-115">**\_Matériel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="d1599-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="d1599-116">**\_Logiciel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="d1599-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="d1599-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1599-117">Requirements</span></span>



| <span data-ttu-id="d1599-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1599-118">Requirement</span></span> | <span data-ttu-id="d1599-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1599-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1599-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1599-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d1599-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1599-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d1599-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1599-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d1599-123">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1599-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d1599-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1599-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1599-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1599-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1599-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1599-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1599-127">Requêtes protection du contenu</span><span class="sxs-lookup"><span data-stu-id="d1599-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="d1599-128">protection du contenu basé sur GPU</span><span class="sxs-lookup"><span data-stu-id="d1599-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="d1599-129">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="d1599-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




