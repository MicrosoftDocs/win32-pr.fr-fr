---
description: Pour convertir des fichiers multimédias au format ASF, vous pouvez utiliser les encodeurs Windows Media. En savoir plus sur la création d’un encodeur à l’aide de CoCreateInstance.
ms.assetid: 96f19dfb-a328-41db-8fa8-77f052b1a192
title: Création d’un encodeur à l’aide de CoCreateInstance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c4cdf7b72bbfee97031088502113d085738981
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068465"
---
# <a name="creating-an-encoder-by-using-cocreateinstance"></a><span data-ttu-id="bc499-104">Création d’un encodeur à l’aide de CoCreateInstance</span><span class="sxs-lookup"><span data-stu-id="bc499-104">Creating an Encoder by Using CoCreateInstance</span></span>

<span data-ttu-id="bc499-105">Pour convertir des fichiers multimédias au format ASF, vous pouvez utiliser les encodeurs Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bc499-105">For converting media files into ASF format, you can use Windows Media encoders.</span></span> <span data-ttu-id="bc499-106">Pour utiliser ces encodeurs, ceux-ci doivent être inscrits auprès du système.</span><span class="sxs-lookup"><span data-stu-id="bc499-106">To use these encoders, they must be registered with the system.</span></span> <span data-ttu-id="bc499-107">Les encodeurs sont implémentés en tant que [Media Foundation transformations](media-foundation-transforms.md) (MFTS) et doivent exposer l’interface IMFTransform.</span><span class="sxs-lookup"><span data-stu-id="bc499-107">Encoders are implemented as [Media Foundation transforms](media-foundation-transforms.md) (MFTs) and must expose the IMFTransform interface.</span></span> <span data-ttu-id="bc499-108">Cette rubrique décrit comment une application peut obtenir un pointeur vers l’interface IMFTransform de l’encodeur MFT nécessaire et l’instancier pour l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="bc499-108">This topic describes how an application can get a pointer to the required MFT encoder's IMFTransform interface and instantiate it for use.</span></span>

<span data-ttu-id="bc499-109">Pour plus d’informations sur l’inscription de l’encodeur, consultez [instanciation d’un encodeur MFT](instantiating-the-encoder-mft.md).</span><span class="sxs-lookup"><span data-stu-id="bc499-109">For information about encoder registration, see [Instantiating an Encoder MFT](instantiating-the-encoder-mft.md).</span></span>

