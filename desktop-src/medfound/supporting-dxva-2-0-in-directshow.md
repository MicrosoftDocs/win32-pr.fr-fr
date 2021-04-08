---
description: Cette rubrique décrit comment prendre en charge DirectX Video Acceleration (DXVA) 2,0 dans un filtre de décodeur DirectShow.
ms.assetid: 40deaddb-bb17-4a34-8294-5c7dc8a8a457
title: Prise en charge de DXVA 2,0 dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dda956b60d4905c2392e1a50bd62ee8421b944b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863406"
---
# <a name="supporting-dxva-20-in-directshow"></a><span data-ttu-id="7083e-103">Prise en charge de DXVA 2,0 dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="7083e-103">Supporting DXVA 2.0 in DirectShow</span></span>

<span data-ttu-id="7083e-104">Cette rubrique décrit comment prendre en charge DirectX Video Acceleration (DXVA) 2,0 dans un filtre de décodeur DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7083e-104">This topic describes how to support DirectX Video Acceleration (DXVA) 2.0 in a DirectShow decoder filter.</span></span> <span data-ttu-id="7083e-105">Plus précisément, il décrit la communication entre le décodeur et le convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="7083e-105">Specifically, it describes the communication between the decoder and the video renderer.</span></span> <span data-ttu-id="7083e-106">Cette rubrique ne décrit pas comment implémenter le décodage DXVA.</span><span class="sxs-lookup"><span data-stu-id="7083e-106">This topic does not describe how to implement DXVA decoding.</span></span>

