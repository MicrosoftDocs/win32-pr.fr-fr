---
description: Spécifie à quel moment une présentation a été modifiée pour la dernière fois.
ms.assetid: 12990de2-7656-4781-943b-c46f42a0e38d
title: Attribut MF_PD_LAST_MODIFIED_TIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f97bf47cff32834b694f36cbd4c9062e06f2d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952339"
---
# <a name="mf_pd_last_modified_time-attribute"></a><span data-ttu-id="ae854-103">\_Attribut heure de la \_ dernière \_ modification MF PD \_</span><span class="sxs-lookup"><span data-stu-id="ae854-103">MF\_PD\_LAST\_MODIFIED\_TIME attribute</span></span>

<span data-ttu-id="ae854-104">Spécifie à quel moment une présentation a été modifiée pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="ae854-104">Specifies when a presentation was last modified.</span></span>

## <a name="data-type"></a><span data-ttu-id="ae854-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ae854-105">Data type</span></span>

<span data-ttu-id="ae854-106">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="ae854-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="ae854-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ae854-107">Remarks</span></span>

<span data-ttu-id="ae854-108">Les sources multimédias peuvent définir cet attribut sur un descripteur de présentation.</span><span class="sxs-lookup"><span data-stu-id="ae854-108">Media sources can set this attribute on a presentation descriptor.</span></span> <span data-ttu-id="ae854-109">La valeur de l’attribut est une structure **fileTime** , qui est documentée dans la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="ae854-109">The value of the attribute is a **FILETIME** structure, which is documented in the Windows SDK.</span></span>

<span data-ttu-id="ae854-110">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ae854-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae854-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae854-111">Requirements</span></span>



| <span data-ttu-id="ae854-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae854-112">Requirement</span></span> | <span data-ttu-id="ae854-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae854-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ae854-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae854-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ae854-115">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="ae854-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ae854-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae854-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ae854-117">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="ae854-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ae854-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae854-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae854-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae854-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae854-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae854-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae854-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ae854-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ae854-122">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="ae854-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="ae854-123">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="ae854-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="ae854-124">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ae854-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="ae854-125">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="ae854-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