-   [<span data-ttu-id="bc499-110">Utilisation de l’interface IMFTransform d’un encodeur</span><span class="sxs-lookup"><span data-stu-id="bc499-110">Using an Encoder's IMFTransform Interface</span></span>](#creating-an-encoder-by-using-cocreateinstance)
    -   [<span data-ttu-id="bc499-111">Exemple de création d’encodeur</span><span class="sxs-lookup"><span data-stu-id="bc499-111">Encoder Creation Example</span></span>](#encoder-creation-example)
-   [<span data-ttu-id="bc499-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc499-112">Related topics</span></span>](#related-topics)

## <a name="using-an-encoders-imftransform-interface"></a><span data-ttu-id="bc499-113">Utilisation de l’interface IMFTransform d’un encodeur</span><span class="sxs-lookup"><span data-stu-id="bc499-113">Using an Encoder's IMFTransform Interface</span></span>

<span data-ttu-id="bc499-114">Une fois l’inscription des encodeurs Windows Media avec le système terminée, une application peut énumérer les encodeurs en appelant [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum).</span><span class="sxs-lookup"><span data-stu-id="bc499-114">Upon successful registration of Windows Media encoders with the system, an application can enumerate the encoders by calling [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum).</span></span> <span data-ttu-id="bc499-115">Pour Rechercher l’encodeur approprié, vous devez spécifier les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="bc499-115">To search for the right encoder, you must specify the following:</span></span>

-   <span data-ttu-id="bc499-116">GUID qui représente la catégorie, qui est soit l' **\_ \_ \_ encodeur audio de catégorie MFT** , soit l' **\_ \_ \_ encodeur vidéo de catégorie MFT**.</span><span class="sxs-lookup"><span data-stu-id="bc499-116">The GUID that represents the category, which is either **MFT\_CATEGORY\_AUDIO\_ENCODER** or **MFT\_CATEGORY\_VIDEO\_ENCODER**.</span></span>

-   <span data-ttu-id="bc499-117">Format à mettre en correspondance.</span><span class="sxs-lookup"><span data-stu-id="bc499-117">The format to match.</span></span> <span data-ttu-id="bc499-118">Cela est défini dans la structure d' [**\_ \_ \_ informations sur le type de Registre MFT**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) qui spécifie le type et le sous-type principaux du type de média dans lequel l’encodeur génère des échantillons.</span><span class="sxs-lookup"><span data-stu-id="bc499-118">This is set in the [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structure that specifies the major type and subtype of the media type that the encoder will generate samples in.</span></span> <span data-ttu-id="bc499-119">Cette structure est passée dans le paramètre *pOutputType* .</span><span class="sxs-lookup"><span data-stu-id="bc499-119">This structure is passed in the *pOutputType* parameter.</span></span> <span data-ttu-id="bc499-120">Pour plus d’informations sur les types pris en charge, consultez [GUID type Media](media-type-guids.md).</span><span class="sxs-lookup"><span data-stu-id="bc499-120">For information about the supported types, see [Media Type GUIDs](media-type-guids.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="bc499-121">Les informations de type d’entrée dans le paramètre *pInputType* ne sont pas requises.</span><span class="sxs-lookup"><span data-stu-id="bc499-121">The input type information in the *pInputType* parameter is not required.</span></span> <span data-ttu-id="bc499-122">Cela est dû au fait que le type d’entrée est connu de l’application et que l’encodeur s’attend à ce que le flux d’entrée soit dans un format non compressé.</span><span class="sxs-lookup"><span data-stu-id="bc499-122">This is because the input type is known to the application and the encoder expects the input stream to be in an uncompressed format.</span></span>

     

<span data-ttu-id="bc499-123">[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) retourne un tableau de pointeurs [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pour le MFTS d’encodeur qui correspondent aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="bc499-123">[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) returns an array of [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointers for the encoder MFTs that match the search criteria.</span></span> <span data-ttu-id="bc499-124">Vous pouvez instancier un encodeur en appelant la fonction COM **CoCreateInstance** et en passant le CLSID de l’encodeur que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="bc499-124">You can instantiate an encoder by calling the COM function **CoCreateInstance** and passing the CLSID of the encoder you want to use.</span></span> <span data-ttu-id="bc499-125">Cette fonction retourne un pointeur vers l’interface **IMFTransform** qui représente l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="bc499-125">This function returns a pointer to the **IMFTransform** interface that represents the encoder.</span></span> <span data-ttu-id="bc499-126">Pour plus d’informations sur cet appel de fonction, consultez la documentation SDK Windows pour le modèle COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="bc499-126">For more information about this function call, see the Windows SDK documentation for the Component Object Model (COM).</span></span>

### <a name="encoder-creation-example"></a><span data-ttu-id="bc499-127">Exemple de création d’encodeur</span><span class="sxs-lookup"><span data-stu-id="bc499-127">Encoder Creation Example</span></span>

<span data-ttu-id="bc499-128">L’exemple de code suivant montre comment créer un encodeur audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="bc499-128">The following code example shows how to create an audio or video encoder.</span></span>


```C++
HRESULT FindEncoder(
    const GUID& subtype, 
    BOOL bAudio, 
    IMFTransform **ppEncoder
    )
{
    HRESULT hr = S_OK;
    UINT32 count = 0;

    CLSID *ppCLSIDs = NULL;

    MFT_REGISTER_TYPE_INFO info = { 0 };

    info.guidMajorType = bAudio ? MFMediaType_Audio : MFMediaType_Video;
    info.guidSubtype = subtype;

    hr = MFTEnum(   
        bAudio ? MFT_CATEGORY_AUDIO_ENCODER : MFT_CATEGORY_VIDEO_ENCODER,
        0,          // Reserved
        NULL,       // Input type
        &info,      // Output type
        NULL,       // Reserved
        &ppCLSIDs,
        &count
        );

    if (SUCCEEDED(hr) && count == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
    }

    // Create the first encoder in the list.

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(ppCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(ppEncoder));
    }

    CoTaskMemFree(ppCLSIDs);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="bc499-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc499-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc499-130">Instanciation d’une table MFT d’encodeur</span><span class="sxs-lookup"><span data-stu-id="bc499-130">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="bc499-131">Encodeurs Windows Media</span><span class="sxs-lookup"><span data-stu-id="bc499-131">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



