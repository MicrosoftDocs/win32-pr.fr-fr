---
description: Un encodeur écrit des données image dans un flux. Les encodeurs peuvent compresser, chiffrer et modifier les pixels de l’image de plusieurs manières avant de les écrire dans le flux.
ms.assetid: e1e3a9d9-209b-46a6-92da-5570476507cf
title: Vue d’ensemble de l’encodage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be46aa73082071deb69fdd402f42866b18ef0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210286"
---
# <a name="encoding-overview"></a><span data-ttu-id="aae5a-104">Vue d’ensemble de l’encodage</span><span class="sxs-lookup"><span data-stu-id="aae5a-104">Encoding Overview</span></span>

<span data-ttu-id="aae5a-105">Un encodeur écrit des données image dans un flux.</span><span class="sxs-lookup"><span data-stu-id="aae5a-105">An encoder writes image data to a stream.</span></span> <span data-ttu-id="aae5a-106">Les encodeurs peuvent compresser, chiffrer et modifier les pixels de l’image de plusieurs manières avant de les écrire dans le flux.</span><span class="sxs-lookup"><span data-stu-id="aae5a-106">Encoders can compress, encrypt, and alter the image pixels in a number of ways prior to writing them to the stream.</span></span> <span data-ttu-id="aae5a-107">L’utilisation de certains encodeurs donne lieu à des compromis, par exemple JPEG, qui contourne les informations de couleur pour une meilleure compression.</span><span class="sxs-lookup"><span data-stu-id="aae5a-107">Using some encoders results in tradeoffs—for example, JPEG, which trades off color information for better compression.</span></span> <span data-ttu-id="aae5a-108">Les autres encodeurs n’entraînent pas de telles pertes, par exemple bitmap (BMP).</span><span class="sxs-lookup"><span data-stu-id="aae5a-108">Other encoders do not result in such losses—for example, bitmap (BMP).</span></span> <span data-ttu-id="aae5a-109">Étant donné que de nombreux codecs utilisent la technologie propriétaire pour obtenir une meilleure compression et une meilleure fidélité des images, les détails sur la façon dont une image est encodée sont ceux du développeur du codec.</span><span class="sxs-lookup"><span data-stu-id="aae5a-109">Because many codecs use proprietary technology to achieve better compression and image fidelity, the details on how an image gets encoded are up to the codec developer.</span></span>

