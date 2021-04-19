---
description: Les informations d’en-tête ASF sont stockées dans les objets d’en-tête ASF d’un fichier multimédia.
ms.assetid: 1654af97-f4fe-427f-b562-3b109e921719
title: Obtention d’informations à partir d’objets d’en-tête ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f25155929c9e3ba7e59ee1b5f46ea7c5930c3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514556"
---
# <a name="getting-information-from-asf-header-objects"></a><span data-ttu-id="957ab-103">Obtention d’informations à partir d’objets d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="957ab-103">Getting Information from ASF Header Objects</span></span>

<span data-ttu-id="957ab-104">Les informations d’en-tête ASF sont stockées dans les objets d’en-tête ASF d’un fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="957ab-104">ASF header information is stored in the ASF Header Objects of a media file.</span></span> <span data-ttu-id="957ab-105">Media Foundation fournit l' [objet ASF ContentInfo](asf-contentinfo-object.md) pour fonctionner avec l’objet d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="957ab-105">Media Foundation provides the [ASF ContentInfo Object](asf-contentinfo-object.md) to work with the Header Object.</span></span> <span data-ttu-id="957ab-106">Un objet ContentInfo rempli est requis pour permettre à l’application de lire les informations d’en-tête d’un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="957ab-106">A populated ContentInfo object is required in order for the application to read header information of an existing file.</span></span> <span data-ttu-id="957ab-107">Pour ce faire, appelez [**IMFASFContentInfo ::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span><span class="sxs-lookup"><span data-stu-id="957ab-107">This is achieved by calling [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span></span> <span data-ttu-id="957ab-108">Si l’analyse se termine correctement, la bibliothèque ASF du fichier, qui est géré en interne par Media Foundation, est remplie avec les informations d’en-tête de divers objets d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="957ab-108">If parsing completes successfully, the ASF library for the file, which is maintained internally by Media Foundation, is populated with header information from various Header Objects.</span></span> <span data-ttu-id="957ab-109">Certaines de ces propriétés sont exposées à l’application, qu’elle peut récupérer via des attributs du descripteur de présentation, du descripteur de flux, du profil et des propriétés de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="957ab-109">Some of these properties are exposed to the application, which it can retrieve through attributes on the presentation descriptor, stream descriptor, the profile, and metadata properties.</span></span>

<span data-ttu-id="957ab-110">Pour obtenir la liste complète des attributs, consultez [Media Foundation attributs pour les objets d’en-tête ASF](media-foundation-attributes-for-asf-header-objects.md).</span><span class="sxs-lookup"><span data-stu-id="957ab-110">For the complete list of attributes, see [Media Foundation Attributes for ASF Header Objects](media-foundation-attributes-for-asf-header-objects.md).</span></span>

## <a name="retrieving-header-information-from-a-presentation-descriptor"></a><span data-ttu-id="957ab-111">Récupération d’informations d’en-tête à partir d’un descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="957ab-111">Retrieving Header Information from a Presentation Descriptor</span></span>

