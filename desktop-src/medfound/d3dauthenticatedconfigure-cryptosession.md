---
description: Associe une session de chiffrement à un appareil de décodage de DirectX Video Acceleration 2 (DXVA-2) et à un appareil Direct3D.
ms.assetid: d40fead7-8a86-426e-933e-13df21cdf50b
title: D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 4b6fda19aef9629214aaa410fd43c4d64f16dd29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516404"
---
# <a name="d3dauthenticatedconfigure_cryptosession"></a><span data-ttu-id="f9c43-103">D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION</span><span class="sxs-lookup"><span data-stu-id="f9c43-103">D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION</span></span>

<span data-ttu-id="f9c43-104">Associe une session de chiffrement à un appareil de décodage de DirectX Video Acceleration 2 (DXVA-2) et à un appareil Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f9c43-104">Associates a cryptographic session with a DirectX Video Acceleration 2 (DXVA-2) decoder device and a Direct3D device.</span></span>



| <span data-ttu-id="f9c43-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9c43-105">Requirement</span></span> | <span data-ttu-id="f9c43-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9c43-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c43-107">GUID de la commande</span><span class="sxs-lookup"><span data-stu-id="f9c43-107">Command GUID</span></span> | <span data-ttu-id="f9c43-108">**D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**</span><span class="sxs-lookup"><span data-stu-id="f9c43-108">**D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION**</span></span>                                                              |
| <span data-ttu-id="f9c43-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="f9c43-109">Input data</span></span>   | [<span data-ttu-id="f9c43-110">**D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION**</span><span class="sxs-lookup"><span data-stu-id="f9c43-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGURECRYPTOSESSION**</span></span>](d3dauthenticatedchannel-configurecryptosession.md) |



 

## <a name="remarks"></a><span data-ttu-id="f9c43-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f9c43-111">Remarks</span></span>

<span data-ttu-id="f9c43-112">Une fois cette commande envoyée, vous pouvez envoyer la requête [D3DAUTHENTICATEDQUERY \_ OUTPUTID](d3dauthenticatedquery-outputid.md) pour savoir quelles sorties vidéo sont associées à la session de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="f9c43-112">After this command is sent, you can send the [D3DAUTHENTICATEDQUERY\_OUTPUTID](d3dauthenticatedquery-outputid.md) query to find out which video outputs are associated with the cryptographic session.</span></span>

<span data-ttu-id="f9c43-113">Les types de canaux suivants prennent en charge cette commande :</span><span class="sxs-lookup"><span data-stu-id="f9c43-113">The following channel types support this command:</span></span>

-   <span data-ttu-id="f9c43-114">**D3DAUTHENTICATEDCHANNEL \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="f9c43-114">**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
-   <span data-ttu-id="f9c43-115">**\_Logiciel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="f9c43-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="f9c43-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9c43-116">Requirements</span></span>



| <span data-ttu-id="f9c43-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9c43-117">Requirement</span></span> | <span data-ttu-id="f9c43-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9c43-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c43-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9c43-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f9c43-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9c43-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f9c43-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9c43-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f9c43-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9c43-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f9c43-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9c43-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9c43-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9c43-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9c43-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9c43-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9c43-126">Commandes protection du contenu</span><span class="sxs-lookup"><span data-stu-id="f9c43-126">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="f9c43-127">protection du contenu basé sur GPU</span><span class="sxs-lookup"><span data-stu-id="f9c43-127">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="f9c43-128">**IDirect3DAuthenticatedChannel9 :: configure**</span><span class="sxs-lookup"><span data-stu-id="f9c43-128">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




