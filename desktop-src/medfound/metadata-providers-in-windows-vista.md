---
description: Dans Windows Vista, Microsoft Media Foundation expose les métadonnées par le biais de l’interface IMFMetadata.
ms.assetid: a26e40c2-1717-4a13-8bf0-e41376a8d317
title: Fournisseurs de métadonnées dans Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1726e04058a7b15e387fca4f3faa94fce7c91c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544700"
---
# <a name="metadata-providers-in-windows-vista"></a><span data-ttu-id="a648d-103">Fournisseurs de métadonnées dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a648d-103">Metadata Providers in Windows Vista</span></span>

<span data-ttu-id="a648d-104">Dans Windows Vista, Microsoft Media Foundation expose les métadonnées par le biais de l’interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="a648d-104">In Windows Vista, Microsoft Media Foundation exposes metadata through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span>

## <a name="reading-metadata"></a><span data-ttu-id="a648d-105">Lecture des métadonnées</span><span class="sxs-lookup"><span data-stu-id="a648d-105">Reading Metadata</span></span>

<span data-ttu-id="a648d-106">Pour lire les métadonnées d’une source de média, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a648d-106">To read metadata from a media source, perform the following steps:</span></span>

1.  <span data-ttu-id="a648d-107">Obtient un pointeur vers l’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) de la source du média.</span><span class="sxs-lookup"><span data-stu-id="a648d-107">Get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span> <span data-ttu-id="a648d-108">Vous pouvez utiliser l’interface [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) pour récupérer un pointeur **IMFMediaSource** .</span><span class="sxs-lookup"><span data-stu-id="a648d-108">You can use the [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface to get an **IMFMediaSource** pointer.</span></span>
2.  <span data-ttu-id="a648d-109">Appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) pour récupérer le descripteur de présentation de la source du média.</span><span class="sxs-lookup"><span data-stu-id="a648d-109">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to get the media source's presentation descriptor.</span></span>
3.  <span data-ttu-id="a648d-110">Appelez [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) sur la source du média pour obtenir un pointeur vers l’interface [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) .</span><span class="sxs-lookup"><span data-stu-id="a648d-110">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media source to get a pointer to the [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) interface.</span></span> <span data-ttu-id="a648d-111">Dans le paramètre *guidService* de **MFGetService**, spécifiez la **valeur \_ \_ \_ service du fournisseur de métadonnées MF**.</span><span class="sxs-lookup"><span data-stu-id="a648d-111">In the *guidService* parameter of **MFGetService**, specify the value **MF\_METADATA\_PROVIDER\_SERVICE**.</span></span> <span data-ttu-id="a648d-112">Si la source ne prend pas en charge l’interface **IMFMetadataProvider** , **MFGetService** retourne le **\_ service MF E \_ non pris en charge \_**.</span><span class="sxs-lookup"><span data-stu-id="a648d-112">If the source does not support the **IMFMetadataProvider** interface, **MFGetService** returns **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
4.  <span data-ttu-id="a648d-113">Appelez [**IMFMetadataProvider :: GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) et transmettez un pointeur vers le descripteur de présentation.</span><span class="sxs-lookup"><span data-stu-id="a648d-113">Call [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) and pass in a pointer to the presentation descriptor.</span></span> <span data-ttu-id="a648d-114">Cette méthode retourne un pointeur vers l’interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="a648d-114">This method returns a pointer to the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span>
    -   <span data-ttu-id="a648d-115">Pour récupérer les métadonnées au niveau du flux, appelez d’abord [**IMFStreamDescriptor :: GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) pour récupérer l’identificateur de flux.</span><span class="sxs-lookup"><span data-stu-id="a648d-115">To get stream-level metadata first call [**IMFStreamDescriptor::GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) to get the stream identifier.</span></span> <span data-ttu-id="a648d-116">Transmettez ensuite l’identificateur de flux dans le paramètre *dwStreamIdentifier* de [**GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata).</span><span class="sxs-lookup"><span data-stu-id="a648d-116">Then pass the stream identifier in the *dwStreamIdentifier* parameter of [**GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata).</span></span>
    -   <span data-ttu-id="a648d-117">Pour récupérer les métadonnées au niveau de la présentation, définissez *dwStreamIdentifier* sur zéro.</span><span class="sxs-lookup"><span data-stu-id="a648d-117">To get presentation-level metadata, set *dwStreamIdentifier* to zero.</span></span>
