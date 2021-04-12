---
description: Contient le nom d’un flux.
ms.assetid: 80235820-761f-4deb-9bf6-82ef402b3ee4
title: Attribut MF_SD_STREAM_NAME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734c2d20390ba1a450a40c03054b4c67c5c0409a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320625"
---
# <a name="mf_sd_stream_name-attribute"></a><span data-ttu-id="3f1ff-103">\_Attribut de \_ nom de flux SD MF \_</span><span class="sxs-lookup"><span data-stu-id="3f1ff-103">MF\_SD\_STREAM\_NAME attribute</span></span>

<span data-ttu-id="3f1ff-104">Contient le nom d’un flux.</span><span class="sxs-lookup"><span data-stu-id="3f1ff-104">Contains the name of a stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="3f1ff-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="3f1ff-105">Data type</span></span>

<span data-ttu-id="3f1ff-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="3f1ff-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="3f1ff-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="3f1ff-107">Get/set</span></span>

<span data-ttu-id="3f1ff-108">Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="3f1ff-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="3f1ff-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="3f1ff-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="3f1ff-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="3f1ff-110">Applies to</span></span>

[<span data-ttu-id="3f1ff-111">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="3f1ff-111">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a><span data-ttu-id="3f1ff-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3f1ff-112">Remarks</span></span>

<span data-ttu-id="3f1ff-113">La source de média AVI définit cet attribut si le fichier AVI contient un segment « STRN ».</span><span class="sxs-lookup"><span data-stu-id="3f1ff-113">The AVI media source sets this attribute if the AVI file contains a 'strn' chunk.</span></span>

<span data-ttu-id="3f1ff-114">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3f1ff-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f1ff-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f1ff-115">Requirements</span></span>



| <span data-ttu-id="3f1ff-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f1ff-116">Requirement</span></span> | <span data-ttu-id="3f1ff-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f1ff-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3f1ff-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f1ff-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3f1ff-119">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3f1ff-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="3f1ff-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f1ff-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3f1ff-121">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3f1ff-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="3f1ff-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f1ff-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f1ff-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f1ff-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f1ff-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f1ff-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f1ff-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3f1ff-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3f1ff-126">Attributs du descripteur de flux</span><span class="sxs-lookup"><span data-stu-id="3f1ff-126">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




