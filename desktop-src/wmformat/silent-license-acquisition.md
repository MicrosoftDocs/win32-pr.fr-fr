---
title: Acquisition de licence en mode silencieux
description: Acquisition de licence en mode silencieux
ms.assetid: bf88f1bb-0cbb-4c30-92e0-3d342977d67f
keywords:
- Windows Media Format SDK, acquisition de licence en mode silencieux
- Windows Media Format SDK, licences
- gestion des droits numériques (DRM), acquisition de licence en mode silencieux
- DRM (gestion des droits numériques), acquisition de licence en mode silencieux
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- API étendues du client DRM, acquisition de licence silencieuse
- API étendues clientes, acquisition de licence silencieuse
- acquisition de licence en mode silencieux
- licences, acquisition de licence silencieuse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ef92eaf4e347e8eb30f56c1111ec5b27f1e62d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029498"
---
# <a name="silent-license-acquisition"></a><span data-ttu-id="7b1c3-113">Acquisition de licence en mode silencieux</span><span class="sxs-lookup"><span data-stu-id="7b1c3-113">Silent License Acquisition</span></span>

<span data-ttu-id="7b1c3-114">L’acquisition de licence en mode silencieux requiert un seul appel de méthode qui gère toutes les communications réseau avec le serveur de licences de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="7b1c3-114">Silent license acquisition requires only a single method call that handles all of the network communications with the license server asynchronously.</span></span>

<span data-ttu-id="7b1c3-115">Ce type d’acquisition de licence est généralement utilisé comme réponse à l’utilisateur final tentant d’accéder au contenu protégé, par exemple en tentant de lire un fichier protégé dans une application de lecteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="7b1c3-115">This type of license acquisition is usually used as a response to the end user trying to access protected content—for example, trying to play a protected file in a media player application.</span></span> <span data-ttu-id="7b1c3-116">Étant donné que l’acquisition de licence en mode silencieux obtient la licence avec un appel unique, elle ne peut pas être utilisée si une entrée supplémentaire de l’utilisateur, telle que le paiement du contenu, est requise.</span><span class="sxs-lookup"><span data-stu-id="7b1c3-116">Because silent license acquisition gets the license with a single call, it cannot be used if additional input from the user, such as payment for the content, is required.</span></span>

<span data-ttu-id="7b1c3-117">Pour effectuer une acquisition de licence en mode silencieux, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7b1c3-117">To perform silent license acquisition, use the following steps:</span></span>

1.  <span data-ttu-id="7b1c3-118">Appelez la méthode [**IWMDRMLicenseManagement :: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="7b1c3-118">Call the [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span> <span data-ttu-id="7b1c3-119">Transmettez l’en-tête DRM du fichier protégé en tant que paramètre *bstrHeaderData* .</span><span class="sxs-lookup"><span data-stu-id="7b1c3-119">Pass in the DRM header from the protected file as the *bstrHeaderData* parameter.</span></span> <span data-ttu-id="7b1c3-120">Spécifiez les droits que vous souhaitez accorder à la licence dans le paramètre *bstrActions* .</span><span class="sxs-lookup"><span data-stu-id="7b1c3-120">Specify what rights you want the license to grant in the *bstrActions* parameter.</span></span> <span data-ttu-id="7b1c3-121">Enfin, définissez le paramètre *dwFlags* sur WMDRM \_ Acquire \_ licence \_ Silent.</span><span class="sxs-lookup"><span data-stu-id="7b1c3-121">Finally, set the *dwFlags* parameter to WMDRM\_ACQUIRE\_LICENSE\_SILENT.</span></span>
2.  <span data-ttu-id="7b1c3-122">Événements d’interruption de l’interface [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) .</span><span class="sxs-lookup"><span data-stu-id="7b1c3-122">Trap events for the [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) interface.</span></span> <span data-ttu-id="7b1c3-123">Quand vous recevez l’événement **MEWMDRMLicenseAcquisitionCompleted** , vérifiez son code de retour en appelant la méthode **IMFMediaEvent :: GetStatus** , qui est documentée dans la documentation de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="7b1c3-123">When you receive the **MEWMDRMLicenseAcquisitionCompleted** event, check its return code by calling the **IMFMediaEvent::GetStatus** method, which is documented in the Media Foundation documentation.</span></span> <span data-ttu-id="7b1c3-124">Si la valeur **HRESULT** Récupérée est un code de réussite, la licence a été téléchargée avec succès et est dans la Banque de licences locale prête à être utilisée.</span><span class="sxs-lookup"><span data-stu-id="7b1c3-124">If the retrieved **HRESULT** value is a success code, then the license was successfully downloaded and is in the local license store ready for use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b1c3-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7b1c3-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b1c3-126">**Acquisition de licences**</span><span class="sxs-lookup"><span data-stu-id="7b1c3-126">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="7b1c3-127">**Utilisation du modèle d’événement Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="7b1c3-127">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 




