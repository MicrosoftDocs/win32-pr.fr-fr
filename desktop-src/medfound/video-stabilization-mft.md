---
description: La table MFT de stabilisation vidéo est une Microsoft Media Foundation transformation (MFT) qui effectue une stabilisation d’image sur un flux vidéo.
ms.assetid: BBC42190-08E4-4C3B-972A-FD30621A6CC1
title: Stabilisation vidéo MFT (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65eb64b05e41842b1f7b3ad2e49a6c064be08f0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523449"
---
# <a name="video-stabilization-mft"></a><span data-ttu-id="135ff-103">Stabilisation vidéo MFT</span><span class="sxs-lookup"><span data-stu-id="135ff-103">Video Stabilization MFT</span></span>

<span data-ttu-id="135ff-104">La table MFT de stabilisation vidéo est une Microsoft Media Foundation transformation (MFT) qui effectue une stabilisation d’image sur un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="135ff-104">The video stabilization MFT is a Microsoft Media Foundation transform (MFT) that performs image stabilization on a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="135ff-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="135ff-105">CLSID</span></span>

<span data-ttu-id="135ff-106">CLSID \_ CMSVideoDSPMFT</span><span class="sxs-lookup"><span data-stu-id="135ff-106">CLSID\_CMSVideoDSPMFT</span></span>

## <a name="interfaces"></a><span data-ttu-id="135ff-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="135ff-107">Interfaces</span></span>

-   [<span data-ttu-id="135ff-108">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="135ff-108">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="135ff-109">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="135ff-109">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="135ff-110">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="135ff-110">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="135ff-111">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="135ff-111">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="135ff-112">**IMediaExtension**</span><span class="sxs-lookup"><span data-stu-id="135ff-112">**IMediaExtension**</span></span>](/uwp/api/Windows.Media.IMediaExtension?view=winrt-19041)

## <a name="input-formats"></a><span data-ttu-id="135ff-113">Formats d’entrée</span><span class="sxs-lookup"><span data-stu-id="135ff-113">Input Formats</span></span>

<span data-ttu-id="135ff-114">Les combinaisons type de média et sous-type d’entrée acceptées par la MFT de stabilisation vidéo pour la vidéo non compressée sont :</span><span class="sxs-lookup"><span data-stu-id="135ff-114">The input media type and sub-type combinations accepted by the video stabilization MFT for uncompressed video are:</span></span>

-   <span data-ttu-id="135ff-115">**vidéo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="135ff-115">**MEDIATYPE\_VIDEO**</span></span>
-   <span data-ttu-id="135ff-116">**MEDIASUBTYPE \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="135ff-116">**MEDIASUBTYPE\_NV12**</span></span>
-   <span data-ttu-id="135ff-117">**MEDIASUBTYPE \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="135ff-117">**MEDIASUBTYPE\_YUY2**</span></span>

## <a name="output-formats"></a><span data-ttu-id="135ff-118">Formats de sortie</span><span class="sxs-lookup"><span data-stu-id="135ff-118">Output Formats</span></span>

<span data-ttu-id="135ff-119">Les combinaisons type de média de sortie et sous-type acceptées par la MFT de stabilisation vidéo sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="135ff-119">The output media type and sub-type combinations accepted by the video stabilization MFT are:</span></span>

-   <span data-ttu-id="135ff-120">**vidéo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="135ff-120">**MEDIATYPE\_VIDEO**</span></span>
-   <span data-ttu-id="135ff-121">**MEDIASUBTYPE \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="135ff-121">**MEDIASUBTYPE\_NV12**</span></span>

<span data-ttu-id="135ff-122">Le type de média d’entrée doit être défini avant le type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="135ff-122">The input media type must be set before the output media type.</span></span> <span data-ttu-id="135ff-123">Dans la plupart des cas, la prise en charge du format limité n’est pas un problème, car le pipeline insère automatiquement les conversions de couleur nécessaires.</span><span class="sxs-lookup"><span data-stu-id="135ff-123">In most situations, the limited format support is not an issue because the pipeline automatically inserts the necessary color conversions.</span></span>

<span data-ttu-id="135ff-124">Le composant MFT de stabilisation vidéo est en capacité de modifier le format dynamique en cas de modification de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="135ff-124">The video stabilization MFT component is capable of dynamic format change when input changes.</span></span> <span data-ttu-id="135ff-125">Lorsque la taille de l’image d’entrée change ou que le sous-type change, une modification de format dynamique est déclenchée sur le flux de sortie.</span><span class="sxs-lookup"><span data-stu-id="135ff-125">When the input picture size changes or the subtype changes, it will trigger a dynamic format change on the output stream.</span></span>

<span data-ttu-id="135ff-126">La table MFT de stabilisation vidéo effectue une conversion des couleurs dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="135ff-126">The video stabilization MFT will do color conversion in the following cases:</span></span>

-   <span data-ttu-id="135ff-127">Lorsque le format d’entrée est **MEDIASUBTYPE \_ YUY2**.</span><span class="sxs-lookup"><span data-stu-id="135ff-127">When the input format is **MEDIASUBTYPE\_YUY2**.</span></span>
-   <span data-ttu-id="135ff-128">Lorsque le mode de compatibilité de Microsoft DirectX 9,0 est utilisé.</span><span class="sxs-lookup"><span data-stu-id="135ff-128">When Microsoft DirectX 9.0 compatibility mode is used.</span></span>

### <a name="attributes"></a><span data-ttu-id="135ff-129">Attributs</span><span class="sxs-lookup"><span data-stu-id="135ff-129">Attributes</span></span>

<span data-ttu-id="135ff-130">Les attributs suivants sont pris en charge par la table MFT de stabilisation vidéo par le biais de l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="135ff-130">The following attributes are supported by the video stabilization MFT through the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

-   <span data-ttu-id="135ff-131">L’attribut [ \_ \_ mode MF VIDEODSP](mf-videodsp-mode.md) place la table MFT de stabilisation vidéo en mode de stabilisation ou en mode pass-through.</span><span class="sxs-lookup"><span data-stu-id="135ff-131">The attribute [MF\_VIDEODSP\_MODE](mf-videodsp-mode.md) puts the video stabilization MFT into either stabilization mode or pass-through mode.</span></span> <span data-ttu-id="135ff-132">L’application doit appeler [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) sur le **\_ \_ type GUID MF VIDEODSP** avec un entier correspondant à l’une des valeurs valides suivantes : **MFVideoDSPMode \_ stabilisation** = 4, **MFVideoDSPMode \_ passthrough** = 1.</span><span class="sxs-lookup"><span data-stu-id="135ff-132">The application should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on the GUID **MF\_VIDEODSP\_TYPE** with an integer corresponding to one of the following valid values: **MFVideoDSPMode\_Stabilization** = 4, **MFVideoDSPMode\_Passthrough** = 1.</span></span> <span data-ttu-id="135ff-133">Le \_ mode VIDEODSP MF \_ peut être modifié à tout moment pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="135ff-133">MF\_VIDEODSP\_MODE can be changed at any time during playback.</span></span> <span data-ttu-id="135ff-134">Cela provoque une modification du mode dynamique.</span><span class="sxs-lookup"><span data-stu-id="135ff-134">This causes a dynamic mode change.</span></span> <span data-ttu-id="135ff-135">La sortie passera à la valeur stabilised ou passera après les 16 ou 2 images (selon le mode de latence) après la modification de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="135ff-135">The output will switch to either stabilized or pass through after either 16 or 2 frames (depending on the latency mode) after the attribute is changed.</span></span>
-   <span data-ttu-id="135ff-136">La [ \_ faible \_ latence MF](mf-low-latency.md) de l’attribut place la MFT de stabilisation vidéo en mode de latence faible ou en mode haute qualité.</span><span class="sxs-lookup"><span data-stu-id="135ff-136">The attribute [MF\_LOW\_LATENCY](mf-low-latency.md) puts the video stabilization MFT into either low latency mode or high quality mode.</span></span> <span data-ttu-id="135ff-137">L’application doit appeler [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) sur la **\_ \_ latence faible** de GUID MF avec un entier correspondant à l’une des valeurs valides suivantes : faible latence = 1 haute qualité = 0</span><span class="sxs-lookup"><span data-stu-id="135ff-137">The application should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on the GUID **MF\_LOW\_LATENCY** with an integer corresponding to one of the following valid values: Low latency = 1 High Quality = 0</span></span>
-   <span data-ttu-id="135ff-138">L’attribut [MF \_ sa \_ d3d11 \_ BINDFLAGS](mf-sa-d3d11-bindflags.md) est utilisé par le pipeline pour spécifier les indicateurs de liaison d3d11 à partir desquels créer les exemples de sortie.</span><span class="sxs-lookup"><span data-stu-id="135ff-138">The attribute [MF\_SA\_D3D11\_BINDFLAGS](mf-sa-d3d11-bindflags.md) is used by the pipeline to specify the D3D11 bind flags to create the output samples with.</span></span> <span data-ttu-id="135ff-139">Toute combinaison de valeurs provenant de l’énumération de l' [**\_ \_ indicateur de liaison d3d11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) est valide.</span><span class="sxs-lookup"><span data-stu-id="135ff-139">Any combination of values from the [**D3D11\_BIND\_FLAG**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) enumeration is valid.</span></span>
-   <span data-ttu-id="135ff-140">Le nombre minimal d’échantillons de sortie de l’attribut **MF \_ sa \_ \_ \_ \_** est utilisé par le pipeline pour spécifier le nombre minimal d’exemples que ce composant doit prendre en charge lors de la sortie.</span><span class="sxs-lookup"><span data-stu-id="135ff-140">The attribute **MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT** is used by the pipeline to specify the minimum number of samples that this component must support on output.</span></span>
-   <span data-ttu-id="135ff-141">L’attribut [MFSampleExtension \_ VideoDSPMode](mfsampleextension-videodspmode.md) est défini sur chaque échantillon produit par la stabilisation pour indiquer que [le \_ \_ mode MF VIDEODSP](mf-videodsp-mode.md) effectif est appliqué à cet exemple (que l’exemple ait été stabilisé ou non).</span><span class="sxs-lookup"><span data-stu-id="135ff-141">The attribute [MFSampleExtension\_VideoDSPMode](mfsampleextension-videodspmode.md) is set on every sample produced by stabilization to indicate the effective [MF\_VIDEODSP\_MODE](mf-videodsp-mode.md) applied to that sample (whether or not the sample was stabilized).</span></span> <span data-ttu-id="135ff-142">Dans certaines conditions, les échantillons peuvent ne pas être stabilisés (en raison d’une charge élevée du système, ou des demandes de l’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="135ff-142">Under certain conditions, samples may not be stabilized (due to high system load, or requests by the user).</span></span> <span data-ttu-id="135ff-143">Cet attribut a les mêmes valeurs que l' \_ attribut de \_ mode VIDEODSP MF **( \_ stabilisation MFVideoDSPMode** et **MFVideoDSPMode \_ passthrough**).</span><span class="sxs-lookup"><span data-stu-id="135ff-143">This attribute has the same values as the MF\_VIDEODSP\_MODE attribute (**MFVideoDSPMode\_Stabilization** and **MFVideoDSPMode\_Passthrough**).</span></span> <span data-ttu-id="135ff-144">Pour récupérer la valeur de cet attribut, les applications doivent appeler [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) sur le GUID **MFSampleExtension \_ VideoDSPMode**.</span><span class="sxs-lookup"><span data-stu-id="135ff-144">To get the value of this attribute applications should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on GUID **MFSampleExtension\_VideoDSPMode**.</span></span>

## <a name="remarks"></a><span data-ttu-id="135ff-145">Notes</span><span class="sxs-lookup"><span data-stu-id="135ff-145">Remarks</span></span>

<span data-ttu-id="135ff-146">Une instance du DSP de stabilisation vidéo peut être créée de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="135ff-146">An instance of the video stabilization DSP can be created in one of the following ways:</span></span>

-   <span data-ttu-id="135ff-147">En appelant [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="135ff-147">By calling [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="135ff-148">Le DSP de stabilisation vidéo est enregistré sous la catégorie d' **\_ \_ \_ effet vidéo de la catégorie MFT** .</span><span class="sxs-lookup"><span data-stu-id="135ff-148">The video stabilization DSP is registered under the **MFT\_CATEGORY\_VIDEO\_EFFECT** category.</span></span>
-   <span data-ttu-id="135ff-149">En appelant la fonction COM **CoCreateInstance** en lui transmettant le CLSID CLSID **\_ CMSVideoDSPMFT**.</span><span class="sxs-lookup"><span data-stu-id="135ff-149">By calling the COM function **CoCreateInstance** passing it the CLSID **CLSID\_CMSVideoDSPMFT**.</span></span> <span data-ttu-id="135ff-150">Pour utiliser cette méthode, vous devez inclure wmcodecdsp. h et établir une liaison avec wmcodecdspuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="135ff-150">To use this method, you must include wmcodecdsp.h and link against wmcodecdspuuid.lib.</span></span>

<span data-ttu-id="135ff-151">En outre, le DSP de stabilisation vidéo prend en charge l’instanciation à l’aide de Windows Runtime en tant qu’extension Windows Media.</span><span class="sxs-lookup"><span data-stu-id="135ff-151">Additionally, the video stabilization DSP supports instantiation using Windows Runtime as a Windows Media Extension.</span></span> <span data-ttu-id="135ff-152">Il est défini sur [**Windows. Media. VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)et son nom complet est « Windows. Media. VideoEffects. VideoStabilization ».</span><span class="sxs-lookup"><span data-stu-id="135ff-152">It is defined on the [**Windows.Media.VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041), and its full name is "Windows.Media.VideoEffects.VideoStabilization".</span></span>

## <a name="requirements"></a><span data-ttu-id="135ff-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="135ff-153">Requirements</span></span>



| <span data-ttu-id="135ff-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="135ff-154">Requirement</span></span> | <span data-ttu-id="135ff-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="135ff-155">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="135ff-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="135ff-156">Header</span></span><br/> | <dl> <span data-ttu-id="135ff-157"><dt>Camerauicontrol. h</dt></span><span class="sxs-lookup"><span data-stu-id="135ff-157"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="135ff-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="135ff-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="135ff-159">Processeurs de signaux numériques</span><span class="sxs-lookup"><span data-stu-id="135ff-159">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> <dt>

[<span data-ttu-id="135ff-160">**Windows.Media.VideoEffects**</span><span class="sxs-lookup"><span data-stu-id="135ff-160">**Windows.Media.VideoEffects**</span></span>](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)
</dt> </dl>

 

 
