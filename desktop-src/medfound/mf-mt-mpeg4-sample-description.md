---
description: Contient l’exemple de zone de description pour un fichier MP4 ou 3GP.
ms.assetid: ea157988-bd15-465c-bd6a-6d33cc1a0323
title: Attribut MF_MT_MPEG4_SAMPLE_DESCRIPTION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4620ae0b50a2c6f2dae7663aab0c49f13bc5a162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867545"
---
# <a name="mf_mt_mpeg4_sample_description-attribute"></a><span data-ttu-id="31872-103">\_Attribut de \_ Description du MPEG4 MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="31872-103">MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION attribute</span></span>

<span data-ttu-id="31872-104">Contient l’exemple de zone de description pour un fichier MP4 ou 3GP.</span><span class="sxs-lookup"><span data-stu-id="31872-104">Contains the sample description box for an MP4 or 3GP file.</span></span>

## <a name="data-type"></a><span data-ttu-id="31872-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="31872-105">Data type</span></span>

<span data-ttu-id="31872-106">**POIDS\[\]**</span><span class="sxs-lookup"><span data-stu-id="31872-106">**BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="31872-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="31872-107">Get/set</span></span>

<span data-ttu-id="31872-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="31872-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="31872-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="31872-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="31872-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="31872-110">Applies to</span></span>

[<span data-ttu-id="31872-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="31872-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="31872-112">Notes</span><span class="sxs-lookup"><span data-stu-id="31872-112">Remarks</span></span>

<span data-ttu-id="31872-113">La zone Description de l’exemple décrit l’encodage utilisé pour un flux dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="31872-113">The sample description box describes the encoding used for a stream in the file.</span></span>

<span data-ttu-id="31872-114">La source de fichier MPEG-4 définit cet attribut sur le type de média pour chaque flux.</span><span class="sxs-lookup"><span data-stu-id="31872-114">The MPEG-4 file source sets this attribute on the media type for each stream.</span></span> <span data-ttu-id="31872-115">La valeur de l’attribut correspond aux données brutes de la zone de description de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="31872-115">The value of the attribute is the raw data in the sample description box.</span></span> <span data-ttu-id="31872-116">Si la source du fichier MPEG-4 peut analyser l’exemple de description, elle ajoute également les détails du format au type de média.</span><span class="sxs-lookup"><span data-stu-id="31872-116">If the MPEG-4 file source can parse the sample description, it also adds the format details to the media type.</span></span> <span data-ttu-id="31872-117">Dans le cas contraire, l’application ou le décodeur doit analyser l’exemple de description de l' \_ attribut de description du MPEG4 MF MT \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="31872-117">Otherwise, the application or the decoder must parse the sample description from the MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION attribute.</span></span>

<span data-ttu-id="31872-118">Lors de la définition de cet attribut sur le récepteur MPEG-4 par le biais de la méthode [**IMFMediaTypeHandler :: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) , les données de l’exemple de description de l’exemple d’attribut \_ MPEG4 MT MT \_ \_ \_ ne doivent pas changer après l’envoi d’un ou de plusieurs échantillons au récepteur de l’interface [**IMFStreamSink ::P rocesssample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) du flux correspondant.</span><span class="sxs-lookup"><span data-stu-id="31872-118">When setting this attribute on MPEG-4 sink through [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) method, the data for the attribute MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION should not change after one or more samples have been sent to the sink on the corresponding stream's [**IMFStreamSink::ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) interface.</span></span>

<span data-ttu-id="31872-119">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="31872-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="31872-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31872-120">Requirements</span></span>



| <span data-ttu-id="31872-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31872-121">Requirement</span></span> | <span data-ttu-id="31872-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="31872-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="31872-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31872-123">Minimum supported client</span></span><br/> | <span data-ttu-id="31872-124">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="31872-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="31872-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31872-125">Minimum supported server</span></span><br/> | <span data-ttu-id="31872-126">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="31872-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="31872-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="31872-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="31872-128"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="31872-128"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31872-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31872-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31872-130">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="31872-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="31872-131">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="31872-131">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




