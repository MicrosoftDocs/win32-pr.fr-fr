---
title: Acquisition de licence non silencieuse
description: Acquisition de licence non silencieuse
ms.assetid: 3b3fce53-9202-4e55-82d5-7c70ea833087
keywords:
- Windows Media Format SDK, acquisition de licence non silencieuse
- Windows Media Format SDK, licences
- gestion des droits numériques (DRM), acquisition de licence non silencieuse
- DRM (gestion des droits numériques), acquisition de licence non silencieuse
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- API étendues du client DRM, acquisition de licence non silencieuse
- API étendues clientes, acquisition de licence non silencieuse
- acquisition de licence non silencieuse
- licences, acquisition de licence non silencieuse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb8d7c4865e74fd5ce383cff8317de905828afe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507427"
---
# <a name="non-silent-license-acquisition"></a><span data-ttu-id="ca21f-113">Acquisition de licence non silencieuse</span><span class="sxs-lookup"><span data-stu-id="ca21f-113">Non-Silent License Acquisition</span></span>

<span data-ttu-id="ca21f-114">L’acquisition de licence non silencieuse permet au fournisseur de licences d’interagir avec l’utilisateur final par le biais d’une page Web, comme étape intermédiaire du processus d’acquisition de licence.</span><span class="sxs-lookup"><span data-stu-id="ca21f-114">Non-silent license acquisition enables the license provider to interact with the end user through a Web page, as an intermediate step in the license acquisition process.</span></span> <span data-ttu-id="ca21f-115">Une acquisition de licence non silencieuse est lancée en réponse à un utilisateur qui tente d’accéder à du contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="ca21f-115">Non-silent license acquisition is initiated in response to a user trying to access protected content.</span></span>

<span data-ttu-id="ca21f-116">Pour effectuer une acquisition de licence non silencieuse, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="ca21f-116">To perform non-silent license acquisition, use the following steps:</span></span>

1.  <span data-ttu-id="ca21f-117">Appelez la méthode [**IWMDRMLicenseManagement :: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="ca21f-117">Call the [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span> <span data-ttu-id="ca21f-118">Transmettez l’en-tête DRM du fichier protégé en tant que paramètre *bstrHeaderData* .</span><span class="sxs-lookup"><span data-stu-id="ca21f-118">Pass in the DRM header from the protected file as the *bstrHeaderData* parameter.</span></span> <span data-ttu-id="ca21f-119">Spécifiez les droits que vous souhaitez accorder à la licence dans le paramètre *bstrActions* .</span><span class="sxs-lookup"><span data-stu-id="ca21f-119">Specify what rights you want the license to grant in the *bstrActions* parameter.</span></span> <span data-ttu-id="ca21f-120">Enfin, définissez le paramètre *dwFlags* sur WMDRM \_ Acquire \_ License No \_ Silent.</span><span class="sxs-lookup"><span data-stu-id="ca21f-120">Finally, set the *dwFlags* parameter to WMDRM\_ACQUIRE\_LICENSE\_NONSILENT.</span></span>
2.  <span data-ttu-id="ca21f-121">Événements d’interruption de l’interface **IWMDRMLicenseManagement** .</span><span class="sxs-lookup"><span data-stu-id="ca21f-121">Trap events for the **IWMDRMLicenseManagement** interface.</span></span> <span data-ttu-id="ca21f-122">Quand vous recevez l’événement **MEWMDRMLicenseAcquisitionCompleted** , obtenez sa valeur associée en appelant **IMFMediaEvent :: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="ca21f-122">When you receive the **MEWMDRMLicenseAcquisitionCompleted** event, get its associated value by calling **IMFMediaEvent::GetValue**.</span></span> <span data-ttu-id="ca21f-123">La valeur doit être de type VT \_ inconnu, un pointeur vers une interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="ca21f-123">The value should be of type VT\_UNKNOWN, a pointer to an **IUnknown** interface.</span></span>
3.  <span data-ttu-id="ca21f-124">Appelez la méthode **QueryInterface** de l’interface **IUnknown** Récupérée à l’étape 2 pour obtenir l’interface [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) .</span><span class="sxs-lookup"><span data-stu-id="ca21f-124">Call the **QueryInterface** method of the **IUnknown** interface retrieved in step 2 to get the [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) interface.</span></span>
4.  <span data-ttu-id="ca21f-125">Appelez [**IWMDRMNonSilentLicenseAquisition :: GetChallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) pour récupérer la demande de licence.</span><span class="sxs-lookup"><span data-stu-id="ca21f-125">Call [**IWMDRMNonSilentLicenseAquisition::GetChallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) to retrieve the license challenge.</span></span> <span data-ttu-id="ca21f-126">Appelez également [**IWMDRMNonSilentLicenseAquisition :: getURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) si vous n’avez pas déjà l’URL du serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="ca21f-126">Also call [**IWMDRMNonSilentLicenseAquisition::GetURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) if you do not have the URL of the license server already.</span></span>
5.  <span data-ttu-id="ca21f-127">Envoyez la stimulation à la page Web spécifiée par l’URL.</span><span class="sxs-lookup"><span data-stu-id="ca21f-127">Send the challenge to the Web page specified by the URL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca21f-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ca21f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca21f-129">**Acquisition de licences**</span><span class="sxs-lookup"><span data-stu-id="ca21f-129">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="ca21f-130">**Utilisation du modèle d’événement Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="ca21f-130">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 




