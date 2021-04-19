---
description: Contient les propriétés de configuration du lecteur source.
ms.assetid: f7e5ef6a-5fc3-4f39-acc0-61ce79030211
title: Attribut MF_SOURCE_READER_MEDIASOURCE_CONFIG (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f36b2a09810dd1c2563033ea65643f1dabcb3f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106542101"
---
# <a name="mf_source_reader_mediasource_config-attribute"></a><span data-ttu-id="9a409-103">Attribut de configuration de la \_ source du lecteur de source MF \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="9a409-103">MF\_SOURCE\_READER\_MEDIASOURCE\_CONFIG attribute</span></span>

<span data-ttu-id="9a409-104">Contient les propriétés de configuration du [lecteur source](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="9a409-104">Contains configuration properties for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="9a409-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="9a409-105">Data type</span></span>

<span data-ttu-id="9a409-106">**IPropertyStore \* *_ stocké en tant que _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="9a409-106">**IPropertyStore\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="9a409-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="9a409-107">Get/set</span></span>

<span data-ttu-id="9a409-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="9a409-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="9a409-109">Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="9a409-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="9a409-110">Notes</span><span class="sxs-lookup"><span data-stu-id="9a409-110">Remarks</span></span>

<span data-ttu-id="9a409-111">La valeur de cet attribut est un pointeur vers l’interface **IPropertyStore** d’une banque de propriétés.</span><span class="sxs-lookup"><span data-stu-id="9a409-111">The value of this attribute is a pointer to the **IPropertyStore** interface of a property store.</span></span> <span data-ttu-id="9a409-112">Vous pouvez utiliser cet attribut pour passer des propriétés de configuration à la source du média.</span><span class="sxs-lookup"><span data-stu-id="9a409-112">You can use this attribute to pass configuration properties to the media source.</span></span>

<span data-ttu-id="9a409-113">Utilisez cet attribut avec les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="9a409-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="9a409-114">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="9a409-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="9a409-115">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="9a409-115">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

<span data-ttu-id="9a409-116">En interne, le lecteur source transmet le pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="9a409-116">Internally, the source reader passes the **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="9a409-117">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="9a409-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a409-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a409-118">Requirements</span></span>



| <span data-ttu-id="9a409-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a409-119">Requirement</span></span> | <span data-ttu-id="9a409-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a409-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a409-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a409-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9a409-122">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="9a409-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="9a409-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a409-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9a409-124">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="9a409-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="9a409-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="9a409-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a409-126"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a409-126"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a409-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a409-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a409-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9a409-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9a409-129">Lecteur source</span><span class="sxs-lookup"><span data-stu-id="9a409-129">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="9a409-130">Attributs du lecteur source</span><span class="sxs-lookup"><span data-stu-id="9a409-130">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




