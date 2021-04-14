---
description: Définition des propriétés de compression vidéo
ms.assetid: 2be03a2c-39a5-46da-9bbc-af42c08150ab
title: Définition des propriétés de compression vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d29ed7e42745ffd51fca14b7da5f72c749281e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392672"
---
# <a name="setting-video-compression-properties"></a><span data-ttu-id="f7ada-103">Définition des propriétés de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="f7ada-103">Setting Video Compression Properties</span></span>

<span data-ttu-id="f7ada-104">Les filtres de compression vidéo peuvent prendre en charge l’interface [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) sur leurs broches de sortie.</span><span class="sxs-lookup"><span data-stu-id="f7ada-104">Video compression filters can support the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface on their output pins.</span></span> <span data-ttu-id="f7ada-105">Utilisez cette interface pour définir les propriétés de compression, telles que la fréquence d’images clés, le nombre d’images prédites (P) par image clé et la qualité de compression relative.</span><span class="sxs-lookup"><span data-stu-id="f7ada-105">Use this interface to set compression properties, such as the key frame rate, the number of predicted (P) frames per key frame, and the relative compression quality.</span></span>

<span data-ttu-id="f7ada-106">Tout d’abord, appelez la méthode [**IBaseFilter :: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) pour rechercher la broche de sortie du filtre, puis interrogez le code confidentiel de l’interface.</span><span class="sxs-lookup"><span data-stu-id="f7ada-106">First, call the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method to find the filter's output pin, and query the pin for the interface.</span></span> <span data-ttu-id="f7ada-107">Certains filtres peuvent ne pas prendre en charge l’interface du tout.</span><span class="sxs-lookup"><span data-stu-id="f7ada-107">Some filters may not support the interface at all.</span></span> <span data-ttu-id="f7ada-108">D’autres peuvent exposer l’interface, mais ne prennent pas en charge chaque propriété de compression.</span><span class="sxs-lookup"><span data-stu-id="f7ada-108">Others may expose the interface but not support every compression property.</span></span> <span data-ttu-id="f7ada-109">Pour déterminer les propriétés prises en charge, appelez [**IAMVideoCompression :: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span><span class="sxs-lookup"><span data-stu-id="f7ada-109">To determine which properties are supported, call [**IAMVideoCompression::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span></span> <span data-ttu-id="f7ada-110">Cette méthode retourne plusieurs éléments d’information :</span><span class="sxs-lookup"><span data-stu-id="f7ada-110">This method returns several pieces of information:</span></span>

-   <span data-ttu-id="f7ada-111">Un ensemble d’indicateurs de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="f7ada-111">A set of capabilities flags</span></span>
-   <span data-ttu-id="f7ada-112">Chaîne descriptive et chaîne de numéro de version</span><span class="sxs-lookup"><span data-stu-id="f7ada-112">A descriptive string and version-number string</span></span>
-   <span data-ttu-id="f7ada-113">Valeurs par défaut pour la fréquence d’images clés, la fréquence d’images P et la qualité (en cas de prise en charge)</span><span class="sxs-lookup"><span data-stu-id="f7ada-113">Default values for key frame rate, P frame rate, and quality (when supported)</span></span>

<span data-ttu-id="f7ada-114">La méthode a la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="f7ada-114">The method has the following syntax:</span></span>


```C++
hr = pCompress->GetInfo(pszVersion, &cbVersion, pszDesc, &cbDesc, 
         &lKeyFrame, &lPFrame, &dblQuality, &lCap);
```