5.  <span data-ttu-id="a648d-118">\[\]Appelez [**IMFMetadata :: GetAllLanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) facultatif pour obtenir la liste des langues dans lesquelles les métadonnées sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="a648d-118">\[Optional\] Call [**IMFMetadata::GetAllLanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) to get a list of the languages in which metadata is available.</span></span> <span data-ttu-id="a648d-119">Les langues sont identifiées à l’aide de balises de langue conformes à RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="a648d-119">Languages are identified using RFC 1766-compliant language tags.</span></span>
6.  <span data-ttu-id="a648d-120">\[\]Appelez [**IMFMetadata :: SetLanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) facultatif pour sélectionner la langue.</span><span class="sxs-lookup"><span data-stu-id="a648d-120">\[Optional\] Call [**IMFMetadata::SetLanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) to select the language.</span></span>
7.  <span data-ttu-id="a648d-121">\[\]Appelez [**IMFMetadata :: GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) facultatif pour obtenir la liste des noms de toutes les propriétés de métadonnées pour ce flux ou cette présentation.</span><span class="sxs-lookup"><span data-stu-id="a648d-121">\[Optional\] Call [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) to get a list of the names of all the metadata properties for this stream or presentation.</span></span>
8.  <span data-ttu-id="a648d-122">Appelez [**IMFMetadata :: GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) pour obtenir une valeur de propriété de métadonnées spécifique, en passant le nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="a648d-122">Call [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) to get a specific metadata property value, passing in the name of the property.</span></span>

<span data-ttu-id="a648d-123">Le code suivant montre les étapes 2 à 4 :</span><span class="sxs-lookup"><span data-stu-id="a648d-123">The following code shows steps 2–4:</span></span>


```C++
HRESULT GetMetadata(
    IMFMediaSource *pSource, IMFMetadata **ppMetadata, DWORD dwStream = 0)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFMetadataProvider *pProvider = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFGetService(
        pSource, MF_METADATA_PROVIDER_SERVICE, IID_PPV_ARGS(&pProvider));

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProvider->GetMFMetadata(pPD, dwStream, 0, ppMetadata);

done:
    SafeRelease(&pPD);
    SafeRelease(&pProvider);
    return hr;
}
```



<span data-ttu-id="a648d-124">Le code suivant montre les étapes 7 à 8.</span><span class="sxs-lookup"><span data-stu-id="a648d-124">The following code shows steps 7–8.</span></span> <span data-ttu-id="a648d-125">Supposons que `DisplayProperty` est une fonction qui affiche une valeur **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="a648d-125">Assume that `DisplayProperty` is a function that displays a **PROPVARIANT** value.</span></span>


```C++
HRESULT DisplayMetadata(IMFMetadata *pMetadata)
{
    PROPVARIANT varNames;
    HRESULT hr = pMetadata->GetAllPropertyNames(&varNames);
    if (FAILED(hr))
    {
        return hr;
    }

    for (ULONG i = 0; i < varNames.calpwstr.cElems; i++)
    {
        wprintf(L"%s\n", varNames.calpwstr.pElems[i]);

        PROPVARIANT varValue;
        hr = pMetadata->GetProperty( varNames.calpwstr.pElems[i], &varValue );
        if (SUCCEEDED(hr))
        {
            DisplayProperty(varValue);
            PropVariantClear(&varValue);
        }
    }

    PropVariantClear(&varNames);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="a648d-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a648d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a648d-127">Métadonnées de média</span><span class="sxs-lookup"><span data-stu-id="a648d-127">Media Metadata</span></span>](media-metadata.md)
</dt> <dt>

[<span data-ttu-id="a648d-128">Fournisseurs de métadonnées de Shell</span><span class="sxs-lookup"><span data-stu-id="a648d-128">Shell Metadata Providers</span></span>](shell-metadata-providers.md)
</dt> </dl>

 

 



