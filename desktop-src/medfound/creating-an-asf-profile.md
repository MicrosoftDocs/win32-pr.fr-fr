---
description: Cette rubrique explique comment créer en tant que profil ASF dans Microsoft Media Foundation.
ms.assetid: 9633bc88-12bd-404a-b779-878eb1ee5699
title: Création d’un profil ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ed9553811645b8589de7fb1805f1a307c4bdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519243"
---
# <a name="creating-an-asf-profile"></a><span data-ttu-id="4ca46-103">Création d’un profil ASF</span><span class="sxs-lookup"><span data-stu-id="4ca46-103">Creating an ASF Profile</span></span>

<span data-ttu-id="4ca46-104">Cette rubrique explique comment créer en tant que profil ASF dans Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="4ca46-104">This topic describes how to create as ASF profile in Microsoft Media Foundation.</span></span>

-   [<span data-ttu-id="4ca46-105">Créer un nouveau profil</span><span class="sxs-lookup"><span data-stu-id="4ca46-105">Create a New Profile</span></span>](#create-a-new-profile)
-   [<span data-ttu-id="4ca46-106">Récupérer le profil à partir de l’objet ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="4ca46-106">Get the Profile from the ASF ContentInfo Object</span></span>](#get-the-profile-from-the-asf-contentinfo-object)
-   [<span data-ttu-id="4ca46-107">Obtenir le profil à partir d’un descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="4ca46-107">Get the Profile from a Presentation Descriptor</span></span>](#get-the-profile-from-a-presentation-descriptor)
-   [<span data-ttu-id="4ca46-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4ca46-108">Related topics</span></span>](#related-topics)

## <a name="create-a-new-profile"></a><span data-ttu-id="4ca46-109">Créer un nouveau profil</span><span class="sxs-lookup"><span data-stu-id="4ca46-109">Create a New Profile</span></span>

<span data-ttu-id="4ca46-110">Pour créer un profil ASF vide, appelez la fonction [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="4ca46-110">To create an empty ASF profile, call the [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) function.</span></span> <span data-ttu-id="4ca46-111">Cette fonction retourne un pointeur vers l’interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="4ca46-111">This function returns a pointer to the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span> <span data-ttu-id="4ca46-112">L’application peut utiliser cette interface pour ajouter des flux au profil et configurer chacun des flux.</span><span class="sxs-lookup"><span data-stu-id="4ca46-112">The application can use this interface to add streams to the profile, and to configure each of the streams.</span></span> <span data-ttu-id="4ca46-113">Pour plus d’informations, consultez [création et configuration de flux ASF](creating-and-configuring-asf-streams.md).</span><span class="sxs-lookup"><span data-stu-id="4ca46-113">For more information, see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md).</span></span>

<span data-ttu-id="4ca46-114">L’application peut éventuellement ajouter des objets d’exclusion mutuelle à deux flux ou plus.</span><span class="sxs-lookup"><span data-stu-id="4ca46-114">Optionally, the application can add mutual-exclusion objects to two or more streams.</span></span> <span data-ttu-id="4ca46-115">Consultez [utilisation de l’exclusion mutuelle pour les flux ASF](using-mutual-exclusion-for-asf-streams.md).</span><span class="sxs-lookup"><span data-stu-id="4ca46-115">See [Using Mutual Exclusion for ASF Streams](using-mutual-exclusion-for-asf-streams.md).</span></span>

## <a name="get-the-profile-from-the-asf-contentinfo-object"></a><span data-ttu-id="4ca46-116">Récupérer le profil à partir de l’objet ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="4ca46-116">Get the Profile from the ASF ContentInfo Object</span></span>

<span data-ttu-id="4ca46-117">Une application peut récupérer le profil ASF d’un fichier ASF existant à partir de l' [objet ASF ContentInfo](asf-contentinfo-object.md).</span><span class="sxs-lookup"><span data-stu-id="4ca46-117">An application can get the ASF profile of an existing ASF file from the [ASF ContentInfo Object](asf-contentinfo-object.md).</span></span> <span data-ttu-id="4ca46-118">Le profil est déjà configuré et contient des paramètres pour tous les flux du fichier.</span><span class="sxs-lookup"><span data-stu-id="4ca46-118">The profile is already configured and contains settings for the all of the streams in the file.</span></span>

<span data-ttu-id="4ca46-119">Initialisez l’objet ContentInfo en analysant l’objet d’en-tête ASF du fichier.</span><span class="sxs-lookup"><span data-stu-id="4ca46-119">Initialize the ContentInfo object by parsing the ASF Header Object of the file.</span></span> <span data-ttu-id="4ca46-120">Cela s’effectue par le biais de la méthode [**IMFASFContentInfo ::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="4ca46-120">This is done through the [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span> <span data-ttu-id="4ca46-121">Une fois tous les objets d’en-tête lus et la bibliothèque ASF remplie, le profil de ce fichier est généré.</span><span class="sxs-lookup"><span data-stu-id="4ca46-121">After all the Header Objects are read and the ASF library is populated, the profile for this file is generated.</span></span> <span data-ttu-id="4ca46-122">L’application peut obtenir un pointeur vers ce profil initialisé en appelant [**IMFASFContentInfo :: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="4ca46-122">The application can get a pointer to this initialized profile by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span>

## <a name="get-the-profile-from-a-presentation-descriptor"></a><span data-ttu-id="4ca46-123">Obtenir le profil à partir d’un descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="4ca46-123">Get the Profile from a Presentation Descriptor</span></span>

<span data-ttu-id="4ca46-124">Vous pouvez obtenir l’objet de profil d’un fichier ASF existant à partir du [descripteur de présentation](presentation-descriptors.md) pour le fichier ou à partir de l’objet [ASF ContentInfo](asf-contentinfo-object.md) .</span><span class="sxs-lookup"><span data-stu-id="4ca46-124">You can get the profile object of an existing ASF file from the [presentation descriptor](presentation-descriptors.md) for the file, or from the [ASF ContentInfo](asf-contentinfo-object.md) object.</span></span> <span data-ttu-id="4ca46-125">Dans ce cas, le profil est déjà configuré et contient des paramètres pour tous les flux du fichier.</span><span class="sxs-lookup"><span data-stu-id="4ca46-125">In this case, the profile is already configured and contains settings for all of the streams in the file.</span></span> <span data-ttu-id="4ca46-126">Cela peut être utile si vous souhaitez modifier un profil ASF existant.</span><span class="sxs-lookup"><span data-stu-id="4ca46-126">This can be useful if you want to modify an existing ASF profile.</span></span> <span data-ttu-id="4ca46-127">Par exemple, vous souhaiterez peut-être recoder un fichier de Windows Media Video à une vitesse de transmission inférieure.</span><span class="sxs-lookup"><span data-stu-id="4ca46-127">For example, you might wish to re-encode a Windows Media Video file at a lower bit rate.</span></span>

<span data-ttu-id="4ca46-128">Pour récupérer le profil à partir du descripteur de présentation, appelez [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="4ca46-128">To get the profile from the presentation descriptor, call [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor).</span></span> <span data-ttu-id="4ca46-129">Cette fonction analyse le descripteur de présentation et remplit un profil ASF avec des informations sur le fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="4ca46-129">This function parses the presentation descriptor, and populates an ASF profile with information about the media file.</span></span> <span data-ttu-id="4ca46-130">La fonction retourne un pointeur vers l’interface IMFASFProfile.</span><span class="sxs-lookup"><span data-stu-id="4ca46-130">The function returns a pointer to the IMFASFProfile interface.</span></span> <span data-ttu-id="4ca46-131">Vous pouvez ensuite utiliser cette interface pour modifier le profil.</span><span class="sxs-lookup"><span data-stu-id="4ca46-131">You can then use this interface to modify the profile.</span></span>

<span data-ttu-id="4ca46-132">Pour récupérer le descripteur de présentation, appelez l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4ca46-132">To get the presentation descriptor, call one of the following methods:</span></span>

-   <span data-ttu-id="4ca46-133">À partir de la source de média ASF, appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="4ca46-133">From the ASF media source, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>
-   <span data-ttu-id="4ca46-134">À partir de l’objet [ASF ContentInfo](asf-contentinfo-object.md) , appelez [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="4ca46-134">From the [ASF ContentInfo](asf-contentinfo-object.md) object, call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="4ca46-135">Avant d’appeler cette méthode, assurez-vous que l’objet ContentInfo est initialisé pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="4ca46-135">Prior to calling this method, make sure that the ContentInfo object is initialized for reading.</span></span> <span data-ttu-id="4ca46-136">Pour plus d’informations, consultez « initialisation de l’objet ContentInfo à partir d’un fichier ASF existant » dans [lecture de l’objet d’en-tête ASF d’un fichier existant](reading-the-asf-header-object-of-an-existing-file.md).</span><span class="sxs-lookup"><span data-stu-id="4ca46-136">For more information, see "Initializing the ContentInfo Object from an Existing ASF File" in [Reading the ASF Header Object of an Existing File](reading-the-asf-header-object-of-an-existing-file.md).</span></span> <span data-ttu-id="4ca46-137">Toutefois, si vous disposez déjà d’un objet ContentInfo initialisé, vous pouvez obtenir le profil directement à partir de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="4ca46-137">However, if you already have an initialized ContentInfo object, you can get the profile directly from it.</span></span> <span data-ttu-id="4ca46-138">Cela est décrit dans la section « obtention du profil à partir de l’objet ContentInfo », plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="4ca46-138">This is described in "Getting the Profile from the ContentInfo Object " later in this topic.</span></span>

<span data-ttu-id="4ca46-139">L’exemple suivant montre comment créer un profil à partir d’un descripteur de présentation.</span><span class="sxs-lookup"><span data-stu-id="4ca46-139">The following example shows how to create a profile from a presentation descriptor.</span></span> <span data-ttu-id="4ca46-140">La fonction crée une source de média pour le fichier, obtient le descripteur de présentation à partir de la source du média et crée un profil.</span><span class="sxs-lookup"><span data-stu-id="4ca46-140">The function creates a media source for the file, gets the presentation descriptor from the media source, and creates a profile.</span></span> <span data-ttu-id="4ca46-141">Cet exemple suppose que *pszFileName* spécifie l’URL d’un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="4ca46-141">This example assumes that *pszFileName* specifies the URL of an ASF file.</span></span>


```C++
HRESULT GetASFProfile(PCWSTR pszFileName, IMFASFProfile** ppProfile)
{
    *ppProfile = NULL;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSourceUnk = NULL;
    IMFMediaSource* pSource = NULL;
    IMFPresentationDescriptor* pPD = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        hr = pResolver->CreateObjectFromURL(
                pszFileName,
                MF_RESOLUTION_MEDIASOURCE, 
                NULL,                      
                &ObjectType,               
                &pSourceUnk   
            );
    }

    // Get the IMFMediaSource interface from the media source.
    if (SUCCEEDED(hr))
    {
        hr = pSourceUnk->QueryInterface(IID_PPV_ARGS(&pSource));
    }

    // Get the presentation desccriptor.
    if (SUCCEEDED(hr))
    {
        hr = pSource->CreatePresentationDescriptor(&pPD);
    }

    // Get the profile from the presentation descriptor.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFProfileFromPresentationDescriptor(pPD, ppProfile);
    }

    SafeRelease(&pResolver);
    SafeRelease(&pSourceUnk);
    SafeRelease(&pSource);
    SafeRelease(&pPD);
    return hr;
}
```



<span data-ttu-id="4ca46-142">Cet exemple utilise [SafeRelease](saferelease.md) pour libérer des pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="4ca46-142">This example uses [SafeRelease](saferelease.md) to release interface pointers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ca46-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4ca46-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ca46-144">Profil ASF</span><span class="sxs-lookup"><span data-stu-id="4ca46-144">ASF Profile</span></span>](asf-profile.md)
</dt> </dl>

 

 



