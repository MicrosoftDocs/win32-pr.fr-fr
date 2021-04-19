---
description: À compter de Windows 7, Microsoft Media Foundation expose des métadonnées par le biais de l’interface IPropertyStore.
ms.assetid: d219d3f1-3940-46ed-9811-3cf8bf1eec55
title: Fournisseurs de métadonnées de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35488e750531a5ee7bac7dc915990593ecee1d10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519579"
---
# <a name="shell-metadata-providers"></a><span data-ttu-id="d93d1-103">Fournisseurs de métadonnées de Shell</span><span class="sxs-lookup"><span data-stu-id="d93d1-103">Shell Metadata Providers</span></span>

<span data-ttu-id="d93d1-104">À compter de Windows 7, Microsoft Media Foundation expose des métadonnées par le biais de l’interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="d93d1-104">Starting in Windows 7, Microsoft Media Foundation exposes metadata through the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span>

<span data-ttu-id="d93d1-105">Les métadonnées obtenues à l’aide du processus défini dans cette rubrique doivent être utilisées uniquement pour l’accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d93d1-105">Metadata obtained using the process defined in this topic should only be used for read-only access.</span></span> <span data-ttu-id="d93d1-106">L’écriture de données à l’aide de ce processus n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d93d1-106">Writing data using this process is not supported.</span></span> <span data-ttu-id="d93d1-107">Vous pouvez créer un objet [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) à des fins d’écriture à l’aide d’un identificateur de classe (CLSID) obtenu à partir de [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).</span><span class="sxs-lookup"><span data-stu-id="d93d1-107">You can create an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object for writing purposes using a class identifier (CLSID) obtained from [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).</span></span>

## <a name="reading-metadata"></a><span data-ttu-id="d93d1-108">Lecture des métadonnées</span><span class="sxs-lookup"><span data-stu-id="d93d1-108">Reading Metadata</span></span>

<span data-ttu-id="d93d1-109">Pour lire les métadonnées d’une source de média, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="d93d1-109">To read metadata from a media source, perform the following steps:</span></span>

1.  <span data-ttu-id="d93d1-110">Obtient un pointeur vers l’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) de la source du média.</span><span class="sxs-lookup"><span data-stu-id="d93d1-110">Get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span> <span data-ttu-id="d93d1-111">Vous pouvez utiliser l’interface [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) pour récupérer un pointeur **IMFMediaSource** .</span><span class="sxs-lookup"><span data-stu-id="d93d1-111">You can use the [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface to get an **IMFMediaSource** pointer.</span></span>
2.  <span data-ttu-id="d93d1-112">Appelez [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) sur la source du média pour obtenir un pointeur vers l’interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="d93d1-112">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media source to get a pointer to the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span> <span data-ttu-id="d93d1-113">Dans le paramètre *guidService* de **MFGetService**, spécifiez la **valeur \_ \_ \_ service du gestionnaire de propriétés MF**.</span><span class="sxs-lookup"><span data-stu-id="d93d1-113">In the *guidService* parameter of **MFGetService**, specify the value **MF\_PROPERTY\_HANDLER\_SERVICE**.</span></span> <span data-ttu-id="d93d1-114">Si la source ne prend pas en charge l’interface **IPropertyStore** , **MFGetService** retourne le **\_ service MF E \_ non pris en charge \_**.</span><span class="sxs-lookup"><span data-stu-id="d93d1-114">If the source does not support the **IPropertyStore** interface, **MFGetService** returns **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
3.  <span data-ttu-id="d93d1-115">Appelez les méthodes [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pour énumérer les propriétés de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="d93d1-115">Call [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) methods to enumerate the metadata properties.</span></span>

<span data-ttu-id="d93d1-116">Le code suivant illustre ces étapes.</span><span class="sxs-lookup"><span data-stu-id="d93d1-116">The following code shows these steps.</span></span> <span data-ttu-id="d93d1-117">Supposons que `DisplayProperty` est une fonction qui affiche une valeur **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="d93d1-117">Assume that `DisplayProperty` is a function that displays a **PROPVARIANT** value.</span></span>


```C++
HRESULT EnumerateMetadata(IMFMediaSource *pSource)
{
    IPropertyStore *pProps = NULL;

    HRESULT hr = MFGetService(
        pSource, MF_PROPERTY_HANDLER_SERVICE, IID_PPV_ARGS(&pProps));

    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cProps;

    hr = pProps->GetCount(&cProps);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cProps; i++)
    {
        PROPERTYKEY key;
        hr = pProps->GetAt(i, &key);
        if (FAILED(hr))
        {
            goto done;
        }

        PROPVARIANT pv;

        hr = pProps->GetValue(key, &pv);
        if (FAILED(hr))
        {
            goto done;
        }

        DisplayProperty(key, pv);
        PropVariantClear(&pv);
    }

done:
    SafeRelease(&pProps);
    return hr;
}
```



<span data-ttu-id="d93d1-118">Pour obtenir la liste des clés de propriété de métadonnées, consultez [Propriétés de métadonnées pour les fichiers multimédias](metadata-properties-for-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="d93d1-118">For a list of metadata property keys, see [Metadata Properties for Media Files](metadata-properties-for-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d93d1-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d93d1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d93d1-120">Métadonnées de média</span><span class="sxs-lookup"><span data-stu-id="d93d1-120">Media Metadata</span></span>](media-metadata.md)
</dt> </dl>

 

 
