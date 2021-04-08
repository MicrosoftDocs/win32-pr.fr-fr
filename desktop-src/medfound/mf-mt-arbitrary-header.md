---
description: Données spécifiques au type d’un flux binaire dans un fichier ASF (Advanced Systems Format).
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: Attribut MF_MT_ARBITRARY_HEADER (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd559ede3506335378ae1d56bf5b886e1407946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034207"
---
# <a name="mf_mt_arbitrary_header-attribute"></a><span data-ttu-id="53f9a-103">\_Attribut d' \_ \_ en-tête arbitraire MT</span><span class="sxs-lookup"><span data-stu-id="53f9a-103">MF\_MT\_ARBITRARY\_HEADER attribute</span></span>

<span data-ttu-id="53f9a-104">Données spécifiques au type d’un flux binaire dans un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="53f9a-104">Type-specific data for a binary stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="53f9a-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="53f9a-105">Data type</span></span>

<span data-ttu-id="53f9a-106">**[**MT \_ \_En-tête arbitraire**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** stocké en tant qu' **octet \[ \]**</span><span class="sxs-lookup"><span data-stu-id="53f9a-106">**[**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="53f9a-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="53f9a-107">Get/set</span></span>

<span data-ttu-id="53f9a-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="53f9a-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="53f9a-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="53f9a-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="53f9a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="53f9a-110">Remarks</span></span>

<span data-ttu-id="53f9a-111">Les fichiers ASF peuvent contenir des flux de données binaires.</span><span class="sxs-lookup"><span data-stu-id="53f9a-111">ASF files can contain streams with binary data.</span></span> <span data-ttu-id="53f9a-112">L' \_ \_ \_ attribut d’en-tête arbitraire MT arbitraire dans le type de média contient une structure d' [**\_ \_ en-tête MT arbitraire**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) qui décrit le flux.</span><span class="sxs-lookup"><span data-stu-id="53f9a-112">The MF\_MT\_ARBITRARY\_HEADER attribute in the media type contains an [**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) structure that describes the stream.</span></span>

<span data-ttu-id="53f9a-113">En plus de l' \_ attribut d' \_ \_ en-tête arbitraire MT, le type de média pour un flux binaire ASF contient les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="53f9a-113">In addition to the MF\_MT\_ARBITRARY\_HEADER attribute, the media type for an ASF binary stream contains the following attributes:</span></span>



| <span data-ttu-id="53f9a-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="53f9a-114">Attribute</span></span>                                                 | <span data-ttu-id="53f9a-115">Description</span><span class="sxs-lookup"><span data-stu-id="53f9a-115">Description</span></span>                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="53f9a-116">**\_type de \_ majeurese MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="53f9a-116">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="53f9a-117">La valeur de l’attribut est **MFMediaType \_ binaire**.</span><span class="sxs-lookup"><span data-stu-id="53f9a-117">The value of the attribute is **MFMediaType\_Binary**.</span></span> |
| [<span data-ttu-id="53f9a-118">\_ \_ format arbitraire MT \_</span><span class="sxs-lookup"><span data-stu-id="53f9a-118">MF\_MT\_ARBITRARY\_FORMAT</span></span>](mf-mt-arbitrary-format.md)   | <span data-ttu-id="53f9a-119">Contient des données de format supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="53f9a-119">Contains additional format data.</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="53f9a-120">Dans le kit de développement logiciel (SDK) Windows Media format, les flux binaires sont appelés des *flux arbitraires* ou des *flux de données arbitraires*.</span><span class="sxs-lookup"><span data-stu-id="53f9a-120">In the Windows Media Format SDK, binary streams are called *arbitrary streams* or *arbitrary data streams*.</span></span>

 

<span data-ttu-id="53f9a-121">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="53f9a-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="53f9a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53f9a-122">Requirements</span></span>



| <span data-ttu-id="53f9a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53f9a-123">Requirement</span></span> | <span data-ttu-id="53f9a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="53f9a-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="53f9a-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53f9a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="53f9a-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53f9a-126">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="53f9a-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53f9a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="53f9a-128">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53f9a-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="53f9a-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="53f9a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="53f9a-130"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="53f9a-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53f9a-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53f9a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f9a-132">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="53f9a-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="53f9a-133">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="53f9a-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




