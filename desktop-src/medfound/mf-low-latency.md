---
description: Active le traitement à faible latence dans le pipeline Microsoft Media Foundation.
ms.assetid: 4D11B4D6-8CFF-4850-BF8F-9019A1F79153
title: Attribut MF_LOW_LATENCY (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d1b0a89452256f01fc893ced7dc191fd064bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757864"
---
# <a name="mf_low_latency-attribute"></a><span data-ttu-id="bbac5-103">\_Attribut de \_ latence faible MF</span><span class="sxs-lookup"><span data-stu-id="bbac5-103">MF\_LOW\_LATENCY attribute</span></span>

<span data-ttu-id="bbac5-104">Active le traitement à faible latence dans le pipeline Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="bbac5-104">Enables low-latency processing in the Microsoft Media Foundation pipeline.</span></span>

## <a name="data-type"></a><span data-ttu-id="bbac5-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="bbac5-105">Data type</span></span>

<span data-ttu-id="bbac5-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bbac5-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="bbac5-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="bbac5-107">Get/set</span></span>

<span data-ttu-id="bbac5-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="bbac5-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="bbac5-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="bbac5-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="bbac5-110">Notes</span><span class="sxs-lookup"><span data-stu-id="bbac5-110">Remarks</span></span>

<span data-ttu-id="bbac5-111">Une latence faible est définie comme le plus petit délai possible entre le moment où les données multimédia sont générées (ou reçues) et le moment où elles sont affichées.</span><span class="sxs-lookup"><span data-stu-id="bbac5-111">Low latency is defined as the smallest possible delay from when the media data is generated (or received) to when it is rendered.</span></span> <span data-ttu-id="bbac5-112">Une faible latence est souhaitable pour les scénarios de communication en temps réel.</span><span class="sxs-lookup"><span data-stu-id="bbac5-112">Low latency is desirable for real-time communication scenarios.</span></span> <span data-ttu-id="bbac5-113">Pour d’autres scénarios, tels que la lecture ou le transcodage local, vous ne devez généralement pas activer le mode de latence faible, car cela peut affecter la qualité.</span><span class="sxs-lookup"><span data-stu-id="bbac5-113">For other scenarios, such as local playback or transcoding, you typically should not enable low-latency mode, because it can affect quality.</span></span>

> [!Note]  
> <span data-ttu-id="bbac5-114">La valeur GUID de cet attribut est identique à la propriété [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md) définie pour l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="bbac5-114">The GUID value of this attribute is identical to the [CODECAPI\_AVLowLatencyMode](codecapi-avlowlatencymode.md) property defined for the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>

 

<span data-ttu-id="bbac5-115">Définissez cet attribut sur les composants de pipeline comme suit :</span><span class="sxs-lookup"><span data-stu-id="bbac5-115">Set this attribute on pipeline components as follows:</span></span>

-   <span data-ttu-id="bbac5-116">Source du média : utilisez la méthode [**IMFMediaSourceEx :: GetSourceAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) .</span><span class="sxs-lookup"><span data-stu-id="bbac5-116">Media source: Use the [**IMFMediaSourceEx::GetSourceAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) method.</span></span>
-   <span data-ttu-id="bbac5-117">Media Foundation Transform (MFT) : utilisez la méthode [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="bbac5-117">Media Foundation transform (MFT): Use the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="bbac5-118">Pour les encodeurs, l’encodeur peut prendre en charge une faible latence par le biais de l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="bbac5-118">For encoders, the encoder might support low latency through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>
-   <span data-ttu-id="bbac5-119">Récepteur multimédia : interrogez le récepteur multimédia pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="bbac5-119">Media sink: Query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="bbac5-120">En général, les applications ne définissent pas cet attribut directement sur les composants de pipeline, mais définissent l’attribut sur l’un des objets suivants :</span><span class="sxs-lookup"><span data-stu-id="bbac5-120">Applications typically do not set this attribute directly on the pipeline components, but instead set the attribute on one of the following objects:</span></span>

-   <span data-ttu-id="bbac5-121">[Session multimédia](media-session.md): utilisez le paramètre *pConfiguation* de la fonction [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) ou [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) , ou définissez l’attribut sur la topologie.</span><span class="sxs-lookup"><span data-stu-id="bbac5-121">[Media Session](media-session.md): Use the *pConfiguation* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function, or else set the attribute on the topology.</span></span>
-   <span data-ttu-id="bbac5-122">[Lecteur source](source-reader.md): définissez l’attribut avec les propriétés de configuration lorsque vous créez le lecteur source.</span><span class="sxs-lookup"><span data-stu-id="bbac5-122">[Source Reader](source-reader.md): Set the attribute with the configuration properties when you create the Source Reader.</span></span> <span data-ttu-id="bbac5-123">Pour plus d’informations, consultez [attributs du lecteur source](source-reader-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="bbac5-123">For more information, see [Source Reader Attributes](source-reader-attributes.md).</span></span>
-   <span data-ttu-id="bbac5-124">[Enregistreur du récepteur](sink-writer.md): définissez l’attribut avec les propriétés de configuration lorsque vous créez le writer du récepteur.</span><span class="sxs-lookup"><span data-stu-id="bbac5-124">[Sink Writer](sink-writer.md): Set the attribute with the configuration properties when you create the Sink Writer.</span></span> <span data-ttu-id="bbac5-125">Pour plus d’informations, consultez [attributs du writer du récepteur](sink-writer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="bbac5-125">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbac5-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbac5-126">Requirements</span></span>



| <span data-ttu-id="bbac5-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbac5-127">Requirement</span></span> | <span data-ttu-id="bbac5-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbac5-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bbac5-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbac5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bbac5-130">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="bbac5-130">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="bbac5-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbac5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bbac5-132">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="bbac5-132">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="bbac5-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="bbac5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbac5-134"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbac5-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbac5-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbac5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbac5-136">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bbac5-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bbac5-137">Attributs du writer du récepteur</span><span class="sxs-lookup"><span data-stu-id="bbac5-137">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="bbac5-138">Attributs du lecteur source</span><span class="sxs-lookup"><span data-stu-id="bbac5-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> <dt>

[<span data-ttu-id="bbac5-139">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="bbac5-139">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