<span data-ttu-id="f7ada-115">Les paramètres *pszVersion* et *pszDesc* sont des mémoires tampons à caractères larges qui reçoivent la chaîne de version et la chaîne de description.</span><span class="sxs-lookup"><span data-stu-id="f7ada-115">The *pszVersion* and *pszDesc* parameters are wide-character buffers that receive the version string and description string.</span></span> <span data-ttu-id="f7ada-116">Les paramètres *cbVersion* et *cbDesc* reçoivent les tailles de mémoire tampon requises en octets (et non en caractères).</span><span class="sxs-lookup"><span data-stu-id="f7ada-116">The *cbVersion* and *cbDesc* parameters receive the required buffer sizes in bytes (not characters).</span></span> <span data-ttu-id="f7ada-117">Les paramètres *lKeyFrame*, *lPFrame* et *dblQuality* reçoivent les valeurs par défaut pour la fréquence d’images clé, la fréquence d’images P et la qualité.</span><span class="sxs-lookup"><span data-stu-id="f7ada-117">The *lKeyFrame*, *lPFrame*, and *dblQuality* parameters receive the default values for the key frame rate, P frame rate, and quality.</span></span> <span data-ttu-id="f7ada-118">La qualité est exprimée sous la forme d’un nombre à virgule flottante compris entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="f7ada-118">Quality is expressed as a floating-point number from 0.0 to 1.0.</span></span> <span data-ttu-id="f7ada-119">Le paramètre *lCap* reçoit **une opération or au niveau du bit** des indicateurs de fonctionnalités, qui sont définis par le type énuméré [**CompressionCaps**](/windows/desktop/api/strmif/ne-strmif-compressioncaps) .</span><span class="sxs-lookup"><span data-stu-id="f7ada-119">The *lCap* parameter receives a bitwise **OR** of the capabilities flags, which are defined by the [**CompressionCaps**](/windows/desktop/api/strmif/ne-strmif-compressioncaps) enumerated type.</span></span>

<span data-ttu-id="f7ada-120">L’un de ces paramètres peut être **null**, auquel cas la méthode ignore ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="f7ada-120">Any of these parameters can be **NULL**, in which case the method ignores that parameter.</span></span> <span data-ttu-id="f7ada-121">Par exemple, pour allouer des tampons pour les chaînes de version et de description, appelez d’abord la méthode avec **null** dans les premier et troisième paramètres.</span><span class="sxs-lookup"><span data-stu-id="f7ada-121">For example, to allocate buffers for the version and description strings, first call the method with **NULL** in the first and third parameters.</span></span> <span data-ttu-id="f7ada-122">Utilisez les valeurs retournées pour *cbVersion* et *cbDesc* pour allouer les mémoires tampons, puis appelez à nouveau la méthode :</span><span class="sxs-lookup"><span data-stu-id="f7ada-122">Use the returned values for *cbVersion* and *cbDesc* to allocate the buffers and then call the method again:</span></span>


```C++
int cbVersion, cbDesc; // Size in bytes, not characters!
hr = pCompress->GetInfo(0, &cbVersion, 0, &cbDesc, 0, 0, 0, 0);
if (SUCCEEDED(hr))
{
    WCHAR *pszVersion = new WCHAR[cbVersion/2]; // Wide character = 2 bytes
    WCHAR *pszDesc = new WCHAR[cbDesc/2];
    hr = pCompress->GetInfo(pszVersion, 0, pszDesc, 0, 0, 0, 0, 0);
}
```



<span data-ttu-id="f7ada-123">La valeur de *lCap* indique laquelle des autres méthodes **IAMVideoCompression** prend en charge le filtre.</span><span class="sxs-lookup"><span data-stu-id="f7ada-123">The value of *lCap* indicates which of the other **IAMVideoCompression** methods the filter supports.</span></span> <span data-ttu-id="f7ada-124">Par exemple, si *lCap* contient l' \_ indicateur CompressionCaps CanKeyFrame, vous pouvez appeler [**IAMVideoCompression :: obtenir \_ keycadence**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) pour obtenir la fréquence d’images clé et [**IAMVideoCompression ::p ut \_**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) pour définir la fréquence d’images clé.</span><span class="sxs-lookup"><span data-stu-id="f7ada-124">For example, if *lCap* contains the CompressionCaps\_CanKeyFrame flag, you can call [**IAMVideoCompression::get\_KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) to get the key frame rate and [**IAMVideoCompression::put\_KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) to set the key frame rate.</span></span> <span data-ttu-id="f7ada-125">Une valeur négative indique que le filtre utilisera la valeur par défaut, telle qu’elle est obtenue à partir de [**IAMVideoCompression :: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span><span class="sxs-lookup"><span data-stu-id="f7ada-125">A negative value indicates that the filter will use the default value, as obtained from [**IAMVideoCompression::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span></span> <span data-ttu-id="f7ada-126">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f7ada-126">For example:</span></span>


