---
description: Active ou désactive les conversions de format par le lecteur source ou le writer du récepteur.
ms.assetid: 282b70c3-c81c-47dd-bfa2-7e77138ccb91
title: Attribut MF_READWRITE_DISABLE_CONVERTERS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8532c45ca3aeb272fa6b6ef422e0d82e40bd3e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210486"
---
# <a name="mf_readwrite_disable_converters-attribute"></a><span data-ttu-id="a4515-103">\_Attribut de \_ désactivation des \_ convertisseurs MF ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a4515-103">MF\_READWRITE\_DISABLE\_CONVERTERS attribute</span></span>

<span data-ttu-id="a4515-104">Active ou désactive les conversions de format par le lecteur source ou le writer du récepteur.</span><span class="sxs-lookup"><span data-stu-id="a4515-104">Enables or disables format conversions by the source reader or sink writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="a4515-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="a4515-105">Data type</span></span>

<span data-ttu-id="a4515-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a4515-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="a4515-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="a4515-107">Get/set</span></span>

<span data-ttu-id="a4515-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="a4515-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="a4515-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="a4515-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="a4515-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a4515-110">Remarks</span></span>

<span data-ttu-id="a4515-111">Par défaut, le lecteur source et le writer du récepteur peuvent effectuer des conversions de format sur des flux audio et vidéo non compressés.</span><span class="sxs-lookup"><span data-stu-id="a4515-111">By default, the source reader and sink writer can perform some format conversions on uncompressed audio and video streams.</span></span> <span data-ttu-id="a4515-112">Pour désactiver ce comportement, affectez la **valeur true** à cet attribut lorsque vous créez le lecteur source ou le writer du récepteur.</span><span class="sxs-lookup"><span data-stu-id="a4515-112">To disable this behavior, set this attribute to **TRUE** when you create the source reader or sink writer.</span></span>

<span data-ttu-id="a4515-113">Utilisez cet attribut avec les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="a4515-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="a4515-114">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="a4515-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="a4515-115">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="a4515-115">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="a4515-116">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="a4515-116">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [<span data-ttu-id="a4515-117">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="a4515-117">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="a4515-118">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="a4515-118">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="a4515-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4515-119">Requirements</span></span>



| <span data-ttu-id="a4515-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4515-120">Requirement</span></span> | <span data-ttu-id="a4515-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4515-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4515-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4515-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a4515-123">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a4515-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="a4515-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4515-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a4515-125">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a4515-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a4515-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="a4515-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4515-127"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4515-127"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4515-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4515-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4515-129">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a4515-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a4515-130">Attributs du writer du récepteur</span><span class="sxs-lookup"><span data-stu-id="a4515-130">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="a4515-131">Attributs du lecteur source</span><span class="sxs-lookup"><span data-stu-id="a4515-131">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