<span data-ttu-id="957ab-112">Un objet descripteur de présentation contient la description d’une source multimédia particulière, dans ce cas, la source du média ASF.</span><span class="sxs-lookup"><span data-stu-id="957ab-112">A presentation descriptor object contains the description of a particular media source, in this case the ASF media source.</span></span> <span data-ttu-id="957ab-113">Si l’appel **ParseHeader** se termine correctement, les informations au niveau du fichier de l’objet d’en-tête sont stockées en tant qu’attributs sur le descripteur de présentation.</span><span class="sxs-lookup"><span data-stu-id="957ab-113">If the **ParseHeader** call completes successfully, file-level information from the Header Object is stored as attributes on the presentation descriptor.</span></span> <span data-ttu-id="957ab-114">Pour créer le descripteur de présentation, appelez [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="957ab-114">To create the presentation descriptor, call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="957ab-115">Cette méthode retourne un pointeur vers un objet de descripteur de présentation rempli qui contient ces attributs pour le fichier ASF associé à l’objet ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="957ab-115">This method returns a pointer to a populated presentation descriptor object that contains these attributes for the ASF file associated with the ContentInfo object.</span></span> <span data-ttu-id="957ab-116">Pour obtenir des valeurs pour des attributs spécifiques, appelez les méthodes **IMFAttributes :: GetXXX** sur le descripteur de présentation et spécifiez l’attribut **MF \_ PD \_ ASF \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="957ab-116">To get values for specific attributes, call **IMFAttributes::Getxxx** methods on the presentation descriptor and specify the **MF\_PD\_ASF\_xxx** attribute.</span></span>

<span data-ttu-id="957ab-117">L’exemple de code suivant récupère la durée de lecture d’un fichier ASF, spécifiée par un objet ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="957ab-117">The following example code retrieves the play duration of an ASF file, specified by a ContentInfo object.</span></span>


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



<span data-ttu-id="957ab-118">Pour plus d’informations sur les descripteurs de présentation en général, consultez [descripteurs de présentation](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="957ab-118">For more information about presentation descriptors in general, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

<span data-ttu-id="957ab-119">Pour obtenir l’ensemble complet des attributs du descripteur de présentation, consultez [attributs du descripteur de présentation](presentation-descriptor-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="957ab-119">For the complete set of presentation descriptor attributes, see [Presentation Descriptor Attributes](presentation-descriptor-attributes.md).</span></span>

## <a name="retrieving-header-information-from-a-stream-descriptor"></a><span data-ttu-id="957ab-120">Récupération d’informations d’en-tête à partir d’un descripteur de flux</span><span class="sxs-lookup"><span data-stu-id="957ab-120">Retrieving Header Information from a Stream Descriptor</span></span>

<span data-ttu-id="957ab-121">Un objet descripteur de flux expose l’interface [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) et décrit les caractéristiques des flux dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="957ab-121">A stream descriptor object exposes the [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) interface and describes the characteristics of the streams in the file.</span></span> <span data-ttu-id="957ab-122">Le descripteur de présentation pour le contenu ASF contient un ou plusieurs descripteurs de flux qui représentent les flux listés dans l’objet d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="957ab-122">The presentation descriptor for the ASF content contains one or more stream descriptors that represent the streams listed in the Header Object.</span></span> <span data-ttu-id="957ab-123">Une fois l’appel à [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) terminé, les descripteurs de flux sous-jacents sont remplis avec les informations au niveau du flux des différents objets d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="957ab-123">After the call to [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) completes successfully, the underlying stream descriptors are populated with stream-level information from the various Header Objects.</span></span> <span data-ttu-id="957ab-124">Pour obtenir un descripteur de flux pour un flux ASF, appelez [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) sur le descripteur de présentation généré à partir de l’objet ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="957ab-124">To get a stream descriptor for an ASF stream, call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) on the presentation descriptor that is generated from the ContentInfo object.</span></span>

<span data-ttu-id="957ab-125">Certaines propriétés de flux sont définies en tant qu’attributs sur les descripteurs de flux.</span><span class="sxs-lookup"><span data-stu-id="957ab-125">Some of the stream properties are set as attributes on stream descriptors.</span></span> <span data-ttu-id="957ab-126">Appelez les méthodes **IMFAttributes :: GetXXX** sur un descripteur de flux et spécifiez l’attribut **MF \_ SD \_ ASF \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="957ab-126">Call **IMFAttributes::Getxxx** methods on a stream descriptor and specify the **MF\_SD\_ASF\_xxx** attribute.</span></span>

<span data-ttu-id="957ab-127">Pour obtenir l’ensemble complet des attributs du descripteur de flux, consultez « descripteur de flux spécifique aux ASF » dans [attributs du descripteur de flux](stream-descriptor-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="957ab-127">For the complete set of stream descriptor attributes, see "ASF-Specific Stream Descriptor" attributes listed in [Stream Descriptor Attributes](stream-descriptor-attributes.md).</span></span>

## <a name="retrieving-header-information-from-the-profile-object"></a><span data-ttu-id="957ab-128">Récupération des informations d’en-tête de l’objet de profil</span><span class="sxs-lookup"><span data-stu-id="957ab-128">Retrieving Header Information from the Profile Object</span></span>

<span data-ttu-id="957ab-129">Outre les descripteurs de flux, l’objet de profil ASF décrit également les propriétés de flux.</span><span class="sxs-lookup"><span data-stu-id="957ab-129">In addition to stream descriptors, the ASF profile object also describes the stream properties.</span></span> <span data-ttu-id="957ab-130">Pour récupérer le profil d’un fichier ASF existant, appelez [**IMFASFContentInfo :: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="957ab-130">To get the profile of an existing ASF file, call [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span> <span data-ttu-id="957ab-131">L’objet de profil ASF retourné par cette méthode n’inclut aucun des attributs **MF \_ PD \_ ASF \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="957ab-131">The ASF profile object returned by this method does not include any of the **MF\_PD\_ASF\_xxx** attributes.</span></span> <span data-ttu-id="957ab-132">Ces attributs sont disponibles pour l’application uniquement après avoir appelé [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) pour générer l’objet de profil à partir d’un descripteur de présentation.</span><span class="sxs-lookup"><span data-stu-id="957ab-132">These attributes are available to the application only after it calls [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) to generate the profile object from a presentation descriptor.</span></span> <span data-ttu-id="957ab-133">Vous pouvez utiliser le profil pour atteindre des pointeurs vers les objets d’exclusion mutuelle et de priorité de flux.</span><span class="sxs-lookup"><span data-stu-id="957ab-133">You can use the profile to get pointers to the mutual exclusion and stream prioritization objects.</span></span>

<span data-ttu-id="957ab-134">Pour plus d’informations sur l’objet profil, consultez [ASF Profile](asf-profile.md) .</span><span class="sxs-lookup"><span data-stu-id="957ab-134">For information about the profile object, see [ASF Profile](asf-profile.md) .</span></span>

## <a name="retrieving-metadata-from-header-objects"></a><span data-ttu-id="957ab-135">Récupération de métadonnées à partir d’objets d’en-tête</span><span class="sxs-lookup"><span data-stu-id="957ab-135">Retrieving Metadata from Header Objects</span></span>

<span data-ttu-id="957ab-136">Un fichier ASF peut contenir plusieurs propriétés de métadonnées qui sont définies lors de l’encodage du fichier.</span><span class="sxs-lookup"><span data-stu-id="957ab-136">An ASF file can contain several metadata properties that are set during file encoding.</span></span> <span data-ttu-id="957ab-137">Une application peut énumérer ces propriétés avec l’objet ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="957ab-137">An application can enumerate these properties with the ContentInfo object.</span></span> <span data-ttu-id="957ab-138">Certaines de ces propriétés, telles que les informations VBR (variable bit rate), sont disponibles pour l’application via des attributs sur le descripteur de présentation, les descripteurs de flux et les types de média pour le fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="957ab-138">Some of these properties, such as variable bit rate (VBR) information, are available to the application through attributes on presentation descriptor, stream descriptors, and media types for the media file.</span></span> <span data-ttu-id="957ab-139">Ces attributs sont définis sur l’objet ContentInfo pendant l’initialisation via l’appel [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="957ab-139">These attributes are set on the ContentInfo object during initialization through the [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="957ab-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="957ab-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="957ab-141">Objet ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="957ab-141">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> </dl>

 

 



