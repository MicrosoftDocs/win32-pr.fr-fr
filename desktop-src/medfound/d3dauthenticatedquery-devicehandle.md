---
description: Retourne un handle vers l’appareil associé à ce canal authentifié.
ms.assetid: 948eac1a-640a-47fd-b538-1de3ea5d8f0b
title: D3DAUTHENTICATEDQUERY_DEVICEHANDLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_DEVICEHANDLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a3ebf54530a4ae029a52632eb5bb5afc51b5f152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516806"
---
# <a name="d3dauthenticatedquery_devicehandle"></a><span data-ttu-id="57e46-103">D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE</span><span class="sxs-lookup"><span data-stu-id="57e46-103">D3DAUTHENTICATEDQUERY\_DEVICEHANDLE</span></span>

<span data-ttu-id="57e46-104">Retourne un handle vers l’appareil associé à ce canal authentifié.</span><span class="sxs-lookup"><span data-stu-id="57e46-104">Returns a handle to the device that is associated with this authenticated channel.</span></span> <span data-ttu-id="57e46-105">Vous pouvez utiliser ce handle pour vérifier si deux canaux authentifiés communiquent avec le même appareil.</span><span class="sxs-lookup"><span data-stu-id="57e46-105">You can use this handle to verify whether two authenticated channels are communicating with the same device.</span></span>



| <span data-ttu-id="57e46-106">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57e46-106">Requirement</span></span> | <span data-ttu-id="57e46-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="57e46-107">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57e46-108">GUID de la requête</span><span class="sxs-lookup"><span data-stu-id="57e46-108">Query GUID</span></span>  | <span data-ttu-id="57e46-109">**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**</span><span class="sxs-lookup"><span data-stu-id="57e46-109">**D3DAUTHENTICATEDQUERY\_DEVICEHANDLE**</span></span>                                                                        |
| <span data-ttu-id="57e46-110">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="57e46-110">Input data</span></span>  | [<span data-ttu-id="57e46-111">**\_Entrée de requête D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="57e46-111">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                           |
| <span data-ttu-id="57e46-112">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="57e46-112">Return data</span></span> | [<span data-ttu-id="57e46-113">**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYDEVICEHANDLE \_**</span><span class="sxs-lookup"><span data-stu-id="57e46-113">**D3DAUTHENTICATEDCHANNEL\_QUERYDEVICEHANDLE\_OUTPUT**</span></span>](d3dauthenticatedchannel-querydevicehandle-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="57e46-114">Notes</span><span class="sxs-lookup"><span data-stu-id="57e46-114">Remarks</span></span>

<span data-ttu-id="57e46-115">Cette requête est valide pour tous les types de canaux.</span><span class="sxs-lookup"><span data-stu-id="57e46-115">This query is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="57e46-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57e46-116">Requirements</span></span>



| <span data-ttu-id="57e46-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57e46-117">Requirement</span></span> | <span data-ttu-id="57e46-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="57e46-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57e46-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57e46-119">Minimum supported client</span></span><br/> | <span data-ttu-id="57e46-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57e46-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="57e46-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57e46-121">Minimum supported server</span></span><br/> | <span data-ttu-id="57e46-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57e46-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="57e46-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="57e46-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="57e46-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="57e46-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57e46-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57e46-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57e46-126">Requêtes protection du contenu</span><span class="sxs-lookup"><span data-stu-id="57e46-126">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="57e46-127">protection du contenu basé sur GPU</span><span class="sxs-lookup"><span data-stu-id="57e46-127">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="57e46-128">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="57e46-128">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




