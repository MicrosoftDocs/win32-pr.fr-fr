---
description: Permet au lecteur source ou au writer de récepteur d’utiliser des transformations Media Foundation basées sur le matériel (MFTs).
ms.assetid: 03f2fa76-b828-40b1-929d-60e7d5ab49bb
title: Attribut MF_READWRITE_ENABLE_HARDWARE_TRANSFORMS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 642be732a51f064d07e57609a886810f2a9c40b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319978"
---
# <a name="mf_readwrite_enable_hardware_transforms-attribute"></a><span data-ttu-id="644b7-103">MF \_ ReadWrite \_ activer \_ l' \_ attribut de transformations de matériel</span><span class="sxs-lookup"><span data-stu-id="644b7-103">MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS attribute</span></span>

<span data-ttu-id="644b7-104">Permet au lecteur source ou au writer de récepteur d’utiliser des transformations Media Foundation basées sur le matériel (MFTs).</span><span class="sxs-lookup"><span data-stu-id="644b7-104">Enables the source reader or sink writer to use hardware-based Media Foundation transforms (MFTs).</span></span>

## <a name="data-type"></a><span data-ttu-id="644b7-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="644b7-105">Data type</span></span>

<span data-ttu-id="644b7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="644b7-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="644b7-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="644b7-107">Get/set</span></span>

<span data-ttu-id="644b7-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="644b7-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="644b7-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="644b7-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="644b7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="644b7-110">Remarks</span></span>

<span data-ttu-id="644b7-111">Par défaut, le lecteur source et le writer du récepteur n’utilisent pas de décodeurs ou d’encodeurs matériels.</span><span class="sxs-lookup"><span data-stu-id="644b7-111">By default, the source reader and sink writer do not use hardware decoders or encoders.</span></span> <span data-ttu-id="644b7-112">Pour activer l’utilisation du matériel MFTs, affectez la valeur **true** à cet attribut lorsque vous créez le lecteur source ou le writer du récepteur.</span><span class="sxs-lookup"><span data-stu-id="644b7-112">To enable the use of hardware MFTs, set this attribute to **TRUE** when you create the source reader or sink writer.</span></span>

<span data-ttu-id="644b7-113">Utilisez cet attribut avec les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="644b7-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="644b7-114">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="644b7-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="644b7-115">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="644b7-115">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="644b7-116">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="644b7-116">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [<span data-ttu-id="644b7-117">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="644b7-117">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="644b7-118">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="644b7-118">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

<span data-ttu-id="644b7-119">Il existe une exception au comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="644b7-119">There is one exception to the default behavior.</span></span> <span data-ttu-id="644b7-120">Le lecteur source et le writer du récepteur utilisent automatiquement des MFTs qui sont inscrits localement dans le processus de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="644b7-120">The source reader and sink writer automatically use MFTs that are registered locally in the caller's process.</span></span> <span data-ttu-id="644b7-121">Pour inscrire une table MFT localement, appelez [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) ou [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid).</span><span class="sxs-lookup"><span data-stu-id="644b7-121">To register an MFT locally, call [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid).</span></span> <span data-ttu-id="644b7-122">Les MFTs matériels inscrits localement sont utilisés, même si l’attribut de **\_ \_ \_ \_ transformations matérielles MF ReadWrite Enable** n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="644b7-122">Hardware MFTs that are registered locally are used even if the **MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS** attribute is not set.</span></span>

<span data-ttu-id="644b7-123">Cet attribut n’affecte pas le décodage vidéo accéléré par le matériel qui utilise l’accélération vidéo DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="644b7-123">This attribute does not affect hardware-accelerated video decoding that uses DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="644b7-124">Pour activer le décodage DXVA dans le lecteur source, définissez l’attribut du [ \_ \_ \_ \_ Gestionnaire D3D du lecteur source MF](mf-source-reader-d3d-manager.md) .</span><span class="sxs-lookup"><span data-stu-id="644b7-124">To enable DXVA decoding in the source reader, set the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute.</span></span>

<span data-ttu-id="644b7-125">Si cet attribut a la **valeur true**, ne définissez pas l’attribut de [ \_ \_ \_ convertisseurs de désactivation MF ReadWrite](mf-readwrite-disable-converters.md) .</span><span class="sxs-lookup"><span data-stu-id="644b7-125">If this attribute is **TRUE**, do not set the [MF\_READWRITE\_DISABLE\_CONVERTERS](mf-readwrite-disable-converters.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="644b7-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="644b7-126">Requirements</span></span>



| <span data-ttu-id="644b7-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="644b7-127">Requirement</span></span> | <span data-ttu-id="644b7-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="644b7-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="644b7-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="644b7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="644b7-130">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="644b7-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="644b7-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="644b7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="644b7-132">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="644b7-132">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="644b7-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="644b7-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="644b7-134"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="644b7-134"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="644b7-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="644b7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="644b7-136">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="644b7-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="644b7-137">Attributs du writer du récepteur</span><span class="sxs-lookup"><span data-stu-id="644b7-137">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="644b7-138">Attributs du lecteur source</span><span class="sxs-lookup"><span data-stu-id="644b7-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




