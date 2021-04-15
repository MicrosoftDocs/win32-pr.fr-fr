---
description: Contient un type de média encapsulé dans un autre type de média.
ms.assetid: 3bd94523-0206-44d8-83a2-e569e4ab7815
title: Attribut MF_MT_WRAPPED_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad09c69f7b99c2c376a207270cadb034e735546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393259"
---
# <a name="mf_mt_wrapped_type-attribute"></a><span data-ttu-id="1e487-103">\_Attribut de \_ \_ type encapsulé pour MF MT</span><span class="sxs-lookup"><span data-stu-id="1e487-103">MF\_MT\_WRAPPED\_TYPE attribute</span></span>

<span data-ttu-id="1e487-104">Contient un type de média encapsulé dans un autre type de média.</span><span class="sxs-lookup"><span data-stu-id="1e487-104">Contains a media type that has been wrapped in another media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="1e487-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="1e487-105">Data type</span></span>

<span data-ttu-id="1e487-106">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="1e487-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="1e487-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1e487-107">Remarks</span></span>

<span data-ttu-id="1e487-108">Cet attribut est utilisé dans la fonction [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) , qui encapsule un type de média à l’intérieur d’un autre type de média.</span><span class="sxs-lookup"><span data-stu-id="1e487-108">This attribute is used in the [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) function, which wraps a media type inside another media type.</span></span>

<span data-ttu-id="1e487-109">La fonction [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1e487-109">The [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) function does the following:</span></span>

1.  <span data-ttu-id="1e487-110">Convertit le type de média d’origine en tableau binaire.</span><span class="sxs-lookup"><span data-stu-id="1e487-110">Converts the original media type into a binary array.</span></span>
2.  <span data-ttu-id="1e487-111">Définit l’attribut de **\_ \_ \_ type encapsulé MT Wrapped** sur le nouveau type de média.</span><span class="sxs-lookup"><span data-stu-id="1e487-111">Sets the **MF\_MT\_WRAPPED\_TYPE** attribute on the new media type.</span></span> <span data-ttu-id="1e487-112">La valeur de l’attribut est le tableau binaire.</span><span class="sxs-lookup"><span data-stu-id="1e487-112">The value of the attribute is the binary array.</span></span>

<span data-ttu-id="1e487-113">En général, les applications n’utilisent pas cet attribut directement.</span><span class="sxs-lookup"><span data-stu-id="1e487-113">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="1e487-114">Pour désencapsuler le type de média d’origine, appelez [**MFUnwrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype).</span><span class="sxs-lookup"><span data-stu-id="1e487-114">To unwrap the original media type, call [**MFUnwrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype).</span></span>

<span data-ttu-id="1e487-115">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1e487-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e487-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e487-116">Requirements</span></span>



| <span data-ttu-id="1e487-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e487-117">Requirement</span></span> | <span data-ttu-id="1e487-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e487-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e487-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e487-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1e487-120">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="1e487-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="1e487-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e487-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1e487-122">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="1e487-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="1e487-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e487-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e487-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e487-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e487-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e487-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e487-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1e487-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1e487-127">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="1e487-127">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="1e487-128">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="1e487-128">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="1e487-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="1e487-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="1e487-130">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="1e487-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




