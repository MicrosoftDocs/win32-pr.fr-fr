---
description: Le récepteur de fichiers ASF est une implémentation de IMFMediaSink fournie par Media Foundation qu’une application peut utiliser pour archiver des données de média ASF dans un fichier. Pour plus d’informations sur le modèle objet des récepteurs de média ASF et l’utilisation générale, consultez récepteurs de média ASF.
ms.assetid: ecfddf4e-71b4-42c4-8b54-9868cec6ed9b
title: Ajout de métadonnées au récepteur de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71bb63a10d935b52e6d048dbc5dcd07370dd2ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034029"
---
# <a name="adding-metadata-to-the-file-sink"></a><span data-ttu-id="648e4-104">Ajout de métadonnées au récepteur de fichiers</span><span class="sxs-lookup"><span data-stu-id="648e4-104">Adding Metadata to the File Sink</span></span>

<span data-ttu-id="648e4-105">Le récepteur de fichiers ASF est une implémentation de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fournie par Media Foundation qu’une application peut utiliser pour archiver des données de média ASF dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="648e4-105">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="648e4-106">Pour plus d’informations sur le modèle objet et l’utilisation générale des récepteurs de média ASF, consultez [récepteurs de média ASF](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="648e4-106">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="648e4-107">Une fois [le récepteur de fichiers ASF créé](creating-the-asf-file-sink.md), il doit être configuré avec des informations sur les flux et les informations d’encodage dans le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="648e4-107">After [Creating the ASF file sink](creating-the-asf-file-sink.md), it must be configured with information about the streams and encoding information in the output file.</span></span> <span data-ttu-id="648e4-108">Ces procédures sont décrites dans [Ajout d’informations de flux au récepteur de fichiers ASF](adding-stream-information-to-the-asf-file-sink.md) et [définition des propriétés dans le récepteur de fichiers](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="648e4-108">These procedures are described in [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md) and [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span> <span data-ttu-id="648e4-109">En outre, vous pouvez également ajouter des informations de métadonnées avec des paires nom/valeur, telles que « auteur », titre.</span><span class="sxs-lookup"><span data-stu-id="648e4-109">In addition, You can also add metadata information includes name/value pairs such as "Author", Title".</span></span> <span data-ttu-id="648e4-110">Cette rubrique décrit le processus d’ajout d’informations de métadonnées au récepteur de fichiers afin qu’il apparaisse dans l' [objet d’en-tête ASF](asf-file-structure.md)final.</span><span class="sxs-lookup"><span data-stu-id="648e4-110">This topic describes the process of adding metadata information to the file sink so that it appears in the final [ASF Header Object](asf-file-structure.md).</span></span>

<span data-ttu-id="648e4-111">Vous pouvez ajouter des informations de métadonnées au récepteur de fichiers ASF avant de générer la topologie d’encodage.</span><span class="sxs-lookup"><span data-stu-id="648e4-111">You can add metadata information to the ASF file sink before building the encoding topology.</span></span> <span data-ttu-id="648e4-112">L’objet ASF ContentInfo pour le récepteur de fichiers effectue le suivi des propriétés de métadonnées et est exposé à l’application via l’interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="648e4-112">The ASF ContentInfo object for the file sink keeps track of the metadata properties and are exposed to the application through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span> <span data-ttu-id="648e4-113">Certaines de ces propriétés, telles que « IsVBR », qui indiquent si le fichier contient des flux à débit binaire variable (VBR), sont définies automatiquement par le récepteur de fichiers en analysant les propriétés d’encodage de flux définies.</span><span class="sxs-lookup"><span data-stu-id="648e4-113">Some of these properties, such as "IsVBR" that indicates if the file contains variable bit rate (VBR) streams, are set automatically by the file sink by parsing the stream encoding properties that are set.</span></span>

<span data-ttu-id="648e4-114">Pour obtenir la liste complète des propriétés, consultez la rubrique « liste d’attributs » dans la documentation du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="648e4-114">For a complete list of properties, see the "Attribute List" topic in the Format SDK documentation.</span></span>

## <a name="using-the-imfmetadata-interface-on-the-asf-file-sink"></a><span data-ttu-id="648e4-115">Utilisation de l’interface IMFMetadata sur le récepteur de fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="648e4-115">Using the IMFMetadata Interface on the ASF File Sink</span></span>

1.  <span data-ttu-id="648e4-116">Interrogez l’objet de récepteur de fichiers ASF pour obtenir un pointeur vers son implémentation de l’interface [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) .</span><span class="sxs-lookup"><span data-stu-id="648e4-116">Query the ASF file sink object to get a pointer to its implementation of the [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) interface.</span></span>
2.  <span data-ttu-id="648e4-117">Appelez [**IMFMetadataProvider :: GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) pour accéder à un pointeur [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="648e4-117">Call [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) to get an [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) pointer.</span></span>

    <span data-ttu-id="648e4-118">Le paramètre *pPresentationDescriptor* est ignoré et l’application peut passer la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="648e4-118">The *pPresentationDescriptor* parameter is ignored and the application can pass **NULL**.</span></span> <span data-ttu-id="648e4-119">Si l’application passe zéro comme identificateur de flux dans le paramètre *dwStreamIdentifier* , la méthode récupère les métadonnées qui s’appliquent à l’ensemble du fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="648e4-119">If the application passes zero as the stream identifier in the *dwStreamIdentifier* parameter, the method retrieves metadata that applies to the entire ASF file.</span></span> <span data-ttu-id="648e4-120">Dans le cas contraire, seules les métadonnées du flux sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="648e4-120">Otherwise, only the metadata for the stream is retrieved.</span></span>

3.  <span data-ttu-id="648e4-121">Appelez [**IMFMetadata :: GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) pour récupérer la liste des propriétés de codage de fichiers définies sur le contenu multimédia.</span><span class="sxs-lookup"><span data-stu-id="648e4-121">Call [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) to retrieve the list of file-encoding properties set on the media content.</span></span>
4.  <span data-ttu-id="648e4-122">Appelez [**IMFMetadata :: GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) pour récupérer les valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="648e4-122">Call [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) to get the property values.</span></span>

## <a name="example"></a><span data-ttu-id="648e4-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="648e4-123">Example</span></span>

<span data-ttu-id="648e4-124">L’exemple de code suivant montre comment énumérer les noms et les valeurs des propriétés qui sont définis sur le fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="648e4-124">The following example code shows how to enumerate the property names and values that are set on the ASF file.</span></span>


```C++
/////////////////////////////////////////////////////////////////////
// Name: ListASFProperties
//
// Enumerates the metadata properties of the ASF file. 
//
// pContentInfo: Pointer to the ASF ContentInfo object.
/////////////////////////////////////////////////////////////////////

HRESULT ListASFProperties(IMFASFContentInfo *pContentInfo)
{
    HRESULT hr = S_OK;
    
    PROPVARIANT varNames;
    PropVariantInit(&varNames);

    PROPVARIANT varValue;
    PropVariantInit(&varValue);

    IMFMetadataProvider* pProvider = NULL;
    IMFMetadata* pMetadata = NULL;

    // Query the ContentInfo object for IMFMetadataProvider.
    CHECK_HR(hr = pContentInfo->QueryInterface(IID_IMFMetadataProvider,
        (void**)&pProvider));

    // Get a pointer to IMFMetadata for file-wide metadata.
    CHECK_HR(hr = pProvider->GetMFMetadata(NULL, 0, 0, &pMetadata));

    // Get the property names that are stored in the metadata object.
    CHECK_HR(hr = pMetadata->GetAllPropertyNames(&varNames));

    // Loop through the properties and get their values.
    if (varNames.vt == (VT_VECTOR | VT_LPWSTR))
    {
        ULONG cElements = varNames.calpwstr.cElems;
        for (ULONG i = 0; i < cElements; i++)
        {
            const WCHAR* sName = varNames.calpwstr.pElems[i];
            CHECK_HR(hr = pMetadata->GetProperty(sName, &varValue));
            //Use the property values. Not shown.
            PropVariantClear(&varValue);
        }
    }
done:
    PropVariantClear(&varNames);
    PropVariantClear(&varValue);
    SAFE_RELEASE (pMetaData);
    SAFE_RELEASE (pProvider);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="648e4-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="648e4-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="648e4-126">Récepteurs de média ASF</span><span class="sxs-lookup"><span data-stu-id="648e4-126">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="648e4-127">Composants ASF de couche de pipeline</span><span class="sxs-lookup"><span data-stu-id="648e4-127">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="648e4-128">Prise en charge ASF dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="648e4-128">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



