---
description: Configuration d’une source de média
ms.assetid: 1378bbe6-be94-4be1-b428-5ec58dabd1fa
title: Configuration d’une source de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea741e3c04282af445fbea7be07854bf517ec44f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106523756"
---
# <a name="configuring-a-media-source"></a><span data-ttu-id="2989e-103">Configuration d’une source de média</span><span class="sxs-lookup"><span data-stu-id="2989e-103">Configuring a Media Source</span></span>

<span data-ttu-id="2989e-104">Lorsque vous utilisez le programme de [résolution source](source-resolver.md) pour créer une source de média, vous pouvez spécifier une banque de propriétés qui contient les propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="2989e-104">When you use the [Source Resolver](source-resolver.md) to create a media source, you can specify a property store that contains configuration properties.</span></span> <span data-ttu-id="2989e-105">Ces propriétés sont utilisées pour initialiser la source du média.</span><span class="sxs-lookup"><span data-stu-id="2989e-105">These properties will be used to initialize the media source.</span></span> <span data-ttu-id="2989e-106">L’ensemble des propriétés prises en charge dépend de l’implémentation de la source du média.</span><span class="sxs-lookup"><span data-stu-id="2989e-106">The set of supported properties depends on the implementation of the media source.</span></span> <span data-ttu-id="2989e-107">Toutes les sources de média ne définissent pas les propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="2989e-107">Not every media source defines configuration properties.</span></span>

<span data-ttu-id="2989e-108">Le tableau suivant répertorie les propriétés de configuration des sources de média fournies dans Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2989e-108">The following table lists the configuration properties for the media sources that are provided in Media Foundation.</span></span> <span data-ttu-id="2989e-109">Les sources de média tierces peuvent définir leurs propres propriétés personnalisées.</span><span class="sxs-lookup"><span data-stu-id="2989e-109">Third-party media sources can define their own custom properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2989e-110">Source du média</span><span class="sxs-lookup"><span data-stu-id="2989e-110">Media source</span></span></th>
<th><span data-ttu-id="2989e-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2989e-111">Properties</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2989e-112">Source réseau</span><span class="sxs-lookup"><span data-stu-id="2989e-112">Network source</span></span></td>
<td><span data-ttu-id="2989e-113">Voir <a href="network-source-features.md">fonctionnalités de la source réseau</a>.</span><span class="sxs-lookup"><span data-stu-id="2989e-113">See <a href="network-source-features.md">Network Source Features</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2989e-114">Source de média ASF</span><span class="sxs-lookup"><span data-stu-id="2989e-114">ASF media source</span></span></td>
<td><ul>
<li><span data-ttu-id="2989e-115"><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></span><span class="sxs-lookup"><span data-stu-id="2989e-115"><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></span></span></li>
<li><span data-ttu-id="2989e-116"><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></span><span class="sxs-lookup"><span data-stu-id="2989e-116"><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></span></span></li>
<li><span data-ttu-id="2989e-117"><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></span><span class="sxs-lookup"><span data-stu-id="2989e-117"><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></span></span></li>
<li><span data-ttu-id="2989e-118"><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></span><span class="sxs-lookup"><span data-stu-id="2989e-118"><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2989e-119">Pour configurer une source, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="2989e-119">To configure a source, perform the following steps.</span></span>

1.  <span data-ttu-id="2989e-120">Appelez **PSCreateMemoryPropertyStore** pour créer une banque de propriétés.</span><span class="sxs-lookup"><span data-stu-id="2989e-120">Call **PSCreateMemoryPropertyStore** to create a new property store.</span></span> <span data-ttu-id="2989e-121">Cette fonction retourne un pointeur **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="2989e-121">This function returns an **IPropertyStore** pointer.</span></span>
2.  <span data-ttu-id="2989e-122">Appelez **IPropertyStore :: SetValue** pour définir une ou plusieurs propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="2989e-122">Call **IPropertyStore::SetValue** to set one or more configuration properties.</span></span>
3.  <span data-ttu-id="2989e-123">Appelez l’une des fonctions de création du programme de résolution source, telles que [**IMFSourceResolver :: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), et transmettez le pointeur **IPropertyStore** dans le paramètre *pProps* .</span><span class="sxs-lookup"><span data-stu-id="2989e-123">Call one of the source resolver's creation functions, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), and pass the **IPropertyStore** pointer in the *pProps* parameter.</span></span>


```C++
// Creates a media source from a URL.

HRESULT CreateMediaSource(
    PCWSTR pszURL, 
    IPropertyStore *pConfig,    // Optional, can be NULL
    IMFMediaSource **ppSource
    )
{
    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        DbgLog(L"CreateObjectFromURL");

        hr = pSourceResolver->CreateObjectFromURL(
            pszURL,                     
            MF_RESOLUTION_MEDIASOURCE,  // Create a media source.
            pConfig,                    // Configuration properties.
            &ObjectType,                // Receives the object type. 
            &pSource            
            );

        DbgLog(L"CreateObjectFromURL - FINISHED");

    }

    if (SUCCEEDED(hr))
    {
        hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));
    }

    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



<span data-ttu-id="2989e-124">Le programme de résolution source transmet directement le pointeur **IPropertyStore** au gestionnaire de schéma ou au gestionnaire de flux d’octets qui crée la source.</span><span class="sxs-lookup"><span data-stu-id="2989e-124">The source resolver passes the **IPropertyStore** pointer directly to the scheme handler or byte-stream handler that creates the source.</span></span> <span data-ttu-id="2989e-125">Le programme de résolution source n’effectue aucune tentative de validation des propriétés.</span><span class="sxs-lookup"><span data-stu-id="2989e-125">The source resolver makes no attempt to validate the properties.</span></span>

<span data-ttu-id="2989e-126">En règle générale, ces propriétés sont utilisées pour les paramètres avancés.</span><span class="sxs-lookup"><span data-stu-id="2989e-126">Generally, these properties are used for advanced settings.</span></span> <span data-ttu-id="2989e-127">Si vous ne fournissez pas de banque de propriétés, la source du média doit toujours fonctionner correctement avec les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="2989e-127">If you don't provide a property store, the media source should still function correctly with default settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2989e-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2989e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2989e-129">Résolveur source</span><span class="sxs-lookup"><span data-stu-id="2989e-129">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



