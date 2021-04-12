---
description: Contient un pointeur vers l’interface de rappel des applications pour le lecteur source.
ms.assetid: de226a5a-03c0-4bfe-bb20-8969ce43cf53
title: Attribut MF_SOURCE_READER_ASYNC_CALLBACK (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66542a155fbb6fa3e56958733626b1d0b750ab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203714"
---
# <a name="mf_source_reader_async_callback-attribute"></a><span data-ttu-id="08d9d-103">\_Attribut de \_ \_ rappel asynchrone du lecteur source MF \_</span><span class="sxs-lookup"><span data-stu-id="08d9d-103">MF\_SOURCE\_READER\_ASYNC\_CALLBACK attribute</span></span>

<span data-ttu-id="08d9d-104">Contient un pointeur vers l’interface de rappel de l’application pour le [lecteur source](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="08d9d-104">Contains a pointer to the application's callback interface for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="08d9d-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="08d9d-105">Data type</span></span>

<span data-ttu-id="08d9d-106">**IMFSourceReaderCallback \** _ stocké en tant que _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="08d9d-106">**IMFSourceReaderCallback\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="08d9d-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="08d9d-107">Get/set</span></span>

<span data-ttu-id="08d9d-108">Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="08d9d-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="08d9d-109">Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="08d9d-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="08d9d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="08d9d-110">Remarks</span></span>

<span data-ttu-id="08d9d-111">La valeur de cet attribut est un pointeur vers l’interface [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) de l’application.</span><span class="sxs-lookup"><span data-stu-id="08d9d-111">The value of this attribute is a pointer to the application's [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) interface.</span></span>

<span data-ttu-id="08d9d-112">Utilisez cet attribut avec les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="08d9d-112">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="08d9d-113">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="08d9d-113">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="08d9d-114">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="08d9d-114">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="08d9d-115">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="08d9d-115">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

## <a name="requirements"></a><span data-ttu-id="08d9d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08d9d-116">Requirements</span></span>



| <span data-ttu-id="08d9d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08d9d-117">Requirement</span></span> | <span data-ttu-id="08d9d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="08d9d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="08d9d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08d9d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="08d9d-120">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="08d9d-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="08d9d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08d9d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="08d9d-122">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="08d9d-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="08d9d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="08d9d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="08d9d-124"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="08d9d-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08d9d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08d9d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08d9d-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08d9d-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="08d9d-127">Lecteur source</span><span class="sxs-lookup"><span data-stu-id="08d9d-127">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="08d9d-128">Attributs du lecteur source</span><span class="sxs-lookup"><span data-stu-id="08d9d-128">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




