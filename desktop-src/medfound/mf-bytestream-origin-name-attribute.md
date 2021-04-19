---
description: Spécifie l’URL d’origine d’un flux d’octets.
ms.assetid: 31d7de71-5bbb-4c29-8ce0-df3684c56916
title: Attribut MF_BYTESTREAM_ORIGIN_NAME (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe32602501b3750f709135cf7ca458b6eb6a572f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106539062"
---
# <a name="mf_bytestream_origin_name-attribute"></a><span data-ttu-id="4401e-103">\_Attribut de \_ nom d’origine MF BYTESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="4401e-103">MF\_BYTESTREAM\_ORIGIN\_NAME attribute</span></span>

<span data-ttu-id="4401e-104">Spécifie l’URL d’origine d’un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="4401e-104">Specifies the original URL for a byte stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="4401e-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="4401e-105">Data type</span></span>

<span data-ttu-id="4401e-106">Chaîne de caractères larges</span><span class="sxs-lookup"><span data-stu-id="4401e-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="4401e-107">Notes</span><span class="sxs-lookup"><span data-stu-id="4401e-107">Remarks</span></span>

<span data-ttu-id="4401e-108">Les flux d’octets basés sur des fichiers peuvent prendre en charge cet attribut.</span><span class="sxs-lookup"><span data-stu-id="4401e-108">File-based byte streams can support this attribute.</span></span> <span data-ttu-id="4401e-109">La valeur de l’attribut est définie lors de la création du flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="4401e-109">The attribute value is set when the byte stream is created.</span></span> <span data-ttu-id="4401e-110">Pour obtenir la valeur de l’attribut, interrogez l’objet de flux d’octets pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="4401e-110">To get the attribute value, query the byte stream object for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="4401e-111">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4401e-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4401e-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4401e-112">Requirements</span></span>



| <span data-ttu-id="4401e-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4401e-113">Requirement</span></span> | <span data-ttu-id="4401e-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="4401e-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4401e-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4401e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4401e-116">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="4401e-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="4401e-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4401e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4401e-118">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="4401e-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="4401e-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="4401e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4401e-120"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4401e-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4401e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4401e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4401e-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4401e-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4401e-123">Attributs de flux d’octets</span><span class="sxs-lookup"><span data-stu-id="4401e-123">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="4401e-124">**IMFAttributes :: GetString**</span><span class="sxs-lookup"><span data-stu-id="4401e-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="4401e-125">**IMFAttributes :: SetString**</span><span class="sxs-lookup"><span data-stu-id="4401e-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="4401e-126">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="4401e-126">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




