---
description: Permet à deux instances de la session multimédia de partager le même processus PMP (Protected Media Path).
ms.assetid: a922c79b-d6c1-447d-b6fa-993970169a3f
title: Attribut MF_SESSION_SERVER_CONTEXT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ce68d1dcd4318f68c4547845e6ce12d2f3aaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115842"
---
# <a name="mf_session_server_context-attribute"></a><span data-ttu-id="87fec-103">\_Attribut de \_ contexte de serveur de session MF \_</span><span class="sxs-lookup"><span data-stu-id="87fec-103">MF\_SESSION\_SERVER\_CONTEXT attribute</span></span>

<span data-ttu-id="87fec-104">Permet à deux instances de la session multimédia de partager le même processus PMP (Protected Media Path).</span><span class="sxs-lookup"><span data-stu-id="87fec-104">Enables two instances of the Media Session to share the same Protected Media Path (PMP) process.</span></span>

## <a name="data-type"></a><span data-ttu-id="87fec-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="87fec-105">Data type</span></span>

<span data-ttu-id="87fec-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="87fec-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="87fec-107">Notes</span><span class="sxs-lookup"><span data-stu-id="87fec-107">Remarks</span></span>

<span data-ttu-id="87fec-108">Utilisez cet attribut si vous souhaitez créer la session de média PMP dans un processus PMP existant.</span><span class="sxs-lookup"><span data-stu-id="87fec-108">Use this attribute if you want to create the PMP Media Session in an existing PMP process.</span></span> <span data-ttu-id="87fec-109">La valeur de l’attribut est un pointeur vers l’interface [_ *IMFPMPServer* \*](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) .</span><span class="sxs-lookup"><span data-stu-id="87fec-109">The value of the attribute is a pointer to the [_ *IMFPMPServer*\*](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) interface.</span></span>

<span data-ttu-id="87fec-110">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="87fec-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="87fec-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87fec-111">Requirements</span></span>



| <span data-ttu-id="87fec-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87fec-112">Requirement</span></span> | <span data-ttu-id="87fec-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="87fec-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="87fec-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87fec-114">Minimum supported client</span></span><br/> | <span data-ttu-id="87fec-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87fec-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="87fec-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87fec-116">Minimum supported server</span></span><br/> | <span data-ttu-id="87fec-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87fec-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="87fec-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="87fec-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="87fec-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="87fec-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87fec-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87fec-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87fec-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="87fec-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="87fec-122">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="87fec-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="87fec-123">**IMFAttributes :: Setunknown,**</span><span class="sxs-lookup"><span data-stu-id="87fec-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="87fec-124">Attributs de session multimédia</span><span class="sxs-lookup"><span data-stu-id="87fec-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> </dl>

 

 




