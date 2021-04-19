---
description: GUID de type principal pour un type de média.
ms.assetid: b88b5fcf-8025-4638-930d-9fc5cf0ec8a3
title: Attribut MF_MT_MAJOR_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c4cc02df4f89e261605c91b71ac1c80ba38b9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515049"
---
# <a name="mf_mt_major_type-attribute"></a><span data-ttu-id="126ce-103">\_Attribut de \_ type de majeure-MF MT \_</span><span class="sxs-lookup"><span data-stu-id="126ce-103">MF\_MT\_MAJOR\_TYPE attribute</span></span>

<span data-ttu-id="126ce-104">GUID de type principal pour un type de média.</span><span class="sxs-lookup"><span data-stu-id="126ce-104">Major type GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="126ce-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="126ce-105">Data type</span></span>

<span data-ttu-id="126ce-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="126ce-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="126ce-107">Notes</span><span class="sxs-lookup"><span data-stu-id="126ce-107">Remarks</span></span>

<span data-ttu-id="126ce-108">Le type principal définit la catégorie globale des données multimédia.</span><span class="sxs-lookup"><span data-stu-id="126ce-108">The major type defines the overall category of the media data.</span></span> <span data-ttu-id="126ce-109">Les principaux types sont les suivants : vidéo, audio, script et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="126ce-109">Major types include video, audio, script, and so forth.</span></span> <span data-ttu-id="126ce-110">Pour obtenir la liste des valeurs possibles, consultez [types de média majeurs](media-type-guids.md).</span><span class="sxs-lookup"><span data-stu-id="126ce-110">For a list of possible values, see [Major Media Types](media-type-guids.md).</span></span>

<span data-ttu-id="126ce-111">Une autre façon de récupérer cet attribut consiste à appeler [**IMFMediaType :: GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype).</span><span class="sxs-lookup"><span data-stu-id="126ce-111">An alternate way to retrieve this attribute is to call [**IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype).</span></span>

<span data-ttu-id="126ce-112">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="126ce-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="126ce-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="126ce-113">Requirements</span></span>



| <span data-ttu-id="126ce-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="126ce-114">Requirement</span></span> | <span data-ttu-id="126ce-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="126ce-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="126ce-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="126ce-116">Minimum supported client</span></span><br/> | <span data-ttu-id="126ce-117">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="126ce-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="126ce-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="126ce-118">Minimum supported server</span></span><br/> | <span data-ttu-id="126ce-119">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="126ce-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="126ce-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="126ce-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="126ce-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="126ce-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="126ce-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="126ce-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="126ce-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="126ce-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="126ce-124">**IMFAttributes :: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="126ce-124">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="126ce-125">**IMFAttributes :: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="126ce-125">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="126ce-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="126ce-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="126ce-127">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="126ce-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




