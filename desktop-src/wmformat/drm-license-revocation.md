---
title: Révocation de licence (client Microsoft Windows Media DRM)
description: Révocation de licence (client Microsoft Windows Media DRM)
ms.assetid: 615ddddf-4f2f-400d-9c4d-ff3a2851d699
keywords:
- Windows Media Format SDK, licences
- Windows Media Format SDK, révocation de licence
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- gestion des droits numériques (DRM), révocation des licences
- DRM (gestion des droits numériques), révocation de licence
- API étendues du client DRM, licences
- API étendues clientes, licences
- API étendues du client DRM, révocation de licence
- API étendues clientes, révocation de licence
- licences, révocation
- révocation de licence, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90388a7392c79f583143e06fb78ecfe45e188612
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104211176"
---
# <a name="license-revocation-microsoft-windows-media-drm-client"></a><span data-ttu-id="8c8b4-115">Révocation de licence (client Microsoft Windows Media DRM)</span><span class="sxs-lookup"><span data-stu-id="8c8b4-115">License Revocation (Microsoft Windows Media DRM Client)</span></span>

<span data-ttu-id="8c8b4-116">La révocation de licence fait référence à la suppression de licences d’un magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-116">License revocation refers to the removal of licenses from a local license store.</span></span> <span data-ttu-id="8c8b4-117">Un scénario courant de révocation de licence se produit lorsqu’un fournisseur de services, tel qu’un service d’abonnement musical, doit désactiver le service sur l’ordinateur d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-117">A common scenario for license revocation occurs when a service provider, such as a music subscription service, must deactivate the service on a user's computer.</span></span>

<span data-ttu-id="8c8b4-118">Le processus de révocation de licence est initié par un service fourni par l’émetteur de licence.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-118">The license revocation process is initiated by a service provided by the license issuer.</span></span> <span data-ttu-id="8c8b4-119">Votre application peut héberger ce service ou une application Web.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-119">Your application can host this service or it can be a Web application.</span></span> <span data-ttu-id="8c8b4-120">Dans les deux cas, votre application doit être en mesure de recevoir une demande de licence créée par le service.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-120">In either case, your application must be able to receive a license challenge created by the service.</span></span>

<span data-ttu-id="8c8b4-121">Pour supprimer des licences du magasin de licences, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="8c8b4-121">To remove licenses from the license store, do the following:</span></span>

1.  <span data-ttu-id="8c8b4-122">Lors de la réception d’une demande de licence de l’émetteur de licence, créez une demande de révocation à l’aide de la méthode [**IWMDRMLicenseManagement :: CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) .</span><span class="sxs-lookup"><span data-stu-id="8c8b4-122">Upon receiving a license challenge from the license issuer, create a revocation challenge using the [**IWMDRMLicenseManagement::CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) method.</span></span> <span data-ttu-id="8c8b4-123">Cette méthode alloue une mémoire tampon contenant des données de stimulation de révocation, qui est transmise à votre application par le biais du paramètre *ppbChallengeOutput* .</span><span class="sxs-lookup"><span data-stu-id="8c8b4-123">This method will allocate a buffer containing a revocation challenge data, which is passed to your application through the *ppbChallengeOutput* parameter.</span></span>
2.  <span data-ttu-id="8c8b4-124">Envoyez la demande de révocation de licence à un service de révocation de licence.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-124">Send the license revocation challenge to a license revocation service.</span></span> <span data-ttu-id="8c8b4-125">Le serveur génère un objet BLOB de révocation de licence (LRB) en réponse.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-125">The server will generate a license revocation BLOB (LRB) in response.</span></span>
3.  <span data-ttu-id="8c8b4-126">Supprimez la licence du magasin local à l’aide de la méthode [**IWMDRMLicenseManagement ::P rocesslicenserevocationresponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) , en passant le LRB retourné par le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="8c8b4-126">Remove the license from the local store using the [**IWMDRMLicenseManagement::ProcessLicenseRevocationResponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) method, passing the LRB returned by license server.</span></span>
4.  <span data-ttu-id="8c8b4-127">Libérez la mémoire tampon allouée par **CreateLicenseRevocationChallenge** à l’aide de la fonction **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="8c8b4-127">Deallocate the buffer allocated by **CreateLicenseRevocationChallenge** by using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="8c8b4-128">Pour plus d’informations sur le fonctionnement de la révocation des licences ou sur l’écriture d’un service de révocation, consultez Implémentation de la révocation des [licences](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp).</span><span class="sxs-lookup"><span data-stu-id="8c8b4-128">For more information on how license revocation works or on how to write a revocation service, see [Implementing License Revocation](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c8b4-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c8b4-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c8b4-130">**Activation de la prise en charge de DRM**</span><span class="sxs-lookup"><span data-stu-id="8c8b4-130">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="8c8b4-131">**Magasin de licences local**</span><span class="sxs-lookup"><span data-stu-id="8c8b4-131">**Local License Store**</span></span>](local-license-store.md)
</dt> <dt>

[<span data-ttu-id="8c8b4-132">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="8c8b4-132">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 