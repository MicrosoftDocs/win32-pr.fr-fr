---
description: Définition d’un type de sortie pour un encodeur WMA
ms.assetid: 0a1a22bb-460f-4ac2-be76-4249997441de
title: Définition d’un type de sortie pour un encodeur WMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6b078dc2426b062a90f706c5d113960f54ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111846"
---
# <a name="setting-an-output-type-for-a-wma-encoder"></a><span data-ttu-id="9db3f-103">Définition d’un type de sortie pour un encodeur WMA</span><span class="sxs-lookup"><span data-stu-id="9db3f-103">Setting an Output Type for a WMA Encoder</span></span>

<span data-ttu-id="9db3f-104">Pour créer un type de sortie valide pour un encodeur Windows Media Audio (WMA), vous devez disposer des informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9db3f-104">To create a valid output type for a Windows Media Audio (WMA) encoder, you must have the following information:</span></span>

-   <span data-ttu-id="9db3f-105">Sous-type audio qui repesents le format WMA encodé.</span><span class="sxs-lookup"><span data-stu-id="9db3f-105">The audio subtype that repesents the encoded WMA format.</span></span> <span data-ttu-id="9db3f-106">Consultez [GUID de sous-type audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="9db3f-106">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>
-   <span data-ttu-id="9db3f-107">Propriétés de configuration à définir sur l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="9db3f-107">The configuration properties to set on the encoder.</span></span>

    <span data-ttu-id="9db3f-108">Les propriétés de configuration sont documentées dans la documentation Windows Media Audio et le codec vidéo et les API DSP.</span><span class="sxs-lookup"><span data-stu-id="9db3f-108">The configuration properties are documented in the Windows Media Audio and Video Codec and DSP APIs documentation.</span></span> <span data-ttu-id="9db3f-109">Pour plus d’informations, consultez « Propriétés des flux audio » dans [Propriétés de codage](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="9db3f-109">For more information, see "Audio Stream Properties" in [Encoding Properties](configuring-the-encoder.md).</span></span>

### <a name="windows-vista-or-later"></a><span data-ttu-id="9db3f-110">Windows Vista ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9db3f-110">Windows Vista or Later</span></span>

<span data-ttu-id="9db3f-111">Pour obtenir un type de sortie valide pour l’encodeur, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="9db3f-111">To get a valid output type for the encoder, perform the following steps.</span></span>

1.  <span data-ttu-id="9db3f-112">Utilisez la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) ou [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) pour créer une instance de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="9db3f-112">Use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function to create an instance of the encoder.</span></span>
2.  <span data-ttu-id="9db3f-113">Interrogez l’encodeur pour l’interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="9db3f-113">Query the encoder for the **IPropertyStore** interface.</span></span>
3.  <span data-ttu-id="9db3f-114">Utilisez l’interface **IPropertyStore** pour configurer l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="9db3f-114">Use the **IPropertyStore** interface to configure the encoder.</span></span>
4.  <span data-ttu-id="9db3f-115">Récupérez les types de sortie pris en charge en appelant [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) dans une boucle jusqu’à ce que l’encodeur retourne **MF E plus de \_ \_ \_ \_ types** et que vous choisissiez le type de média cible.</span><span class="sxs-lookup"><span data-stu-id="9db3f-115">Retrieve the supported output types by calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) in a loop until the encoder returns **MF\_E\_NO\_MORE\_TYPES** and you choose the target media type.</span></span> <span data-ttu-id="9db3f-116">I</span><span class="sxs-lookup"><span data-stu-id="9db3f-116">I</span></span>
5.  <span data-ttu-id="9db3f-117">Appelez [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) pour définir le type de support de compression sur l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="9db3f-117">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

### <a name="windows-7"></a><span data-ttu-id="9db3f-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9db3f-118">Windows 7</span></span>

<span data-ttu-id="9db3f-119">Pour obtenir un type de sortie valide pour l’encodeur dans Windows 7, Media Foundation fournit la fonction [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) .</span><span class="sxs-lookup"><span data-stu-id="9db3f-119">To get a valid output type for the encoder in Windows 7, Media Foundation provides the [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) function.</span></span> <span data-ttu-id="9db3f-120">Une application doit passer le sous-type audio qui repesents le WMA encodé et les propriétés d’encodage.</span><span class="sxs-lookup"><span data-stu-id="9db3f-120">An application must pass required the audio subtype that repesents the encoded WMA and the encoding properties.</span></span> <span data-ttu-id="9db3f-121">Les propriétés sont obligatoires, car l’encodeur modifie les types de sortie pris en charge en fonction du mode défini.</span><span class="sxs-lookup"><span data-stu-id="9db3f-121">The properties are required because the encoder changes the supported output types depending upon the mode set.</span></span>

> [!Note]  
> <span data-ttu-id="9db3f-122">[**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)est uniquement pris en charge pour un [encodage à vitesse binaire constante](constant-bit-rate-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="9db3f-122">[**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)is only supported for [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span>

 

<span data-ttu-id="9db3f-123">Si l’appel s’effectue correctement, l’application reçoit une liste de pointeurs IUnknown des types de supports de sortie pris en charge dans un objet [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) .</span><span class="sxs-lookup"><span data-stu-id="9db3f-123">If the call succeeds, the application receives a list of IUnknown pointers of the supported output media types in an [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) object.</span></span> <span data-ttu-id="9db3f-124">Pour définir le type de média de sortie, recherchez celui qui correspond à votre type cible et appelez [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) pour définir le type de support de compression sur l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="9db3f-124">To set the output media type, find the one that matches your target type and call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9db3f-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9db3f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9db3f-126">Instanciation d’une table MFT d’encodeur</span><span class="sxs-lookup"><span data-stu-id="9db3f-126">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="9db3f-127">Encodeurs Windows Media</span><span class="sxs-lookup"><span data-stu-id="9db3f-127">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



