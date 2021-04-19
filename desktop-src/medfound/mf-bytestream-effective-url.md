---
description: Obtient l’URL effective d’un flux d’octets.
ms.assetid: 0A83CFC0-7EAA-464B-BA39-50DF220AF683
title: Attribut MF_BYTESTREAM_EFFECTIVE_URL (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95e01238f04c30f72d55f940b3f3105863247ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533608"
---
# <a name="mf_bytestream_effective_url-attribute"></a><span data-ttu-id="bb4ff-103">\_Attribut d' \_ URL efficace BYTESTREAM \_ MF</span><span class="sxs-lookup"><span data-stu-id="bb4ff-103">MF\_BYTESTREAM\_EFFECTIVE\_URL attribute</span></span>

<span data-ttu-id="bb4ff-104">Obtient l’URL effective d’un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="bb4ff-104">Gets the effective URL of a byte stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="bb4ff-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="bb4ff-105">Data type</span></span>

## <a name="getset"></a><span data-ttu-id="bb4ff-106">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="bb4ff-106">Get/set</span></span>

<span data-ttu-id="bb4ff-107">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="bb4ff-107">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="bb4ff-108">Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="bb4ff-108">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="bb4ff-109">S’applique à</span><span class="sxs-lookup"><span data-stu-id="bb4ff-109">Applies to</span></span>

[<span data-ttu-id="bb4ff-110">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="bb4ff-110">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a><span data-ttu-id="bb4ff-111">Notes</span><span class="sxs-lookup"><span data-stu-id="bb4ff-111">Remarks</span></span>

<span data-ttu-id="bb4ff-112">L’URL effective peut être différente de l’URL d’origine si l’URL d’origine contient des informations supplémentaires, telles que des chaînes ou des ancres de recherche, ou si la demande a été redirigée.</span><span class="sxs-lookup"><span data-stu-id="bb4ff-112">The effective URL can differ from the original URL if the original URL contains any extra information, such as search strings or anchors, or if the request was redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb4ff-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb4ff-113">Requirements</span></span>



| <span data-ttu-id="bb4ff-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb4ff-114">Requirement</span></span> | <span data-ttu-id="bb4ff-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb4ff-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb4ff-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb4ff-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bb4ff-117">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="bb4ff-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                      |
| <span data-ttu-id="bb4ff-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb4ff-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bb4ff-119">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="bb4ff-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                            |
| <span data-ttu-id="bb4ff-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb4ff-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb4ff-121"><dt>Mfobjects. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb4ff-121"><dt>Mfobjects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb4ff-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb4ff-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb4ff-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bb4ff-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bb4ff-124">Attributs de flux d’octets</span><span class="sxs-lookup"><span data-stu-id="bb4ff-124">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="bb4ff-125">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="bb4ff-125">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




