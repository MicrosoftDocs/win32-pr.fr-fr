---
description: Contient des indicateurs qui définissent les fonctionnalités de la session multimédia, en fonction de la présentation actuelle.
ms.assetid: a78a3f3f-4ba1-41f3-b808-43f1e4975bb9
title: Attribut MF_EVENT_SESSIONCAPS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af38d61f07bf038d1906d6f11e46fea63e800efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517759"
---
# <a name="mf_event_sessioncaps-attribute"></a><span data-ttu-id="d0a8a-103">\_ \_ Attribut SESSIONCAPS de l’événement MF</span><span class="sxs-lookup"><span data-stu-id="d0a8a-103">MF\_EVENT\_SESSIONCAPS attribute</span></span>

<span data-ttu-id="d0a8a-104">Contient des indicateurs qui définissent les fonctionnalités de la session multimédia, en fonction de la présentation actuelle.</span><span class="sxs-lookup"><span data-stu-id="d0a8a-104">Contains flags that define the capabilities of the Media Session, based on the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="d0a8a-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="d0a8a-105">Data type</span></span>

<span data-ttu-id="d0a8a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d0a8a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d0a8a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d0a8a-107">Remarks</span></span>

<span data-ttu-id="d0a8a-108">Cet attribut contient une opération **de bits or** de zéro, un ou plusieurs indicateurs.</span><span class="sxs-lookup"><span data-stu-id="d0a8a-108">This attribute contains a bitwise **OR** of zero or more flags.</span></span> <span data-ttu-id="d0a8a-109">Pour obtenir la liste des indicateurs possibles, consultez [**IMFMediaSession :: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span><span class="sxs-lookup"><span data-stu-id="d0a8a-109">For a list of possible flags, see [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span></span>

<span data-ttu-id="d0a8a-110">Cet attribut est utilisé avec l’événement [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="d0a8a-110">This attribute is used with the [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) event.</span></span>

<span data-ttu-id="d0a8a-111">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d0a8a-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0a8a-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0a8a-112">Requirements</span></span>



| <span data-ttu-id="d0a8a-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0a8a-113">Requirement</span></span> | <span data-ttu-id="d0a8a-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0a8a-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d0a8a-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0a8a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d0a8a-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0a8a-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d0a8a-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0a8a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d0a8a-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0a8a-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d0a8a-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0a8a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0a8a-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0a8a-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0a8a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0a8a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0a8a-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d0a8a-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d0a8a-123">Attributs d'événement</span><span class="sxs-lookup"><span data-stu-id="d0a8a-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="d0a8a-124">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d0a8a-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="d0a8a-125">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d0a8a-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




