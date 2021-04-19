---
description: Spécifie le type MIME d’un flux d’octets.
ms.assetid: bcf86ece-2673-4ed8-98fd-cd0e2154b4a8
title: Attribut MF_BYTESTREAM_CONTENT_TYPE (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d7413fa6fd2ce74530432d60976e3c7ebf702af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514050"
---
# <a name="mf_bytestream_content_type-attribute"></a><span data-ttu-id="4c276-103">\_Attribut de \_ type de contenu BYTESTREAM MF \_</span><span class="sxs-lookup"><span data-stu-id="4c276-103">MF\_BYTESTREAM\_CONTENT\_TYPE attribute</span></span>

<span data-ttu-id="4c276-104">Spécifie le type MIME d’un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="4c276-104">Specifies the MIME type of a byte stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="4c276-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="4c276-105">Data type</span></span>

<span data-ttu-id="4c276-106">Chaîne de caractères larges</span><span class="sxs-lookup"><span data-stu-id="4c276-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="4c276-107">Notes</span><span class="sxs-lookup"><span data-stu-id="4c276-107">Remarks</span></span>

<span data-ttu-id="4c276-108">Pour obtenir la valeur de l’attribut, interrogez l’objet de flux d’octets pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="4c276-108">To get the attribute value, query the byte stream object for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="4c276-109">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4c276-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c276-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c276-110">Requirements</span></span>



| <span data-ttu-id="4c276-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c276-111">Requirement</span></span> | <span data-ttu-id="4c276-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c276-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c276-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c276-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4c276-114">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="4c276-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="4c276-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c276-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4c276-116">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="4c276-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="4c276-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c276-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c276-118"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c276-118"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c276-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c276-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c276-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4c276-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4c276-121">Attributs de flux d’octets</span><span class="sxs-lookup"><span data-stu-id="4c276-121">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="4c276-122">**IMFAttributes :: GetString**</span><span class="sxs-lookup"><span data-stu-id="4c276-122">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="4c276-123">**IMFAttributes :: SetString**</span><span class="sxs-lookup"><span data-stu-id="4c276-123">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="4c276-124">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="4c276-124">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




