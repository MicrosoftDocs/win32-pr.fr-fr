---
description: Spécifie que la source du média sera créée dans un processus distant.
ms.assetid: 3a2f9ff5-1780-40f3-b36b-3a7cccb47d05
title: Attribut MF_SESSION_REMOTE_SOURCE_MODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a27b26a71e8bea53ab687eaf6126a1803e71ba16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203863"
---
# <a name="mf_session_remote_source_mode-attribute"></a><span data-ttu-id="68bf4-103">\_Attribut de \_ \_ mode Source distant de session MF \_</span><span class="sxs-lookup"><span data-stu-id="68bf4-103">MF\_SESSION\_REMOTE\_SOURCE\_MODE attribute</span></span>

<span data-ttu-id="68bf4-104">Spécifie que la source du média sera créée dans un processus distant.</span><span class="sxs-lookup"><span data-stu-id="68bf4-104">Specifies that the media source will be created in a remote process.</span></span>

## <a name="data-type"></a><span data-ttu-id="68bf4-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="68bf4-105">Data type</span></span>

<span data-ttu-id="68bf4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="68bf4-106">**UINT32**</span></span>

<span data-ttu-id="68bf4-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="68bf4-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68bf4-108">Notes</span><span class="sxs-lookup"><span data-stu-id="68bf4-108">Remarks</span></span>

<span data-ttu-id="68bf4-109">Vous pouvez définir cet attribut sur la session PMP (Protected Media Path) à l’aide du paramètre *pConfiguration* de la fonction [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="68bf4-109">You can set this attribute on the protected media path (PMP) session by using the *pConfiguration* parameter of the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="68bf4-110">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="68bf4-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="68bf4-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68bf4-111">Requirements</span></span>



| <span data-ttu-id="68bf4-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68bf4-112">Requirement</span></span> | <span data-ttu-id="68bf4-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="68bf4-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68bf4-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68bf4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="68bf4-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68bf4-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="68bf4-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68bf4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="68bf4-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68bf4-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="68bf4-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="68bf4-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="68bf4-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="68bf4-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68bf4-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68bf4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68bf4-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="68bf4-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="68bf4-122">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="68bf4-122">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="68bf4-123">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="68bf4-123">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="68bf4-124">Attributs de session multimédia</span><span class="sxs-lookup"><span data-stu-id="68bf4-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="68bf4-125">Session média PMP</span><span class="sxs-lookup"><span data-stu-id="68bf4-125">PMP Media Session</span></span>](pmp-media-session.md)
</dt> </dl>

 

 




