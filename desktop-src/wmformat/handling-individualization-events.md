---
title: Gestion des événements d’individualisation
description: Gestion des événements d’individualisation
ms.assetid: f533978f-f366-4900-b784-f51e88393984
keywords:
- Windows Media Format SDK, gestion des événements d’individualisation
- Windows Media Format SDK, événements d’individualisation
- ASF (Advanced Systems Format), gestion des événements d’individualisation
- ASF (format de systèmes avancés), gestion des événements d’individualisation
- ASF (Advanced Systems Format), événements de individualisation
- ASF (format des systèmes avancés), événements d’individualisation
- gestion des droits numériques (DRM), gestion des événements d’individualisation
- DRM (gestion des droits numériques), gestion des événements d’individualisation
- gestion des droits numériques (DRM), événements d’individualisation
- DRM (gestion des droits numériques), événements d’individualisation
- événements d’individualisation
- événements, événements d’individualisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e74df94bf871ec62ec2acb94658785969812640
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106512715"
---
# <a name="handling-individualization-events"></a><span data-ttu-id="93f01-115">Gestion des événements d’individualisation</span><span class="sxs-lookup"><span data-stu-id="93f01-115">Handling Individualization Events</span></span>

<span data-ttu-id="93f01-116">Lorsqu’une application DRM tente d’ouvrir un fichier protégé, le composant DRM examine l’attribut [**\_ \_ IndividualizedVersion DRM DRMHeader**](drm-drmheader-individualizedversion.md) dans le fichier, qui spécifie le niveau de version minimal requis pour accéder au contenu.</span><span class="sxs-lookup"><span data-stu-id="93f01-116">When a DRM-enabled application attempts to open a protected file, the DRM component examines the [**DRM\_DRMHeader\_IndividualizedVersion**](drm-drmheader-individualizedversion.md) attribute in the file, which specifies the minimum version level required to access the content.</span></span> <span data-ttu-id="93f01-117">Tous les niveaux du composant DRM fonctionnent avec toutes les versions 7,0 et ultérieures du lecteur Windows Media et du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="93f01-117">All levels of the DRM component work with all 7.0 and later versions of Windows Media Player and the Windows Media Format SDK.</span></span> <span data-ttu-id="93f01-118">Si le niveau de version individualisé du composant DRM est inférieur à la version requise, le composant DRM enverra un événement **d' \_ \_ individualisation** à la méthode [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) de l’application.</span><span class="sxs-lookup"><span data-stu-id="93f01-118">If the DRM component's individualized version level is lower than the required version, the DRM component will send a **WMT\_NEEDS\_INDIVIDUALIZATION** event to the application's [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="93f01-119">L’application doit ensuite afficher un message ou une boîte de dialogue invitant les utilisateurs à démarrer ou à annuler la mise à niveau de sécurité.</span><span class="sxs-lookup"><span data-stu-id="93f01-119">The application must then display a message or dialog box prompting users to either start or cancel the security upgrade.</span></span> <span data-ttu-id="93f01-120">Cette invite est nécessaire car, pour des raisons de confidentialité, les utilisateurs doivent donner leur autorisation avant l’installation d’une mise à niveau de sécurité sur leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="93f01-120">This prompt is necessary because, for privacy reasons, users must give their permission before a security upgrade is installed on their computer.</span></span>

> [!Note]  
> <span data-ttu-id="93f01-121">L’en-tête du contenu spécifie uniquement les deux premiers chiffres pour DRM \_ DRMVersion \_ IndividualizedVersion.</span><span class="sxs-lookup"><span data-stu-id="93f01-121">The header of the content specifies only the first two digits for DRM\_DRMVersion\_IndividualizedVersion.</span></span> <span data-ttu-id="93f01-122">En d’autres termes, pour exiger un composant DRM de niveau 2.2.0.1, l’en-tête contient « 2,2 ».</span><span class="sxs-lookup"><span data-stu-id="93f01-122">In other words, to require a level 2.2.0.1 DRM component, the header would contain "2.2".</span></span>

 

<span data-ttu-id="93f01-123">Pour démarrer la mise à niveau de sécurité et/ou déclencher l’individualisation, appelez la méthode [**IWMDRMReader :: Individual**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) avec le paramètre *dwFlags* défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="93f01-123">To start the security upgrade and/or trigger individualization, call the [**IWMDRMReader::Individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) method with the *dwFlags* parameter set to 1.</span></span>

<span data-ttu-id="93f01-124">Vous devez gérer l' **événement \_ Individual WMT** dans votre application.</span><span class="sxs-lookup"><span data-stu-id="93f01-124">You must handle the **WMT\_INDIVIDUALIZE** event in your application.</span></span> <span data-ttu-id="93f01-125">Cet événement est déclenché plusieurs fois par le composant DRM avec l’état du processus d’individualisation indiqué dans le paramètre *pValue* , qui est converti en pointeur vers une structure d' [**État de l' \_ individualisation \_ WM**](wm-individualize-status.md) .</span><span class="sxs-lookup"><span data-stu-id="93f01-125">This event will be fired multiple times by the DRM component with the status of the individualization process indicated in the *pValue* parameter, which is cast to a pointer to a [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

<span data-ttu-id="93f01-126">Une fois le composant DRM correctement individualisé, l’application reçoit un événement **WMT \_ no \_ Rights \_ ex** , qui indique que l’application peut maintenant continuer à acquérir une licence pour le contenu.</span><span class="sxs-lookup"><span data-stu-id="93f01-126">After the DRM component is successfully individualized, the application will receive a **WMT\_NO\_RIGHTS\_EX** event, indicating that the application can now proceed to acquire a license for the content.</span></span>

> [!Note]  
> <span data-ttu-id="93f01-127">DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="93f01-127">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="93f01-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="93f01-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93f01-129">**Gestion des événements d’acquisition de licence**</span><span class="sxs-lookup"><span data-stu-id="93f01-129">**Handling License Acquisition Events**</span></span>](handling-license-acquisition-events.md)
</dt> <dt>

[<span data-ttu-id="93f01-130">**Individualiser des applications DRM**</span><span class="sxs-lookup"><span data-stu-id="93f01-130">**Individualizing DRM Applications**</span></span>](individualizing-drm-applications.md)
</dt> <dt>

[<span data-ttu-id="93f01-131">**Interface IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="93f01-131">**IWMDRMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> </dl>

 

 