-   [<span data-ttu-id="7083e-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="7083e-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="7083e-108">Remarques sur la migration</span><span class="sxs-lookup"><span data-stu-id="7083e-108">Migration Notes</span></span>](#migration-notes)
-   [<span data-ttu-id="7083e-109">Recherche d’une configuration de décodeur</span><span class="sxs-lookup"><span data-stu-id="7083e-109">Finding a Decoder Configuration</span></span>](#finding-a-decoder-configuration)
-   [<span data-ttu-id="7083e-110">Notification du convertisseur vidéo</span><span class="sxs-lookup"><span data-stu-id="7083e-110">Notifying the Video Renderer</span></span>](#notifying-the-video-renderer)
-   [<span data-ttu-id="7083e-111">Allocation de mémoires tampons non compressées</span><span class="sxs-lookup"><span data-stu-id="7083e-111">Allocating Uncompressed Buffers</span></span>](#allocating-uncompressed-buffers)
-   [<span data-ttu-id="7083e-112">Décodage</span><span class="sxs-lookup"><span data-stu-id="7083e-112">Decoding</span></span>](#decoding)
-   [<span data-ttu-id="7083e-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7083e-113">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="7083e-114">Prérequis</span><span class="sxs-lookup"><span data-stu-id="7083e-114">Prerequisites</span></span>

<span data-ttu-id="7083e-115">Cette rubrique suppose que vous êtes familiarisé avec l’écriture de filtres DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7083e-115">This topic assumes that you are familiar with writing DirectShow filters.</span></span> <span data-ttu-id="7083e-116">Pour plus d’informations, consultez la rubrique [écriture de filtres DirectShow](../directshow/writing-directshow-filters.md) dans la documentation du kit de développement logiciel (SDK) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7083e-116">For more information, see the topic [Writing DirectShow Filters](../directshow/writing-directshow-filters.md) in the DirectShow SDK documentation.</span></span> <span data-ttu-id="7083e-117">Les exemples de code de cette rubrique supposent que le filtre de décodeur est dérivé de la classe [**CTransformFilter**](../directshow/ctransformfilter.md) , avec la définition de classe suivante :</span><span class="sxs-lookup"><span data-stu-id="7083e-117">The code examples in this topic assume that the decoder filter is derived from the [**CTransformFilter**](../directshow/ctransformfilter.md) class, with the following class definition:</span></span>


```C++
class CDecoder : public CTransformFilter
{
public:
    static CUnknown* WINAPI CreateInstance(IUnknown *pUnk, HRESULT *pHr);

    HRESULT CompleteConnect(PIN_DIRECTION direction, IPin *pPin);

    HRESULT InitAllocator(IMemAllocator **ppAlloc);
    HRESULT DecideBufferSize(IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp);

    // TODO: The implementations of these methods depend on the specific decoder.
    HRESULT CheckInputType(const CMediaType *mtIn);
    HRESULT CheckTransform(const CMediaType *mtIn, const CMediaType *mtOut);
    HRESULT CTransformFilter::GetMediaType(int,CMediaType *);

private:
    CDecoder(HRESULT *pHr);
    ~CDecoder();

    CBasePin * GetPin(int n);

    HRESULT ConfigureDXVA2(IPin *pPin);
    HRESULT SetEVRForDXVA2(IPin *pPin);

    HRESULT FindDecoderConfiguration(
        /* [in] */  IDirectXVideoDecoderService *pDecoderService,
        /* [in] */  const GUID& guidDecoder, 
        /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
        /* [out] */ BOOL *pbFoundDXVA2Configuration
        );

private:
    IDirectXVideoDecoderService *m_pDecoderService;

    DXVA2_ConfigPictureDecode m_DecoderConfig;
    GUID                      m_DecoderGuid;
    HANDLE                    m_hDevice;

    FOURCC                    m_fccOutputFormat;
};
```



<span data-ttu-id="7083e-118">Dans le reste de cette rubrique, le *décodeur* de terme fait référence au filtre de décodeur, qui reçoit une vidéo compressée et génère des sorties vidéo non compressées.</span><span class="sxs-lookup"><span data-stu-id="7083e-118">In the remainder of this topic, the term *decoder* refers to the decoder filter, which receives compressed video and outputs uncompressed video.</span></span> <span data-ttu-id="7083e-119">L' *appareil décodeur* terme fait référence à un accélérateur vidéo matériel implémenté par le pilote Graphics.</span><span class="sxs-lookup"><span data-stu-id="7083e-119">The term *decoder device* refers to a hardware video accelerator implemented by the graphics driver.</span></span>

<span data-ttu-id="7083e-120">Voici les étapes de base qu’un filtre de décodeur doit effectuer pour prendre en charge DXVA 2,0 :</span><span class="sxs-lookup"><span data-stu-id="7083e-120">Here are the basic steps that a decoder filter must perform to support DXVA 2.0:</span></span>

1.  <span data-ttu-id="7083e-121">Négocier un type de média.</span><span class="sxs-lookup"><span data-stu-id="7083e-121">Negotiate a media type.</span></span>
2.  <span data-ttu-id="7083e-122">Recherchez une configuration de décodeur DXVA.</span><span class="sxs-lookup"><span data-stu-id="7083e-122">Find a DXVA decoder configuration.</span></span>
3.  <span data-ttu-id="7083e-123">Informez le convertisseur vidéo que le décodeur utilise le décodage DXVA.</span><span class="sxs-lookup"><span data-stu-id="7083e-123">Notify the video renderer that the decoder is using DXVA decoding.</span></span>
4.  <span data-ttu-id="7083e-124">Fournissez un allocateur personnalisé qui alloue des surfaces Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7083e-124">Provide a custom allocator that allocates Direct3D surfaces.</span></span>

<span data-ttu-id="7083e-125">Ces étapes sont décrites plus en détail dans le reste de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="7083e-125">These steps are described in more detail in the remainder of this topic.</span></span>

## <a name="migration-notes"></a><span data-ttu-id="7083e-126">Remarques sur la migration</span><span class="sxs-lookup"><span data-stu-id="7083e-126">Migration Notes</span></span>

<span data-ttu-id="7083e-127">Si vous effectuez une migration à partir de DXVA 1,0, vous devez être conscient des différences significatives entre les deux versions :</span><span class="sxs-lookup"><span data-stu-id="7083e-127">If you are migrating from DXVA 1.0, you should be aware of some significant differences between the two versions:</span></span>

-   <span data-ttu-id="7083e-128">DXVA 2,0 n’utilise pas les interfaces [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) et [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) , car le décodeur peut accéder aux API DXVA 2,0 directement par le biais de l’interface [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .</span><span class="sxs-lookup"><span data-stu-id="7083e-128">DXVA 2.0 does not use the [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) and [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) interfaces, because the decoder can access the DXVA 2.0 APIs directly through the [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) interface.</span></span>
-   <span data-ttu-id="7083e-129">Pendant la négociation de type de média, le décodeur n’utilise pas de GUID d’accélération vidéo comme sous-type.</span><span class="sxs-lookup"><span data-stu-id="7083e-129">During media type negotiation, the decoder does not use a video acceleration GUID as the subtype.</span></span> <span data-ttu-id="7083e-130">Au lieu de cela, le sous-type est simplement le format vidéo non compressé (par exemple, NV12), comme avec le décodage logiciel.</span><span class="sxs-lookup"><span data-stu-id="7083e-130">Instead, the subtype is just the uncompressed video format (such as NV12), as with software decoding.</span></span>
-   <span data-ttu-id="7083e-131">La procédure de configuration de l’accélérateur a changé.</span><span class="sxs-lookup"><span data-stu-id="7083e-131">The procedure for configuring the accelerator has changed.</span></span> <span data-ttu-id="7083e-132">Dans DXVA 1,0, les appels du décodeur **s’exécutent** avec une structure **DXVA \_ ConfigPictureDecode** pour configurer accerlator.</span><span class="sxs-lookup"><span data-stu-id="7083e-132">In DXVA 1.0, the decoder calls **Execute** with a **DXVA\_ConfigPictureDecode** structure to configure the accerlator.</span></span> <span data-ttu-id="7083e-133">Dans DXVA 2,0, le décodeur utilise l’interface [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) , comme décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="7083e-133">In DXVA 2.0, the decoder uses the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface, as described in the next section.</span></span>
-   <span data-ttu-id="7083e-134">Le décodeur alloue les mémoires tampons non compressées.</span><span class="sxs-lookup"><span data-stu-id="7083e-134">The decoder allocates the uncompressed buffers.</span></span> <span data-ttu-id="7083e-135">Le convertisseur vidéo ne les alloue plus.</span><span class="sxs-lookup"><span data-stu-id="7083e-135">The video renderer no longer allocates them.</span></span>
-   <span data-ttu-id="7083e-136">Au lieu d’appeler [**IAMVideoAccelerator ::D isplayframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) pour afficher le frame décodé, le décodeur remet le frame au convertisseur en appelant [**IMemInputPin :: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive), comme avec le décodage logiciel.</span><span class="sxs-lookup"><span data-stu-id="7083e-136">Instead of calling [**IAMVideoAccelerator::DisplayFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) to display the decoded frame, the decoder delivers the frame to the renderer by calling [**IMemInputPin::Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive), as with software decoding.</span></span>
-   <span data-ttu-id="7083e-137">Le décodeur n’est plus responsable de la vérification de la sécurité des tampons de données pour les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="7083e-137">The decoder is no longer responsible for checking when data buffers are safe for updates.</span></span> <span data-ttu-id="7083e-138">Par conséquent, DXVA 2,0 n’a pas de méthode équivalente à [**IAMVideoAccelerator :: QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus).</span><span class="sxs-lookup"><span data-stu-id="7083e-138">Therefore DXVA 2.0 does not have any method equivalent to [**IAMVideoAccelerator::QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus).</span></span>
-   <span data-ttu-id="7083e-139">La fusion de sous-image est effectuée par le convertisseur vidéo, à l’aide des API de processeur vidéo DXVA 2.0.</span><span class="sxs-lookup"><span data-stu-id="7083e-139">Subpicture blending is done by the video renderer, using the DXVA2.0 video processor APIs.</span></span> <span data-ttu-id="7083e-140">Les décodeurs qui fournissent des sous-images (par exemple, des décodeurs DVD) doivent envoyer des données de sous-image sur une broche de sortie distincte.</span><span class="sxs-lookup"><span data-stu-id="7083e-140">Decoders that provide subpictures (for example, DVD decoders) should send subpicture data on a separate output pin.</span></span>

<span data-ttu-id="7083e-141">Pour les opérations de décodage, DXVA 2,0 utilise les mêmes structures de données que DXVA 1,0.</span><span class="sxs-lookup"><span data-stu-id="7083e-141">For decoding operations, DXVA 2.0 uses the same data structures as DXVA 1.0.</span></span>

<span data-ttu-id="7083e-142">Le filtre EVR (Enhanced Video Renderer) prend en charge la 2,0 DXVA.</span><span class="sxs-lookup"><span data-stu-id="7083e-142">The enhanced video renderer (EVR) filter supports DXVA 2.0.</span></span> <span data-ttu-id="7083e-143">Les filtres de convertisseur de mixage vidéo (VMR-7 et VMR-9) prennent uniquement en charge DXVA 1,0.</span><span class="sxs-lookup"><span data-stu-id="7083e-143">The Video Mixing Renderer filters (VMR-7 and VMR-9) support DXVA 1.0 only.</span></span>

## <a name="finding-a-decoder-configuration"></a><span data-ttu-id="7083e-144">Recherche d’une configuration de décodeur</span><span class="sxs-lookup"><span data-stu-id="7083e-144">Finding a Decoder Configuration</span></span>

<span data-ttu-id="7083e-145">Une fois que le décodeur a négocié le type de média de sortie, il doit trouver une configuration compatible pour le périphérique décodeur DXVA.</span><span class="sxs-lookup"><span data-stu-id="7083e-145">After the decoder negotiates the output media type, it must find a compatible configuration for the DXVA decoder device.</span></span> <span data-ttu-id="7083e-146">Vous pouvez effectuer cette étape à l’intérieur de la méthode [**CBaseOutputPin :: CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="7083e-146">You can perform this step inside the output pin's [**CBaseOutputPin::CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="7083e-147">Cette étape garantit que le pilote Graphics prend en charge les fonctionnalités requises par le décodeur, avant que le décodeur ne s’engage à utiliser DXVA.</span><span class="sxs-lookup"><span data-stu-id="7083e-147">This step ensures that the graphics driver supports the capabilities needed by the decoder, before the decoder commits to using DXVA.</span></span>

<span data-ttu-id="7083e-148">Pour rechercher une configuration pour l’appareil décodeur, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7083e-148">To find a configuration for the decoder device, do the following:</span></span>

1.  <span data-ttu-id="7083e-149">Interrogez la broche d’entrée du convertisseur pour l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="7083e-149">Query the renderer's input pin for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="7083e-150">Appelez [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) pour obtenir un pointeur vers l’interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .</span><span class="sxs-lookup"><span data-stu-id="7083e-150">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span> <span data-ttu-id="7083e-151">Le GUID du service est \_ un \_ service d’accélération vidéo \_ .</span><span class="sxs-lookup"><span data-stu-id="7083e-151">The service GUID is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>
3.  <span data-ttu-id="7083e-152">Appelez [**IDirect3DDeviceManager9 :: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) pour obtenir un handle sur le périphérique Direct3D du convertisseur.</span><span class="sxs-lookup"><span data-stu-id="7083e-152">Call [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) to get a handle to the renderer's Direct3D device.</span></span>
4.  <span data-ttu-id="7083e-153">Appelez [**IDirect3DDeviceManager9 :: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) et transmettez le descripteur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7083e-153">Call [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) and pass in the device handle.</span></span> <span data-ttu-id="7083e-154">Cette méthode retourne un pointeur vers l’interface [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) .</span><span class="sxs-lookup"><span data-stu-id="7083e-154">This method returns a pointer to the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface.</span></span>
5.  <span data-ttu-id="7083e-155">Appelez [**IDirectXVideoDecoderService :: GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids).</span><span class="sxs-lookup"><span data-stu-id="7083e-155">Call [**IDirectXVideoDecoderService::GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids).</span></span> <span data-ttu-id="7083e-156">Cette méthode retourne un tableau de GUID d’appareil de décodage.</span><span class="sxs-lookup"><span data-stu-id="7083e-156">This method returns an array of decoder device GUIDs.</span></span>
6.  <span data-ttu-id="7083e-157">Parcourez le tableau de GUID de décodeur pour rechercher ceux que le filtre de décodeur prend en charge.</span><span class="sxs-lookup"><span data-stu-id="7083e-157">Loop through the array of decoder GUIDs to find the ones that the decoder filter supports.</span></span> <span data-ttu-id="7083e-158">Par exemple, pour un décodeur MPEG-2, vous devez rechercher **DXVA2 \_ ModeMPEG2 \_ MOCOMP**, **DXVA2 \_ ModeMPEG2 \_ IDCT** ou DXVA2 ModeMPEG2 **\_ \_ VLD**.</span><span class="sxs-lookup"><span data-stu-id="7083e-158">For example, for an MPEG-2 decoder, you would look for **DXVA2\_ModeMPEG2\_MOCOMP**, **DXVA2\_ModeMPEG2\_IDCT**, or **DXVA2\_ModeMPEG2\_VLD**.</span></span>

7.  <span data-ttu-id="7083e-159">Lorsque vous trouvez un GUID d’appareil décodeur candidat, transmettez le GUID à la méthode [**IDirectXVideoDecoderService :: GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) .</span><span class="sxs-lookup"><span data-stu-id="7083e-159">When you find a candidate decoder device GUID, pass the GUID to the [**IDirectXVideoDecoderService::GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) method.</span></span> <span data-ttu-id="7083e-160">Cette méthode retourne un tableau de formats de cible de rendu, spécifiés en tant que valeurs **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="7083e-160">This method returns an array of render target formats, specified as **D3DFORMAT** values.</span></span>
8.  <span data-ttu-id="7083e-161">Parcourez les formats de cible de rendu et recherchez-en un qui correspond à votre format de sortie.</span><span class="sxs-lookup"><span data-stu-id="7083e-161">Loop through the render target formats and look for one that matches your output format.</span></span> <span data-ttu-id="7083e-162">En règle générale, un appareil de décodage prend en charge un format de cible de rendu unique.</span><span class="sxs-lookup"><span data-stu-id="7083e-162">Typically, a decoder device supports a single render target format.</span></span> <span data-ttu-id="7083e-163">Le filtre de décodeur doit se connecter au convertisseur à l’aide de ce sous-type.</span><span class="sxs-lookup"><span data-stu-id="7083e-163">The decoder filter should connect to the renderer using this subtype.</span></span> <span data-ttu-id="7083e-164">Dans le premier appel à [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md), le décodeur peut déterminer le format de la cible de rendu, puis retourner ce format comme type de sortie préféré.</span><span class="sxs-lookup"><span data-stu-id="7083e-164">In the first call to [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md), the decoder can determing the render target format and then return this format as a preferred output type.</span></span>

9.  <span data-ttu-id="7083e-165">Appelez [**IDirectXVideoDecoderService :: GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations).</span><span class="sxs-lookup"><span data-stu-id="7083e-165">Call [**IDirectXVideoDecoderService::GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations).</span></span> <span data-ttu-id="7083e-166">Transmettez le même GUID de périphérique décodeur, ainsi qu’une structure [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) qui décrit le format proposé.</span><span class="sxs-lookup"><span data-stu-id="7083e-166">Pass in the same decoder device GUID, along with a [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure that describes the proposed format.</span></span> <span data-ttu-id="7083e-167">La méthode retourne un tableau de structures [**DXVA2 \_ ConfigPictureDecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) .</span><span class="sxs-lookup"><span data-stu-id="7083e-167">The method returns an array of [**DXVA2\_ConfigPictureDecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) structures.</span></span> <span data-ttu-id="7083e-168">Chaque structure décrit une configuration possible pour l’appareil décodeur.</span><span class="sxs-lookup"><span data-stu-id="7083e-168">Each structure describes one possible configuration for the decoder device.</span></span>

10. <span data-ttu-id="7083e-169">En supposant que les étapes précédentes sont réussies, stockez le descripteur de périphérique Direct3D, le GUID du périphérique décodeur et la structure de configuration.</span><span class="sxs-lookup"><span data-stu-id="7083e-169">Assuming that the previous steps are successful, store the Direct3D device handle, the decoder device GUID, and the configuration structure.</span></span> <span data-ttu-id="7083e-170">Le filtre utilise ces informations pour créer l’appareil de décodage.</span><span class="sxs-lookup"><span data-stu-id="7083e-170">The filter will use this information to create the decoder device.</span></span>

<span data-ttu-id="7083e-171">Le code suivant montre comment rechercher une configuration de décodeur.</span><span class="sxs-lookup"><span data-stu-id="7083e-171">The following code shows how to find a decoder configuration.</span></span>


```C++
HRESULT CDecoder::ConfigureDXVA2(IPin *pPin)
{
    UINT    cDecoderGuids = 0;
    BOOL    bFoundDXVA2Configuration = FALSE;
    GUID    guidDecoder = GUID_NULL;

    DXVA2_ConfigPictureDecode config;
    ZeroMemory(&config, sizeof(config));

    // Variables that follow must be cleaned up at the end.

    IMFGetService               *pGetService = NULL;
    IDirect3DDeviceManager9     *pDeviceManager = NULL;
    IDirectXVideoDecoderService *pDecoderService = NULL;

    GUID   *pDecoderGuids = NULL; // size = cDecoderGuids
    HANDLE hDevice = INVALID_HANDLE_VALUE;

    // Query the pin for IMFGetService.
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pGetService));

    // Get the Direct3D device manager.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(

            MR_VIDEO_ACCELERATION_SERVICE,
            IID_PPV_ARGS(&pDeviceManager)
            );
    }

    // Open a new device handle.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    } 

    // Get the video decoder service.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->GetVideoService(
            hDevice, IID_PPV_ARGS(&pDecoderService));
    }

    // Get the decoder GUIDs.
    if (SUCCEEDED(hr))
    {
        hr = pDecoderService->GetDecoderDeviceGuids(
            &cDecoderGuids, &pDecoderGuids);
    }

    if (SUCCEEDED(hr))
    {
        // Look for the decoder GUIDs we want.
        for (UINT iGuid = 0; iGuid < cDecoderGuids; iGuid++)
        {
            // Do we support this mode?
            if (!IsSupportedDecoderMode(pDecoderGuids[iGuid]))
            {
                continue;
            }

            // Find a configuration that we support. 
            hr = FindDecoderConfiguration(pDecoderService, pDecoderGuids[iGuid],
                &config, &bFoundDXVA2Configuration);
            if (FAILED(hr))
            {
                break;
            }

            if (bFoundDXVA2Configuration)
            {
                // Found a good configuration. Save the GUID and exit the loop.
                guidDecoder = pDecoderGuids[iGuid];
                break;
            }
        }
    }

    if (!bFoundDXVA2Configuration)
    {
        hr = E_FAIL; // Unable to find a configuration.
    }

    if (SUCCEEDED(hr))
    {
        // Store the things we will need later.

        SafeRelease(&m_pDecoderService);
        m_pDecoderService = pDecoderService;
        m_pDecoderService->AddRef();

        m_DecoderConfig = config;
        m_DecoderGuid = guidDecoder;
        m_hDevice = hDevice;
    }

    if (FAILED(hr))
    {
        if (hDevice != INVALID_HANDLE_VALUE)
        {
            pDeviceManager->CloseDeviceHandle(hDevice);
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pDeviceManager);
    SafeRelease(&pDecoderService);
    return hr;
}
HRESULT CDecoder::FindDecoderConfiguration(
    /* [in] */  IDirectXVideoDecoderService *pDecoderService,
    /* [in] */  const GUID& guidDecoder, 
    /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
    /* [out] */ BOOL *pbFoundDXVA2Configuration
    )
{
    HRESULT hr = S_OK;
    UINT cFormats = 0;
    UINT cConfigurations = 0;

    D3DFORMAT                   *pFormats = NULL;     // size = cFormats
    DXVA2_ConfigPictureDecode   *pConfig = NULL;      // size = cConfigurations

    // Find the valid render target formats for this decoder GUID.
    hr = pDecoderService->GetDecoderRenderTargets(
        guidDecoder,
        &cFormats,
        &pFormats
        );

    if (SUCCEEDED(hr))
    {
        // Look for a format that matches our output format.
        for (UINT iFormat = 0; iFormat < cFormats;  iFormat++)
        {
            if (pFormats[iFormat] != (D3DFORMAT)m_fccOutputFormat)
            {
                continue;
            }

            // Fill in the video description. Set the width, height, format, 
            // and frame rate.
            DXVA2_VideoDesc videoDesc = {0};

            FillInVideoDescription(&videoDesc); // Private helper function.
            videoDesc.Format = pFormats[iFormat];

            // Get the available configurations.
            hr = pDecoderService->GetDecoderConfigurations(
                guidDecoder,
                &videoDesc,
                NULL, // Reserved.
                &cConfigurations,
                &pConfig
                );

            if (FAILED(hr))
            {
                break;
            }

            // Find a supported configuration.
            for (UINT iConfig = 0; iConfig < cConfigurations; iConfig++)
            {
                if (IsSupportedDecoderConfig(pConfig[iConfig]))
                {
                    // This configuration is good.
                    *pbFoundDXVA2Configuration = TRUE;
                    *pSelectedConfig = pConfig[iConfig];
                    break;
                }
            }

            CoTaskMemFree(pConfig);
            break;

        } // End of formats loop.
    }

    CoTaskMemFree(pFormats);

    // Note: It is possible to return S_OK without finding a configuration.
    return hr;
}
```



<span data-ttu-id="7083e-172">Comme cet exemple est générique, une partie de la logique a été placée dans des fonctions d’assistance qui doivent être implémentées par le décodeur.</span><span class="sxs-lookup"><span data-stu-id="7083e-172">Because this example is generic, some of the logic has been placed in helper functions that would need to be implemented by the decoder.</span></span> <span data-ttu-id="7083e-173">Le code suivant illustre les déclarations de ces fonctions :</span><span class="sxs-lookup"><span data-stu-id="7083e-173">The following code shows the declarations for these functions:</span></span>


```C++
// Returns TRUE if the decoder supports a given decoding mode.
BOOL IsSupportedDecoderMode(const GUID& mode);

// Returns TRUE if the decoder supports a given decoding configuration.
BOOL IsSupportedDecoderConfig(const DXVA2_ConfigPictureDecode& config);

// Fills in a DXVA2_VideoDesc structure based on the input format.
void FillInVideoDescription(DXVA2_VideoDesc *pDesc);
```



## <a name="notifying-the-video-renderer"></a><span data-ttu-id="7083e-174">Notification du convertisseur vidéo</span><span class="sxs-lookup"><span data-stu-id="7083e-174">Notifying the Video Renderer</span></span>

<span data-ttu-id="7083e-175">Si le décodeur trouve une configuration de décodeur, l’étape suivante consiste à informer le convertisseur vidéo que le décodeur utilisera l’accélération matérielle.</span><span class="sxs-lookup"><span data-stu-id="7083e-175">If the decoder finds a decoder configuration, the next step is to notify the video renderer that the decoder will use hardware acceleration.</span></span> <span data-ttu-id="7083e-176">Vous pouvez effectuer cette étape à l’intérieur de la méthode [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="7083e-176">You can perform this step inside the [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="7083e-177">Cette étape doit se produire avant que l’allocateur soit sélectionné, car il affecte la manière dont l’allocateur est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7083e-177">This step must occur before the allocator is selected, because it affects how the allocator is selected.</span></span>

1.  <span data-ttu-id="7083e-178">Interrogez la broche d’entrée du convertisseur pour l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="7083e-178">Query the renderer's input pin for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="7083e-179">Appelez [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) pour obtenir un pointeur vers l’interface [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) .</span><span class="sxs-lookup"><span data-stu-id="7083e-179">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) interface.</span></span> <span data-ttu-id="7083e-180">Le GUID du service est un **\_ \_ \_ service d’accélération vidéo**.</span><span class="sxs-lookup"><span data-stu-id="7083e-180">The service GUID is **MR\_VIDEO\_ACCELERATION\_SERVICE**.</span></span>
3.  <span data-ttu-id="7083e-181">Appelez [**IDirectXVideoMemoryConfiguration :: GetAvailableSurfaceTypeByIndex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) dans une boucle, en incrémentant la variable *dwTypeIndex* à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="7083e-181">Call [**IDirectXVideoMemoryConfiguration::GetAvailableSurfaceTypeByIndex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) in a loop, incrementing the *dwTypeIndex* variable from zero.</span></span> <span data-ttu-id="7083e-182">S’arrête lorsque la méthode retourne la valeur **DXVA2 \_ SurfaceType \_ DecoderRenderTarget** dans le paramètre *pdwType* .</span><span class="sxs-lookup"><span data-stu-id="7083e-182">Stop when the method returns the value **DXVA2\_SurfaceType\_DecoderRenderTarget** in the *pdwType* parameter.</span></span> <span data-ttu-id="7083e-183">Cette étape permet de s’assurer que le convertisseur vidéo prend en charge le décodage accéléré par le matériel.</span><span class="sxs-lookup"><span data-stu-id="7083e-183">This step ensures that the video renderer supports hardware-accelerated decoding.</span></span> <span data-ttu-id="7083e-184">Cette étape sera toujours effectuée pour le filtre EVR.</span><span class="sxs-lookup"><span data-stu-id="7083e-184">This step will always succeed for the EVR filter.</span></span>
4.  <span data-ttu-id="7083e-185">Si l’étape précédente a réussi, appelez [**IDirectXVideoMemoryConfiguration :: SetSurfaceType**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) avec la valeur DXVA2 \_ SurfaceType \_ DecoderRenderTarget.</span><span class="sxs-lookup"><span data-stu-id="7083e-185">If the previous step succeeded, call [**IDirectXVideoMemoryConfiguration::SetSurfaceType**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) with the value DXVA2\_SurfaceType\_DecoderRenderTarget.</span></span> <span data-ttu-id="7083e-186">L’appel de **SetSurfaceType** avec cette valeur met le convertisseur vidéo en mode DXVA.</span><span class="sxs-lookup"><span data-stu-id="7083e-186">Calling **SetSurfaceType** with this value puts the video renderer into DXVA mode.</span></span> <span data-ttu-id="7083e-187">Quand le convertisseur vidéo est dans ce mode, le décodeur doit fournir son propre allocateur.</span><span class="sxs-lookup"><span data-stu-id="7083e-187">When the video renderer is in this mode, the decoder must provide its own allocator.</span></span>

<span data-ttu-id="7083e-188">Le code suivant montre comment notifier le convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="7083e-188">The following code shows how to notify the video renderer.</span></span>


```C++
HRESULT CDecoder::SetEVRForDXVA2(IPin *pPin)
{
    HRESULT hr = S_OK;

    IMFGetService                       *pGetService = NULL;
    IDirectXVideoMemoryConfiguration    *pVideoConfig = NULL;

    // Query the pin for IMFGetService.
    hr = pPin->QueryInterface(__uuidof(IMFGetService), (void**)&pGetService);

    // Get the IDirectXVideoMemoryConfiguration interface.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(
            MR_VIDEO_ACCELERATION_SERVICE, IID_PPV_ARGS(&pVideoConfig));
    }

    // Notify the EVR. 
    if (SUCCEEDED(hr))
    {
        DXVA2_SurfaceType surfaceType;

        for (DWORD iTypeIndex = 0; ; iTypeIndex++)
        {
            hr = pVideoConfig->GetAvailableSurfaceTypeByIndex(iTypeIndex, &surfaceType);
            
            if (FAILED(hr))
            {
                break;
            }

            if (surfaceType == DXVA2_SurfaceType_DecoderRenderTarget)
            {
                hr = pVideoConfig->SetSurfaceType(DXVA2_SurfaceType_DecoderRenderTarget);
                break;
            }
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pVideoConfig);

    return hr;
}
```



<span data-ttu-id="7083e-189">Si le décodeur trouve une configuration valide et notifie correctement le convertisseur vidéo, le décodeur peut utiliser DXVA pour le décodage.</span><span class="sxs-lookup"><span data-stu-id="7083e-189">If the decoder finds a valid configuration and successfully notifies the video renderer, the decoder can use DXVA for decoding.</span></span> <span data-ttu-id="7083e-190">Le décodeur doit implémenter un allocateur personnalisé pour sa broche de sortie, comme décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="7083e-190">The decoder must implement a custom allocator for its output pin, as described in the next section.</span></span>

## <a name="allocating-uncompressed-buffers"></a><span data-ttu-id="7083e-191">Allocation de mémoires tampons non compressées</span><span class="sxs-lookup"><span data-stu-id="7083e-191">Allocating Uncompressed Buffers</span></span>

<span data-ttu-id="7083e-192">Dans DXVA 2,0, le décodeur est chargé d’allouer des surfaces Direct3D à utiliser comme mémoires tampons vidéo non compressées.</span><span class="sxs-lookup"><span data-stu-id="7083e-192">In DXVA 2.0, the decoder is responsible for allocating Direct3D surfaces to use as uncompressed video buffers.</span></span> <span data-ttu-id="7083e-193">Par conséquent, le décodeur doit implémenter un allocateur personnalisé qui créera les surfaces.</span><span class="sxs-lookup"><span data-stu-id="7083e-193">Therefore, the decoder must implement a custom allocator that will create the surfaces.</span></span> <span data-ttu-id="7083e-194">Les exemples de média fournis par cet allocateur contiennent des pointeurs vers les surfaces Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7083e-194">The media samples provided by this allocator will hold pointers to the Direct3D surfaces.</span></span> <span data-ttu-id="7083e-195">Le EVR récupère un pointeur vers la surface en appelant [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sur l’exemple de média.</span><span class="sxs-lookup"><span data-stu-id="7083e-195">The EVR retrieves a pointer to the surface by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the media sample.</span></span> <span data-ttu-id="7083e-196">L’identificateur de service est **un \_ \_ service de mémoire tampon Mr**.</span><span class="sxs-lookup"><span data-stu-id="7083e-196">The service identifier is **MR\_BUFFER\_SERVICE**.</span></span>

<span data-ttu-id="7083e-197">Pour fournir l’allocateur personnalisé, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7083e-197">To provide the custom allocator, perform the following steps:</span></span>

1.  <span data-ttu-id="7083e-198">Définissez une classe pour les exemples de supports.</span><span class="sxs-lookup"><span data-stu-id="7083e-198">Define a class for the media samples.</span></span> <span data-ttu-id="7083e-199">Cette classe peut dériver de la classe [**CMediaSample**](../directshow/cmediasample.md) .</span><span class="sxs-lookup"><span data-stu-id="7083e-199">This class can derive from the [**CMediaSample**](../directshow/cmediasample.md) class.</span></span> <span data-ttu-id="7083e-200">À l’intérieur de cette classe, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7083e-200">Inside this class, do the following:</span></span>
    -   <span data-ttu-id="7083e-201">Stocke un pointeur vers la surface Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7083e-201">Store a pointer to the Direct3D surface.</span></span>
    -   <span data-ttu-id="7083e-202">Implémentez l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="7083e-202">Implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span> <span data-ttu-id="7083e-203">Dans la méthode [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , si le GUID du service est un **\_ \_ service de mémoire tampon Mr**, interrogez la surface Direct3D pour l’interface demandée.</span><span class="sxs-lookup"><span data-stu-id="7083e-203">In the [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method, if the service GUID is **MR\_BUFFER\_SERVICE**, query the Direct3D surface for the requested interface.</span></span> <span data-ttu-id="7083e-204">Dans le cas contraire, **GetService** peut retourner le **\_ \_ \_ service non pris en charge MF E**.</span><span class="sxs-lookup"><span data-stu-id="7083e-204">Otherwise, **GetService** can return **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
    -   <span data-ttu-id="7083e-205">Substituez la méthode [**CMediaSample :: GetPointer**](../directshow/cmediasample-getpointer.md) pour retourner E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="7083e-205">Override the [**CMediaSample::GetPointer**](../directshow/cmediasample-getpointer.md) method to return E\_NOTIMPL.</span></span>
2.  <span data-ttu-id="7083e-206">Définissez une classe pour l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="7083e-206">Define a class for the allocator.</span></span> <span data-ttu-id="7083e-207">L’allocateur peut dériver de la classe [**CBaseAllocator**](../directshow/cbaseallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="7083e-207">The allocator can derive from the [**CBaseAllocator**](../directshow/cbaseallocator.md) class.</span></span> <span data-ttu-id="7083e-208">Dans cette classe, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="7083e-208">Inside this class, do the following.</span></span>
    -   <span data-ttu-id="7083e-209">Substituez la méthode [**CBaseAllocator :: Alloc**](../directshow/cbaseallocator-alloc.md) .</span><span class="sxs-lookup"><span data-stu-id="7083e-209">Override the [**CBaseAllocator::Alloc**](../directshow/cbaseallocator-alloc.md) method.</span></span> <span data-ttu-id="7083e-210">À l’intérieur de cette méthode, appelez [**IDirectXVideoAccelerationService :: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) pour créer les surfaces.</span><span class="sxs-lookup"><span data-stu-id="7083e-210">Inside this method, call [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) to create the surfaces.</span></span> <span data-ttu-id="7083e-211">(L’interface [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) hérite de cette méthode de [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).)</span><span class="sxs-lookup"><span data-stu-id="7083e-211">(The [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface inherits this method from [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).)</span></span>
    -   <span data-ttu-id="7083e-212">Substituez la méthode [**CBaseAllocator :: Free**](../directshow/cbaseallocator-free.md) pour libérer les surfaces.</span><span class="sxs-lookup"><span data-stu-id="7083e-212">Override the [**CBaseAllocator::Free**](../directshow/cbaseallocator-free.md) method to release the surfaces.</span></span>
3.  <span data-ttu-id="7083e-213">Dans la broche de sortie de votre filtre, remplacez la méthode [**CBaseOutputPin :: InitAllocator**](../directshow/cbaseoutputpin-initallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="7083e-213">In your filter's output pin, override the [**CBaseOutputPin::InitAllocator**](../directshow/cbaseoutputpin-initallocator.md) method.</span></span> <span data-ttu-id="7083e-214">À l’intérieur de cette méthode, créez une instance de votre allocateur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="7083e-214">Inside this method, create an instance of your custom allocator.</span></span>
4.  <span data-ttu-id="7083e-215">Dans votre filtre, implémentez la méthode [**CTransformFilter ::D ecidebuffersize**](../directshow/ctransformfilter-decidebuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="7083e-215">In your filter, implement the [**CTransformFilter::DecideBufferSize**](../directshow/ctransformfilter-decidebuffersize.md) method.</span></span> <span data-ttu-id="7083e-216">Le paramètre *pProperties* indique le nombre de surfaces requises par le EVR.</span><span class="sxs-lookup"><span data-stu-id="7083e-216">The *pProperties* parameter indicates the number of surfaces that the EVR requires.</span></span> <span data-ttu-id="7083e-217">Ajoutez à cette valeur le nombre de surfaces nécessaires à votre décodeur et appelez [**IMemAllocator :: SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) sur l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="7083e-217">Add to this value the number of surfaces that your decoder requires, and call [**IMemAllocator::SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) on the allocator.</span></span>

<span data-ttu-id="7083e-218">Le code suivant montre comment implémenter la classe d’exemple de média :</span><span class="sxs-lookup"><span data-stu-id="7083e-218">The following code shows how to implement the media sample class:</span></span>


```C++
class CDecoderSample : public CMediaSample, public IMFGetService
{
    friend class CDecoderAllocator;

public:

    CDecoderSample(CDecoderAllocator *pAlloc, HRESULT *phr)
        : CMediaSample(NAME("DecoderSample"), (CBaseAllocator*)pAlloc, phr, NULL, 0),
          m_pSurface(NULL),
          m_dwSurfaceId(0)
    { 
    }

    // Note: CMediaSample does not derive from CUnknown, so we cannot use the
    //       DECLARE_IUNKNOWN macro that is used by most of the filter classes.

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        CheckPointer(ppv, E_POINTER);

        if (riid == IID_IMFGetService)
        {
            *ppv = static_cast<IMFGetService*>(this);
            AddRef();
            return S_OK;
        }
        else
        {
            return CMediaSample::QueryInterface(riid, ppv);
        }
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return CMediaSample::AddRef();
    }

    STDMETHODIMP_(ULONG) Release()
    {
        // Return a temporary variable for thread safety.
        ULONG cRef = CMediaSample::Release();
        return cRef;
    }

    // IMFGetService::GetService
    STDMETHODIMP GetService(REFGUID guidService, REFIID riid, LPVOID *ppv)
    {
        if (guidService != MR_BUFFER_SERVICE)
        {
            return MF_E_UNSUPPORTED_SERVICE;
        }
        else if (m_pSurface == NULL)
        {
            return E_NOINTERFACE;
        }
        else
        {
            return m_pSurface->QueryInterface(riid, ppv);
        }
    }

    // Override GetPointer because this class does not manage a system memory buffer.
    // The EVR uses the MR_BUFFER_SERVICE service to get the Direct3D surface.
    STDMETHODIMP GetPointer(BYTE ** ppBuffer)
    {
        return E_NOTIMPL;
    }

private:

    // Sets the pointer to the Direct3D surface. 
    void SetSurface(DWORD surfaceId, IDirect3DSurface9 *pSurf)
    {
        SafeRelease(&m_pSurface);

        m_pSurface = pSurf;
        if (m_pSurface)
        {
            m_pSurface->AddRef();
        }

        m_dwSurfaceId = surfaceId;
    }

    IDirect3DSurface9   *m_pSurface;
    DWORD               m_dwSurfaceId;
};
```



<span data-ttu-id="7083e-219">Le code suivant montre comment implémenter la méthode [**Alloc**](../directshow/cbaseallocator-alloc.md) sur l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="7083e-219">The following code shows how to implement the [**Alloc**](../directshow/cbaseallocator-alloc.md) method on the allocator.</span></span>


```C++
HRESULT CDecoderAllocator::Alloc()
{
    CAutoLock lock(this);

    HRESULT hr = S_OK;

    if (m_pDXVA2Service == NULL)
    {
        return E_UNEXPECTED;
    }

    hr = CBaseAllocator::Alloc();

    // If the requirements have not changed, do not reallocate.
    if (hr == S_FALSE)
    {
        return S_OK;
    }

    if (SUCCEEDED(hr))
    {
        // Free the old resources.
        Free();

        // Allocate a new array of pointers.
        m_ppRTSurfaceArray = new (std::nothrow) IDirect3DSurface9*[m_lCount];
        if (m_ppRTSurfaceArray == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            ZeroMemory(m_ppRTSurfaceArray, sizeof(IDirect3DSurface9*) * m_lCount);
        }
    }

    // Allocate the surfaces.
    if (SUCCEEDED(hr))
    {
        hr = m_pDXVA2Service->CreateSurface(
            m_dwWidth,
            m_dwHeight,
            m_lCount - 1,
            (D3DFORMAT)m_dwFormat,
            D3DPOOL_DEFAULT,
            0,
            DXVA2_VideoDecoderRenderTarget,
            m_ppRTSurfaceArray,
            NULL
            );
    }

    if (SUCCEEDED(hr))
    {
        for (m_lAllocated = 0; m_lAllocated < m_lCount; m_lAllocated++)
        {
            CDecoderSample *pSample = new (std::nothrow) CDecoderSample(this, &hr);

            if (pSample == NULL)
            {
                hr = E_OUTOFMEMORY;
                break;
            }
            if (FAILED(hr))
            {
                break;
            }
            // Assign the Direct3D surface pointer and the index.
            pSample->SetSurface(m_lAllocated, m_ppRTSurfaceArray[m_lAllocated]);

            // Add to the sample list.
            m_lFree.Add(pSample);
        }
    }

    if (SUCCEEDED(hr))
    {
        m_bChanged = FALSE;
    }
    return hr;
}
```



<span data-ttu-id="7083e-220">Voici le code de la méthode [**Free**](../directshow/cbaseallocator-free.md) :</span><span class="sxs-lookup"><span data-stu-id="7083e-220">Here is the code for the [**Free**](../directshow/cbaseallocator-free.md) method:</span></span>


```C++
void CDecoderAllocator::Free()
{
    CMediaSample *pSample = NULL;

    do
    {
        pSample = m_lFree.RemoveHead();
        if (pSample)
        {
            delete pSample;
        }
    } while (pSample);

    if (m_ppRTSurfaceArray)
    {
        for (long i = 0; i < m_lAllocated; i++)
        {
            SafeRelease(&m_ppRTSurfaceArray[i]);
        }

        delete [] m_ppRTSurfaceArray;
    }
    m_lAllocated = 0;
}
```



<span data-ttu-id="7083e-221">Pour plus d’informations sur l’implémentation d’allocators personnalisés, consultez la rubrique [fournissant un allocateur personnalisé](../directshow/providing-a-custom-allocator.md) dans la documentation du kit de développement logiciel (SDK) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7083e-221">For more information about implementing custom allocators, see the topic [Providing a Custom Allocator](../directshow/providing-a-custom-allocator.md) in the DirectShow SDK documentation.</span></span>

## <a name="decoding"></a><span data-ttu-id="7083e-222">Décodage</span><span class="sxs-lookup"><span data-stu-id="7083e-222">Decoding</span></span>

<span data-ttu-id="7083e-223">Pour créer l’appareil de décodage, appelez [**IDirectXVideoDecoderService :: CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder).</span><span class="sxs-lookup"><span data-stu-id="7083e-223">To create the decoder device, call [**IDirectXVideoDecoderService::CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder).</span></span> <span data-ttu-id="7083e-224">La méthode retourne un pointeur vers l’interface [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) de l’appareil décodeur.</span><span class="sxs-lookup"><span data-stu-id="7083e-224">The method returns a pointer to the [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) interface of the decoder device.</span></span>

<span data-ttu-id="7083e-225">Sur chaque frame, appelez [**IDirect3DDeviceManager9 :: TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) pour tester le handle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7083e-225">On each frame, call [**IDirect3DDeviceManager9::TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) to test the device handle.</span></span> <span data-ttu-id="7083e-226">Si l’appareil a changé, la méthode retourne DXVA2 \_ E \_ New \_ Video \_ Device.</span><span class="sxs-lookup"><span data-stu-id="7083e-226">If the device has changed, the method returns DXVA2\_E\_NEW\_VIDEO\_DEVICE.</span></span> <span data-ttu-id="7083e-227">Si cela se produit, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7083e-227">If this occurs, do the following:</span></span>

1.  <span data-ttu-id="7083e-228">Fermez le handle d’appareil en appelant [**IDirect3DDeviceManager9 :: CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).</span><span class="sxs-lookup"><span data-stu-id="7083e-228">Close the device handle by calling [**IDirect3DDeviceManager9::CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).</span></span>
2.  <span data-ttu-id="7083e-229">Libérez les pointeurs [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) et [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .</span><span class="sxs-lookup"><span data-stu-id="7083e-229">Release the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) and [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) pointers.</span></span>
3.  <span data-ttu-id="7083e-230">Ouvrez un nouveau descripteur d’appareil.</span><span class="sxs-lookup"><span data-stu-id="7083e-230">Open a new device handle.</span></span>
4.  <span data-ttu-id="7083e-231">Négocier une nouvelle configuration de décodeur, comme décrit dans la section [recherche d’une configuration de décodeur](#finding-a-decoder-configuration).</span><span class="sxs-lookup"><span data-stu-id="7083e-231">Negotiate a new decoder configuration, as described in the section [Finding a Decoder Configuration](#finding-a-decoder-configuration).</span></span>
5.  <span data-ttu-id="7083e-232">Créez un appareil de décodage.</span><span class="sxs-lookup"><span data-stu-id="7083e-232">Create a new decoder device.</span></span>

<span data-ttu-id="7083e-233">En supposant que le descripteur de l’appareil est valide, le processus de décodage fonctionne comme suit :</span><span class="sxs-lookup"><span data-stu-id="7083e-233">Assuming that the device handle is valid, the decoding process works as follows:</span></span>

1.  <span data-ttu-id="7083e-234">Appelez [**IDirectXVideoDecoder :: BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).</span><span class="sxs-lookup"><span data-stu-id="7083e-234">Call [**IDirectXVideoDecoder::BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).</span></span>
2.  <span data-ttu-id="7083e-235">Effectuez les opérations suivantes une ou plusieurs fois :</span><span class="sxs-lookup"><span data-stu-id="7083e-235">Do the following one or more times:</span></span>
    1.  <span data-ttu-id="7083e-236">Appelez [**IDirectXVideoDecoder :: GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) pour obtenir une mémoire tampon de décodeur DXVA.</span><span class="sxs-lookup"><span data-stu-id="7083e-236">Call [**IDirectXVideoDecoder::GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) to get a DXVA decoder buffer.</span></span>
    2.  <span data-ttu-id="7083e-237">Remplir la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7083e-237">Fill the buffer.</span></span>
    3.  <span data-ttu-id="7083e-238">Appelez [**IDirectXVideoDecoder :: ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).</span><span class="sxs-lookup"><span data-stu-id="7083e-238">Call [**IDirectXVideoDecoder::ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).</span></span>
3.  <span data-ttu-id="7083e-239">Appelez [**IDirectXVideoDecoder :: Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) pour effectuer les opérations de décodage sur le frame.</span><span class="sxs-lookup"><span data-stu-id="7083e-239">Call [**IDirectXVideoDecoder::Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) to perform the decoding operations on the frame.</span></span>

<span data-ttu-id="7083e-240">DXVA 2,0 utilise les mêmes structures de données que DXVA 1,0 pour les opérations de décodage.</span><span class="sxs-lookup"><span data-stu-id="7083e-240">DXVA 2.0 uses the same data structures as DXVA 1.0 for decoding operations.</span></span> <span data-ttu-id="7083e-241">Pour l’ensemble initial de profils DXVA (pour H. 261, H. 263 et MPEG-2), ces structures de données sont décrites dans la [spécification DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).</span><span class="sxs-lookup"><span data-stu-id="7083e-241">For the original set of DXVA profiles (for H.261, H.263, and MPEG-2), these data structures are described in the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

<span data-ttu-id="7083e-242">Au sein de chaque paire d’appels [**BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe) / [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) , vous pouvez appeler [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) plusieurs fois, mais une seule fois pour chaque type de mémoire tampon DXVA.</span><span class="sxs-lookup"><span data-stu-id="7083e-242">Within each pair of [**BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)/[**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) calls, you may call [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) multiple times, but only once for each type of DXVA buffer.</span></span> <span data-ttu-id="7083e-243">Si vous l’appelez deux fois avec le même type de mémoire tampon, vous allez remplacer les données.</span><span class="sxs-lookup"><span data-stu-id="7083e-243">If you call it twice with the same buffer type, you will overwrite the data.</span></span>

<span data-ttu-id="7083e-244">Après l’appel de l' [**instruction EXECUTE**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute), appelez [**IMemInputPin :: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) pour remettre le frame au convertisseur vidéo, comme avec le décodage logiciel.</span><span class="sxs-lookup"><span data-stu-id="7083e-244">After calling [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute), call [**IMemInputPin::Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) to deliver the frame to the video renderer, as with software decoding.</span></span> <span data-ttu-id="7083e-245">La méthode **Receive** est asynchrone ; une fois retourné, le décodeur peut continuer à décoder le frame suivant.</span><span class="sxs-lookup"><span data-stu-id="7083e-245">The **Receive** method is asynchronous; after it returns, the decoder can continue decoding the next frame.</span></span> <span data-ttu-id="7083e-246">Le pilote d’affichage empêche les commandes de décodage de remplacer la mémoire tampon pendant que la mémoire tampon est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="7083e-246">The display driver prevents any decoding commands from overwriting the buffer while the buffer is in use.</span></span> <span data-ttu-id="7083e-247">Le décodeur ne doit pas réutiliser une surface pour décoder une autre image tant que le convertisseur n’a pas libéré l’exemple.</span><span class="sxs-lookup"><span data-stu-id="7083e-247">The decoder should not reuse a surface to decode another frame until the renderer has released the sample.</span></span> <span data-ttu-id="7083e-248">Quand le convertisseur libère l’exemple, l’allocateur remet l’échantillon dans son pool d’exemples disponibles.</span><span class="sxs-lookup"><span data-stu-id="7083e-248">When the renderer releases the sample, the allocator puts the sample back into its pool of available samples.</span></span> <span data-ttu-id="7083e-249">Pour accéder à l’exemple disponible suivant, appelez [**CBaseOutputPin :: GetDeliveryBuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md), qui à son tour appelle [**IMemAllocator :: GetBuffer**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer).</span><span class="sxs-lookup"><span data-stu-id="7083e-249">To get the next available sample, call [**CBaseOutputPin::GetDeliveryBuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md), which in turn calls [**IMemAllocator::GetBuffer**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer).</span></span> <span data-ttu-id="7083e-250">Pour plus d’informations, consultez la rubrique [vue d’ensemble du Data Flow dans DirectShow](../directshow/overview-of-data-flow-in-directshow.md) dans la documentation DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7083e-250">For more information, see the topic [Overview of Data Flow in DirectShow](../directshow/overview-of-data-flow-in-directshow.md) in the DirectShow documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7083e-251">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7083e-251">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7083e-252">Accélération vidéo DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="7083e-252">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