```C++
if (lCap & CompressionCaps_CanKeyFrame)
{
    hr = pCompress->get_KeyFrameRate(&lKeyFrame);
    if (FAILED(hr) || lKeyFrame < 0)
    {
        lKeyFrame = lDefaultKeyFrame; // From GetInfo.
    }
}
```



<span data-ttu-id="f7ada-127">L’exemple de code suivant tente de trouver l’interface **IAMVideoCompression** sur la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="f7ada-127">The following code example tries to find the **IAMVideoCompression** interface on the output pin.</span></span> <span data-ttu-id="f7ada-128">Si elle est réussie, elle récupère les valeurs par défaut et réelles des propriétés de compression :</span><span class="sxs-lookup"><span data-stu-id="f7ada-128">If it succeeds, it retrieves the default and actual values for the compression properties:</span></span>


```C++
HRESULT hr = E_FAIL;
IEnumPins *pEnum = NULL;
IPin *pPin = NULL;
IAMVideoCompression *pCompress = NULL;

// Find the pin that supports IAMVideoCompression (if any).
pFilter->EnumPins(&pEnum);
while (S_OK == pEnum->Next(1, &pPin, NULL))
{
    hr = pPin->QueryInterface(IID_IAMVideoCompression, (void**)&pCompress);
    pPin->Release();
    if (SUCCEEDED(hr)) // Found the interface.
    {
        break;
    }
}
if (SUCCEEDED(hr)) 
{
    long lCap;                     // Capability flags
    long lKeyFrame, lPFrame;       // Real values
    double m_Quality;
    long lKeyFrameDef, lPFrameDef; // Default values
    double QualityDef;
    
    // Get default values and capabilities.
    hr = pCompress->GetInfo(0, 0, 0, 0, &KeyFrameDef, &lPFrameDef,
             &QualityDef, &lCap);
    if (SUCCEEDED(hr))
    {
        // Get actual values where possible.
        if (lCap & CompressionCaps_CanKeyFrame)
        {
            hr = pCompress->get_KeyFrameRate(&lKeyFrame);
            if (FAILED(hr) || lKeyFrame < 0)
                lKeyFrame = lKeyFrameDef;
        }
        if (lCap & CompressionCaps_CanBFrame)
        {
            hr = pCompress->get_PFramesPerKeyFrame(&lPFrame);
            if (FAILED(hr) || lPFrame < 0)
                lPFrame = lPFrameDef;
        }
        if (lCap & CompressionCaps_CanQuality)
        {
            hr = pCompress->get_Quality(&Quality);
            if (FAILED(hr) || Quality < 0)
                Quality = QualityDef;
        }
    }
}
```



> [!Note]  
> <span data-ttu-id="f7ada-129">Si vous utilisez l’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) pour générer votre graphique, vous pouvez obtenir l’interface **IAMVideoCompression** en appelant [**ICaptureGraphBuilder2 :: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface), au lieu d’utiliser **IBaseFilter :: EnumPins**.</span><span class="sxs-lookup"><span data-stu-id="f7ada-129">If you are using the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface to build your graph, you can obtain the **IAMVideoCompression** interface by calling [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface), instead of using **IBaseFilter::EnumPins**.</span></span> <span data-ttu-id="f7ada-130">La méthode **FindInterface** est une méthode d’assistance qui recherche des filtres et des codes confidentiels dans le graphique pour une interface spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f7ada-130">The **FindInterface** method is a helper method that searches filters and pins in the graph for a specified interface.</span></span>

 

 

 



