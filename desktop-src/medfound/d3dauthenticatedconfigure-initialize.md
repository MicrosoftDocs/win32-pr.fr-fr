---
description: Initialise le canal authentifié.
ms.assetid: a74edbaa-af57-4f8e-9974-f6053f59377f
title: D3DAUTHENTICATEDCONFIGURE_INITIALIZE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_INITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2cd3238b7a7eea27356ce76ec9c83bf8aea4d7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106541180"
---
# <a name="d3dauthenticatedconfigure_initialize"></a><span data-ttu-id="05976-103">Initialisation de D3DAUTHENTICATEDCONFIGURE \_</span><span class="sxs-lookup"><span data-stu-id="05976-103">D3DAUTHENTICATEDCONFIGURE\_INITIALIZE</span></span>

<span data-ttu-id="05976-104">Initialise le canal authentifié.</span><span class="sxs-lookup"><span data-stu-id="05976-104">Initializes the authenticated channel.</span></span>



| <span data-ttu-id="05976-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05976-105">Requirement</span></span> | <span data-ttu-id="05976-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="05976-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05976-107">GUID de la commande</span><span class="sxs-lookup"><span data-stu-id="05976-107">Command GUID</span></span> | <span data-ttu-id="05976-108">**Initialisation de D3DAUTHENTICATEDCONFIGURE \_**</span><span class="sxs-lookup"><span data-stu-id="05976-108">**D3DAUTHENTICATEDCONFIGURE\_INITIALIZE**</span></span>                                                           |
| <span data-ttu-id="05976-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="05976-109">Input data</span></span>   | [<span data-ttu-id="05976-110">**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREINITIALIZE**</span><span class="sxs-lookup"><span data-stu-id="05976-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGUREINITIALIZE**</span></span>](d3dauthenticatedchannel-configureinitialize.md) |



 

## <a name="remarks"></a><span data-ttu-id="05976-111">Notes</span><span class="sxs-lookup"><span data-stu-id="05976-111">Remarks</span></span>

<span data-ttu-id="05976-112">Envoyez cette commande une seule fois, au début de la session.</span><span class="sxs-lookup"><span data-stu-id="05976-112">Send this command once, at the start of the session.</span></span> <span data-ttu-id="05976-113">Cette commande ne peut être envoyée qu’une seule fois pour chaque canal authentifié.</span><span class="sxs-lookup"><span data-stu-id="05976-113">This command can be sent only one time for each authenticated channel.</span></span> <span data-ttu-id="05976-114">Le numéro de séquence d’entrée est ignoré pour cette commande.</span><span class="sxs-lookup"><span data-stu-id="05976-114">The input sequence number is ignored for this command.</span></span>

<span data-ttu-id="05976-115">Les types de canaux suivants prennent en charge cette commande :</span><span class="sxs-lookup"><span data-stu-id="05976-115">The following channel types support this command:</span></span>

-   <span data-ttu-id="05976-116">**\_Matériel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="05976-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="05976-117">**\_Logiciel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="05976-117">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="05976-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05976-118">Requirements</span></span>



| <span data-ttu-id="05976-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05976-119">Requirement</span></span> | <span data-ttu-id="05976-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="05976-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05976-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05976-121">Minimum supported client</span></span><br/> | <span data-ttu-id="05976-122">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05976-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="05976-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05976-123">Minimum supported server</span></span><br/> | <span data-ttu-id="05976-124">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05976-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="05976-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="05976-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="05976-126"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="05976-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05976-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05976-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05976-128">Commandes protection du contenu</span><span class="sxs-lookup"><span data-stu-id="05976-128">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="05976-129">protection du contenu basé sur GPU</span><span class="sxs-lookup"><span data-stu-id="05976-129">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="05976-130">**IDirect3DAuthenticatedChannel9 :: configure**</span><span class="sxs-lookup"><span data-stu-id="05976-130">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