<span data-ttu-id="aae5a-110">Cette rubrique comprend les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="aae5a-110">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="aae5a-111">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="aae5a-111">IWICBitmapEncoder</span></span>](#iwicbitmapencoder)
-   [<span data-ttu-id="aae5a-112">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="aae5a-112">IWICBitmapFrameEncode</span></span>](#iwicbitmapframeencode)
-   [<span data-ttu-id="aae5a-113">Exemple d’encodage TIFF</span><span class="sxs-lookup"><span data-stu-id="aae5a-113">TIFF Encoding Example</span></span>](#tiff-encoding-example)
-   [<span data-ttu-id="aae5a-114">Utilisation des options d’encodeur</span><span class="sxs-lookup"><span data-stu-id="aae5a-114">Encoder Options Usage</span></span>](#encoder-options-usage)
-   [<span data-ttu-id="aae5a-115">Options de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="aae5a-115">Encoder Options</span></span>](#encoder-options-usage)
-   [<span data-ttu-id="aae5a-116">Exemples d’options d’encodeur</span><span class="sxs-lookup"><span data-stu-id="aae5a-116">Encoder Options Examples</span></span>](#encoder-options-examples)
-   [<span data-ttu-id="aae5a-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aae5a-117">Related topics</span></span>](#related-topics)

## <a name="iwicbitmapencoder"></a><span data-ttu-id="aae5a-118">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="aae5a-118">IWICBitmapEncoder</span></span>

<span data-ttu-id="aae5a-119">[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) est l’interface principale pour l’encodage d’une image au format cible et utilisée pour sérialiser les composants d’une image, tels que thumbnail ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) et frames ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), dans le fichier image.</span><span class="sxs-lookup"><span data-stu-id="aae5a-119">[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) is the main interface for encoding an image to the target format and used to serialize an image's components, such as thumbnail ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) and frames ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), to the image file.</span></span>

<span data-ttu-id="aae5a-120">La façon dont et quand la sérialisation se produit est laissée au développeur du codec.</span><span class="sxs-lookup"><span data-stu-id="aae5a-120">How and when serialization occurs is left up to the codec developer.</span></span> <span data-ttu-id="aae5a-121">Chaque bloc de données individuel dans le format de fichier cible doit pouvoir être défini indépendamment de l’ordre, mais là encore, il s’agit de la décision du développeur de codec.</span><span class="sxs-lookup"><span data-stu-id="aae5a-121">Each individual block of data within the target file format should be able to set independent of order, but again, this is the codec developer's decision.</span></span> <span data-ttu-id="aae5a-122">Une fois la méthode [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) appelée, les modifications apportées à l’image ne doivent pas être autorisées et le flux doit être fermé.</span><span class="sxs-lookup"><span data-stu-id="aae5a-122">Once the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) method is called however, changes to the image should not be allowed and the stream should be closed.</span></span>

## <a name="iwicbitmapframeencode"></a><span data-ttu-id="aae5a-123">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="aae5a-123">IWICBitmapFrameEncode</span></span>

<span data-ttu-id="aae5a-124">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) est l’interface pour l’encodage des frames individuels d’une image.</span><span class="sxs-lookup"><span data-stu-id="aae5a-124">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) is the interface for encoding the individual frames of an image.</span></span> <span data-ttu-id="aae5a-125">Il fournit des méthodes pour définir des composants d’image de frame individuels, tels que des miniatures et des images, ainsi que des dimensions d’image, des PPP et des formats de pixel.</span><span class="sxs-lookup"><span data-stu-id="aae5a-125">It provides methods for setting individual frame imaging components, such as thumbnails and frames, as well as image dimensions, DPI, and pixel formats.</span></span>

<span data-ttu-id="aae5a-126">Des frames individuels peuvent être encodés avec des métadonnées propres au frame afin que [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) donne accès à un enregistreur de métadonnées via la méthode [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="aae5a-126">Individual frames may be encoded with frame-specific metadata so [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) provides access to a metadata writer through the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

<span data-ttu-id="aae5a-127">La méthode [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) du frame valide toutes les modifications apportées au frame individuel et indique que les modifications apportées à ce frame ne doivent plus être acceptées.</span><span class="sxs-lookup"><span data-stu-id="aae5a-127">The frame's [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method commits all changes to the individual frame and indicates that changes to that frame should no longer be accepted.</span></span>

## <a name="tiff-encoding-example"></a><span data-ttu-id="aae5a-128">Exemple d’encodage TIFF</span><span class="sxs-lookup"><span data-stu-id="aae5a-128">TIFF Encoding Example</span></span>

<span data-ttu-id="aae5a-129">Dans l’exemple suivant, une image TIFF (Tagged Image File Format) est encodée à l’aide de [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) et d’un [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span><span class="sxs-lookup"><span data-stu-id="aae5a-129">In the following example, a Tagged Image File Format (TIFF) image is encoded using [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) and an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span></span> <span data-ttu-id="aae5a-130">La sortie TIFF est personnalisée à l’aide de [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) et le frame bitmap est initialisé à l’aide des options données.</span><span class="sxs-lookup"><span data-stu-id="aae5a-130">The TIFF output is customized using the [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) and the bitmap frame is initialized using the given options.</span></span> <span data-ttu-id="aae5a-131">Une fois que l’image a été créée à l’aide de [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), la trame est validée au moyen de la [**validation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) et l’image est enregistrée à l’aide de la [**validation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).</span><span class="sxs-lookup"><span data-stu-id="aae5a-131">Once the image has been created using [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), the frame is committed by way of [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) and the image is saved using [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).</span></span>


```C++
IWICImagingFactory *piFactory = NULL;
IWICBitmapEncoder *piEncoder = NULL;
IWICBitmapFrameEncode *piBitmapFrame = NULL;
IPropertyBag2 *pPropertybag = NULL;

IWICStream *piStream = NULL;
UINT uiWidth = 640;
UINT uiHeight = 480;

HRESULT hr = CoCreateInstance(
                CLSID_WICImagingFactory,
                NULL,
                CLSCTX_INPROC_SERVER,
                IID_IWICImagingFactory,
                (LPVOID*) &piFactory);

if (SUCCEEDED(hr))
{
    hr = piFactory->CreateStream(&piStream);
}

if (SUCCEEDED(hr))
{
    hr = piStream->InitializeFromFilename(L"output.tif", GENERIC_WRITE);
}

if (SUCCEEDED(hr))
{
   hr = piFactory->CreateEncoder(GUID_ContainerFormatTiff, NULL, &piEncoder);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->Initialize(piStream, WICBitmapEncoderNoCache);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetSize(uiWidth, uiHeight);
}

WICPixelFormatGUID formatGUID = GUID_WICPixelFormat24bppBGR;
if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetPixelFormat(&formatGUID);
}

if (SUCCEEDED(hr))
{
    // We're expecting to write out 24bppRGB. Fail if the encoder cannot do it.
    hr = IsEqualGUID(formatGUID, GUID_WICPixelFormat24bppBGR) ? S_OK : E_FAIL;
}

if (SUCCEEDED(hr))
{
    UINT cbStride = (uiWidth * 24 + 7)/8/***WICGetStride**_/;
    UINT cbBufferSize = uiHeight _ cbStride;

    BYTE *pbBuffer = new BYTE[cbBufferSize];

    if (pbBuffer != NULL)
    {
        for (UINT i = 0; i < cbBufferSize; i++)
        {
            pbBuffer[i] = static_cast<BYTE>(rand());
        }

        hr = piBitmapFrame->WritePixels(uiHeight, cbStride, cbBufferSize, pbBuffer);

        delete[] pbBuffer;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->Commit();
}    

if (SUCCEEDED(hr))
{
    hr = piEncoder->Commit();
}

if (piFactory)
    piFactory->Release();

if (piEncoder)
    piEncoder->Release();

if (piBitmapFrame)
    piBitmapFrame->Release();

if (pPropertybag)
    pPropertybag->Release();

if (piStream)
    piStream->Release();

return hr;
```



## <a name="encoder-options-usage"></a><span data-ttu-id="aae5a-132">Utilisation des options d’encodeur</span><span class="sxs-lookup"><span data-stu-id="aae5a-132">Encoder Options Usage</span></span>

<span data-ttu-id="aae5a-133">Différents encodeurs pour différents formats doivent exposer des options différentes pour la façon dont une image est encodée.</span><span class="sxs-lookup"><span data-stu-id="aae5a-133">Different encoders for different formats need to expose different options for how an image is encoded.</span></span> <span data-ttu-id="aae5a-134">Le composant WIC (Windows Imaging Component) fournit un mécanisme cohérent pour exprimer si des options d’encodage sont requises tout en permettant aux applications de travailler avec plusieurs encodeurs sans avoir besoin de connaître un format particulier.</span><span class="sxs-lookup"><span data-stu-id="aae5a-134">Windows Imaging Component (WIC) provides a consistent mechanism for expressing whether encoding options are required while still enabling applications to work with multiple encoders without requiring knowledge of a particular format.</span></span> <span data-ttu-id="aae5a-135">Pour ce faire, vous devez fournir un paramètre [IPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) sur la méthode [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) et la méthode [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) .</span><span class="sxs-lookup"><span data-stu-id="aae5a-135">This is accomplished by providing an [IPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) parameter on the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method and the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) method.</span></span>

<span data-ttu-id="aae5a-136">La fabrique de composants fournit un point de création facile pour créer un jeu de propriétés d’options d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="aae5a-136">The component factory provides an easy creation point for creating an encoder options property bag.</span></span> <span data-ttu-id="aae5a-137">Les codecs peuvent utiliser ce service s’ils ont besoin de fournir un ensemble simple, intuitif et non conflictuel d’options d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="aae5a-137">Codecs can use this service if they need to provide a simple, intuitive and non-conflicting set of encoder options.</span></span> <span data-ttu-id="aae5a-138">Le jeu de propriétés d’acquisition d’images doit être initialisé lors de la création avec toutes les options de codeur pertinentes pour ce codec.</span><span class="sxs-lookup"><span data-stu-id="aae5a-138">The imaging property bag must be initialized during creation with all the encoder options relevant to that codec.</span></span> <span data-ttu-id="aae5a-139">Pour les options d’encodeur de l’ensemble canonique, la plage de valeurs sera appliquée lors de l’écriture.</span><span class="sxs-lookup"><span data-stu-id="aae5a-139">For encoder options from the canonical set, the value range will be enforced on Write.</span></span> <span data-ttu-id="aae5a-140">Pour les besoins plus avancés, les codecs doivent écrire leur propre implémentation de conteneur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="aae5a-140">For more advanced needs, codecs should write their own property bag implementation.</span></span>

<span data-ttu-id="aae5a-141">Une application reçoit le jeu d’options d’encodeur pendant la création du frame et doit configurer toutes les valeurs avant d’initialiser le frame de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="aae5a-141">An application is given the encoder options bag during frame creation and must configure any values prior to initializing the encoder frame.</span></span> <span data-ttu-id="aae5a-142">Pour une application pilotée par l’interface utilisateur, elle peut offrir une interface utilisateur fixe pour les options de codeur canoniques et une vue avancée pour les options restantes.</span><span class="sxs-lookup"><span data-stu-id="aae5a-142">For a UI-driven application, it can offer a fixed UI for the canonical encoder options and an advanced view for remaining options.</span></span> <span data-ttu-id="aae5a-143">Les modifications peuvent être apportées une par une à l’aide de la méthode Write et toute erreur sera signalée par le biais de IErrorLog.</span><span class="sxs-lookup"><span data-stu-id="aae5a-143">Changes can be made one at a time through the Write method and any error will be reported through IErrorLog.</span></span> <span data-ttu-id="aae5a-144">L’application d’interface utilisateur doit toujours relire et afficher toutes les options après avoir apporté une modification au cas où la modification a entraîné un effet en cascade.</span><span class="sxs-lookup"><span data-stu-id="aae5a-144">The UI application should always re-read and display all options after making a change in case the change caused a cascade effect.</span></span> <span data-ttu-id="aae5a-145">Une application doit être préparée à gérer l’initialisation des frames ayant échoué pour les codecs qui fournissent uniquement un rapport d’erreurs minimal par le biais de leur conteneur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="aae5a-145">An application should be prepared to handle failed frame initialization for codecs that only provide minimal error reporting through their property bag.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="aae5a-146">Options de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="aae5a-146">Encoder Options</span></span>

<span data-ttu-id="aae5a-147">Une application peut s’attendre à rencontrer l’ensemble d’options d’encodeur suivant.</span><span class="sxs-lookup"><span data-stu-id="aae5a-147">An application can expect to encounter the following set of encoder options.</span></span> <span data-ttu-id="aae5a-148">Les options d’encodeur reflètent les fonctionnalités d’un encodeur et du format de conteneur sous-jacent, et par conséquent, sont par leur nature pas vraiment indépendantes des codecs.</span><span class="sxs-lookup"><span data-stu-id="aae5a-148">Encoder options reflect the capabilities of an encoder and the underlying container format, and therefore are by their nature not really codec-agnostic.</span></span> <span data-ttu-id="aae5a-149">Lorsque cela est possible, les nouvelles options doivent être normalisées pour pouvoir être appliquées aux nouveaux codecs qui émergent.</span><span class="sxs-lookup"><span data-stu-id="aae5a-149">When possible, new options should be normalized so they can be applied to new codecs that emerge.</span></span>



| <span data-ttu-id="aae5a-150">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="aae5a-150">Property Name</span></span>      | <span data-ttu-id="aae5a-151">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="aae5a-151">VARTYPE</span></span>  | <span data-ttu-id="aae5a-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="aae5a-152">Value</span></span>                                                                     | <span data-ttu-id="aae5a-153">Codecs applicables</span><span class="sxs-lookup"><span data-stu-id="aae5a-153">Applicable Codecs</span></span> |
|--------------------|----------|---------------------------------------------------------------------------|-------------------|
| <span data-ttu-id="aae5a-154">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="aae5a-154">ImageQuality</span></span>       | <span data-ttu-id="aae5a-155">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="aae5a-155">VT\_R4</span></span>   | <span data-ttu-id="aae5a-156">0-1,0</span><span class="sxs-lookup"><span data-stu-id="aae5a-156">0-1.0</span></span>                                                                     | <span data-ttu-id="aae5a-157">JPEG, HDPhoto</span><span class="sxs-lookup"><span data-stu-id="aae5a-157">JPEG, HDPhoto</span></span>     |
| <span data-ttu-id="aae5a-158">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="aae5a-158">CompressionQuality</span></span> | <span data-ttu-id="aae5a-159">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="aae5a-159">VT\_R4</span></span>   | <span data-ttu-id="aae5a-160">0-1,0</span><span class="sxs-lookup"><span data-stu-id="aae5a-160">0-1.0</span></span>                                                                     | <span data-ttu-id="aae5a-161">TIFF</span><span class="sxs-lookup"><span data-stu-id="aae5a-161">TIFF</span></span>              |
| <span data-ttu-id="aae5a-162">Lossless</span><span class="sxs-lookup"><span data-stu-id="aae5a-162">Lossless</span></span>           | <span data-ttu-id="aae5a-163">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="aae5a-163">VT\_BOOL</span></span> | <span data-ttu-id="aae5a-164">**true**, **false**</span><span class="sxs-lookup"><span data-stu-id="aae5a-164">**TRUE**, **FALSE**</span></span>                                                       | <span data-ttu-id="aae5a-165">HDPhoto</span><span class="sxs-lookup"><span data-stu-id="aae5a-165">HDPhoto</span></span>           |
| <span data-ttu-id="aae5a-166">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="aae5a-166">BitmapTransform</span></span>    | <span data-ttu-id="aae5a-167">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="aae5a-167">VT\_UI1</span></span>  | [<span data-ttu-id="aae5a-168">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="aae5a-168">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="aae5a-169">JPEG</span><span class="sxs-lookup"><span data-stu-id="aae5a-169">JPEG</span></span>              |



 

<span data-ttu-id="aae5a-170">ImageQualty de 0,0 signifie que le rendu de fidélité le plus bas possible et 1,0 correspond à la fidélité la plus élevée, qui peut également être sans perte en fonction du codec.</span><span class="sxs-lookup"><span data-stu-id="aae5a-170">ImageQualty of 0.0 means the lowest possible fidelity rendition and 1.0 means the highest fidelity, which may also imply lossless depending on the codec.</span></span>

<span data-ttu-id="aae5a-171">CompressionQuality de 0,0 signifie le schéma de compression le moins efficace disponible, ce qui entraîne généralement un encodage rapide mais une sortie plus grande.</span><span class="sxs-lookup"><span data-stu-id="aae5a-171">CompressionQuality of 0.0 means the least efficient compression scheme available, typically resulting in a fast encode but larger output.</span></span> <span data-ttu-id="aae5a-172">La valeur 1,0 correspond au schéma le plus efficace disponible, en utilisant généralement plus de temps pour encoder, mais en produisant une sortie plus petite.</span><span class="sxs-lookup"><span data-stu-id="aae5a-172">A value of 1.0 means the most efficient scheme available, typically taking more time to encode but producing smaller output.</span></span> <span data-ttu-id="aae5a-173">Selon les fonctionnalités du codec, cette plage peut être mappée sur un ensemble discret de méthodes de compression disponibles.</span><span class="sxs-lookup"><span data-stu-id="aae5a-173">Depending on the capabilities of the codec, this range may be mapped onto a discrete set of available compression methods.</span></span>

<span data-ttu-id="aae5a-174">Lossless signifie que le codec encode l’image comme Lossless sans perte de données d’image.</span><span class="sxs-lookup"><span data-stu-id="aae5a-174">Lossless means that the codec encodes the image as lossless with no image data loss.</span></span> <span data-ttu-id="aae5a-175">Si le Lossless est activé, ImageQuality est ignoré.</span><span class="sxs-lookup"><span data-stu-id="aae5a-175">If Lossless is enabled, ImageQuality is ignored.</span></span>

<span data-ttu-id="aae5a-176">Outre les options de codeur génériques ci-dessus, les codecs fournis avec WIC prennent en charge les options suivantes.</span><span class="sxs-lookup"><span data-stu-id="aae5a-176">In addition to the above generic encoder options, codecs supplied with WIC support the following options.</span></span> <span data-ttu-id="aae5a-177">Si un codec a besoin de prendre en charge une option qui est cohérente avec l’utilisation dans ces codecs fournis, il est recommandé de le faire.</span><span class="sxs-lookup"><span data-stu-id="aae5a-177">If a codec has a need to support an option that is consistent with the usage in these supplied codecs, it is encouraged to do so.</span></span>



| <span data-ttu-id="aae5a-178">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="aae5a-178">Property Name</span></span>           | <span data-ttu-id="aae5a-179">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="aae5a-179">VARTYPE</span></span>           | <span data-ttu-id="aae5a-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="aae5a-180">Value</span></span>                                                                             | <span data-ttu-id="aae5a-181">Codecs applicables</span><span class="sxs-lookup"><span data-stu-id="aae5a-181">Applicable Codecs</span></span> |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|-------------------|
| <span data-ttu-id="aae5a-182">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="aae5a-182">InterlaceOption</span></span>         | <span data-ttu-id="aae5a-183">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="aae5a-183">VT\_BOOL</span></span>          | <span data-ttu-id="aae5a-184">Actif/inactif</span><span class="sxs-lookup"><span data-stu-id="aae5a-184">On/Off</span></span>                                                                            | <span data-ttu-id="aae5a-185">PNG</span><span class="sxs-lookup"><span data-stu-id="aae5a-185">PNG</span></span>               |
| <span data-ttu-id="aae5a-186">FilterOption</span><span class="sxs-lookup"><span data-stu-id="aae5a-186">FilterOption</span></span>            | <span data-ttu-id="aae5a-187">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="aae5a-187">VT\_UI1</span></span>           | [<span data-ttu-id="aae5a-188">**WICPngFilterOption**</span><span class="sxs-lookup"><span data-stu-id="aae5a-188">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)                       | <span data-ttu-id="aae5a-189">PNG</span><span class="sxs-lookup"><span data-stu-id="aae5a-189">PNG</span></span>               |
| <span data-ttu-id="aae5a-190">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="aae5a-190">TiffCompressionMethod</span></span>   | <span data-ttu-id="aae5a-191">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="aae5a-191">VT\_UI1</span></span>           | [<span data-ttu-id="aae5a-192">**WICTiffCompressionOption**</span><span class="sxs-lookup"><span data-stu-id="aae5a-192">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)           | <span data-ttu-id="aae5a-193">TIFF</span><span class="sxs-lookup"><span data-stu-id="aae5a-193">TIFF</span></span>              |
| <span data-ttu-id="aae5a-194">Luminance</span><span class="sxs-lookup"><span data-stu-id="aae5a-194">Luminance</span></span>               | <span data-ttu-id="aae5a-195">\_Groupe VT UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="aae5a-195">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="aae5a-196">64 entrées (DCT)</span><span class="sxs-lookup"><span data-stu-id="aae5a-196">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="aae5a-197">JPEG</span><span class="sxs-lookup"><span data-stu-id="aae5a-197">JPEG</span></span>              |
| <span data-ttu-id="aae5a-198">Chrominance</span><span class="sxs-lookup"><span data-stu-id="aae5a-198">Chrominance</span></span>             | <span data-ttu-id="aae5a-199">\_Groupe VT UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="aae5a-199">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="aae5a-200">64 entrées (DCT)</span><span class="sxs-lookup"><span data-stu-id="aae5a-200">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="aae5a-201">JPEG</span><span class="sxs-lookup"><span data-stu-id="aae5a-201">JPEG</span></span>              |
| <span data-ttu-id="aae5a-202">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="aae5a-202">JpegYCrCbSubsampling</span></span>    | <span data-ttu-id="aae5a-203">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="aae5a-203">VT\_UI1</span></span>           | [<span data-ttu-id="aae5a-204">**WICJpegYCrCbSubsamplingOption**</span><span class="sxs-lookup"><span data-stu-id="aae5a-204">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | <span data-ttu-id="aae5a-205">JPEG</span><span class="sxs-lookup"><span data-stu-id="aae5a-205">JPEG</span></span>              |
| <span data-ttu-id="aae5a-206">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="aae5a-206">SuppressApp0</span></span>            | <span data-ttu-id="aae5a-207">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="aae5a-207">VT\_BOOL</span></span>          |                                                                                   | <span data-ttu-id="aae5a-208">JPEG</span><span class="sxs-lookup"><span data-stu-id="aae5a-208">JPEG</span></span>              |
| <span data-ttu-id="aae5a-209">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="aae5a-209">EnableV5Header32bppBGRA</span></span> | <span data-ttu-id="aae5a-210">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="aae5a-210">VT\_BOOL</span></span>          | <span data-ttu-id="aae5a-211">Actif/inactif</span><span class="sxs-lookup"><span data-stu-id="aae5a-211">On/Off</span></span>                                                                            | <span data-ttu-id="aae5a-212">BMP</span><span class="sxs-lookup"><span data-stu-id="aae5a-212">BMP</span></span>               |



 

<span data-ttu-id="aae5a-213">Utilisez **VT \_ vide** pour indiquer qu’il **\* \* n’est pas défini** comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="aae5a-213">Use **VT\_EMPTY** to indicate **\*not set\*** as the default.</span></span> <span data-ttu-id="aae5a-214">Si des propriétés supplémentaires sont définies mais pas prises en charge, l’encodeur doit les ignorer. Cela permet aux applications de coder moins de logique s’ils souhaitent une fonctionnalité qui peut ou non être présente.</span><span class="sxs-lookup"><span data-stu-id="aae5a-214">If additional properties are set but not supported, the encoder should ignore them; this allows applications to code less logic if they want a capability that may or may not be present.</span></span>

## <a name="encoder-options-examples"></a><span data-ttu-id="aae5a-215">Exemples d’options d’encodeur</span><span class="sxs-lookup"><span data-stu-id="aae5a-215">Encoder Options Examples</span></span>

<span data-ttu-id="aae5a-216">Dans l' [exemple d’encodage TIFF](#tiff-encoding-example) ci-dessus, une option d’encodeur spécifique est définie.</span><span class="sxs-lookup"><span data-stu-id="aae5a-216">In the [TIFF Encoding Example](#tiff-encoding-example) above, a specific encoder option is set.</span></span> <span data-ttu-id="aae5a-217">Le membre *pstrName* de la structure PROPBAG2 est défini sur le nom de propriété approprié, et la variante est définie sur le VarType correspondant et la valeur souhaitée (dans ce cas, un membre de l’énumération [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) .</span><span class="sxs-lookup"><span data-stu-id="aae5a-217">The *pstrName* member of the PROPBAG2 structure is set to the appropriate property name, and the VARIANT is set to the corresponding VARTYPE and the desired value—in this case, a member of the [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) enumeration.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



<span data-ttu-id="aae5a-218">Pour utiliser les options d’encodeur par défaut, il vous suffit d’initialiser le frame de bitmap avec le jeu de propriétés retourné lors de la création du frame.</span><span class="sxs-lookup"><span data-stu-id="aae5a-218">To use the default encoder options, simply initialize the bitmap frame with the property bag returned when the frame was created.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // Accept the default encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



<span data-ttu-id="aae5a-219">Il est également possible d’éliminer le jeu de propriétés quand aucune option d’encodeur n’est prise en compte.</span><span class="sxs-lookup"><span data-stu-id="aae5a-219">It is also possible to eliminate the property bag when no encoder options are being considered.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, 0);
}

if (SUCCEEDED(hr))
{        
    // No encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(0);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="aae5a-220">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aae5a-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="aae5a-221">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="aae5a-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="aae5a-222">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="aae5a-222">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="aae5a-223">Décodage, vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="aae5a-223">Decoding Overview</span></span>](-wic-creating-decoder.md)
</dt> <dt>

<span data-ttu-id="aae5a-224">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="aae5a-224">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="aae5a-225">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="aae5a-225">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
