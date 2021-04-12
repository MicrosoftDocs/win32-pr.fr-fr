---
description: Permet à un processus d’ouvrir une ressource partagée ou désactive l’ouverture de ressources partagées par un processus.
ms.assetid: 5fa2b88f-e946-436c-953e-04e0e338146c
title: D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7404a4bed3ac3b1d4002bb03c45d7732500b77e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201160"
---
# <a name="d3dauthenticatedconfigure_sharedresource"></a><span data-ttu-id="428ab-103">D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE</span><span class="sxs-lookup"><span data-stu-id="428ab-103">D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE</span></span>

<span data-ttu-id="428ab-104">Permet à un processus d’ouvrir une ressource partagée ou désactive l’ouverture de ressources partagées par un processus.</span><span class="sxs-lookup"><span data-stu-id="428ab-104">Enables a process to open a shared resource, or disables a process from opening shared resources.</span></span>



| <span data-ttu-id="428ab-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="428ab-105">Requirement</span></span> | <span data-ttu-id="428ab-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="428ab-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="428ab-107">GUID de la commande</span><span class="sxs-lookup"><span data-stu-id="428ab-107">Command GUID</span></span> | <span data-ttu-id="428ab-108">**D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="428ab-108">**D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE**</span></span>                                                               |
| <span data-ttu-id="428ab-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="428ab-109">Input data</span></span>   | [<span data-ttu-id="428ab-110">**D3DAUTHENTICATEDCHANNEL \_ CONFIGURESHAREDRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="428ab-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGURESHAREDRESOURCE**</span></span>](d3dauthenticatedchannel-configuresharedresource.md) |



 

## <a name="remarks"></a><span data-ttu-id="428ab-111">Notes</span><span class="sxs-lookup"><span data-stu-id="428ab-111">Remarks</span></span>

<span data-ttu-id="428ab-112">Les types de canaux suivants prennent en charge cette requête :</span><span class="sxs-lookup"><span data-stu-id="428ab-112">The following channel types support this query:</span></span>

-   <span data-ttu-id="428ab-113">**D3DAUTHENTICATEDCHANNEL de \_ pilote \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="428ab-113">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_D3D9**</span></span>
-   <span data-ttu-id="428ab-114">**\_Logiciel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="428ab-114">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="428ab-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="428ab-115">Requirements</span></span>



| <span data-ttu-id="428ab-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="428ab-116">Requirement</span></span> | <span data-ttu-id="428ab-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="428ab-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="428ab-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="428ab-118">Minimum supported client</span></span><br/> | <span data-ttu-id="428ab-119">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="428ab-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="428ab-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="428ab-120">Minimum supported server</span></span><br/> | <span data-ttu-id="428ab-121">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="428ab-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="428ab-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="428ab-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="428ab-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="428ab-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="428ab-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="428ab-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="428ab-125">Commandes protection du contenu</span><span class="sxs-lookup"><span data-stu-id="428ab-125">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="428ab-126">protection du contenu basé sur GPU</span><span class="sxs-lookup"><span data-stu-id="428ab-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="428ab-127">**IDirect3DAuthenticatedChannel9 :: configure**</span><span class="sxs-lookup"><span data-stu-id="428ab-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




