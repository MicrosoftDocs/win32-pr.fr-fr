---
title: Interfaces du client Microsoft Windows Media DRM
description: Interfaces du client Microsoft Windows Media DRM
ms.assetid: 27bbc33f-8102-4db2-bbc6-1a1da92bac80
keywords:
- Windows Media Format SDK, interfaces
- gestion des droits numériques (DRM), interfaces
- DRM (gestion des droits numériques), interfaces
- API étendues du client DRM, interfaces
- API étendues clientes, interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4e259ef5b8ef410db072a7f942d139f682bc90
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383580"
---
# <a name="microsoft-windows-media-drm-client-interfaces"></a><span data-ttu-id="9e74b-108">Interfaces du client Microsoft Windows Media DRM</span><span class="sxs-lookup"><span data-stu-id="9e74b-108">Microsoft Windows Media DRM Client Interfaces</span></span>

<span data-ttu-id="9e74b-109">Le tableau suivant décrit les interfaces prises en charge par les API clientes Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="9e74b-109">The following table describes the interfaces supported by the Windows Media DRM Client APIs.</span></span>



| <span data-ttu-id="9e74b-110">Interface</span><span class="sxs-lookup"><span data-stu-id="9e74b-110">Interface</span></span>                                                                    | <span data-ttu-id="9e74b-111">Description</span><span class="sxs-lookup"><span data-stu-id="9e74b-111">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e74b-112">**IDRMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="9e74b-112">**IDRMStatusCallback**</span></span>](idrmstatuscallback.md)                             | <span data-ttu-id="9e74b-113">Fournit la définition d’un rappel d’État que vous pouvez implémenter pour gérer les opérations DRM asynchrones.</span><span class="sxs-lookup"><span data-stu-id="9e74b-113">Provides the definition for a status callback that you can implement to handle asynchronous DRM operations.</span></span>     |
| [<span data-ttu-id="9e74b-114">**IWMDRMDecrypt**</span><span class="sxs-lookup"><span data-stu-id="9e74b-114">**IWMDRMDecrypt**</span></span>](iwmdrmdecrypt.md)                                       | <span data-ttu-id="9e74b-115">Fournit une méthode pour déchiffrer le contenu.</span><span class="sxs-lookup"><span data-stu-id="9e74b-115">Provides a method for decrypting content.</span></span>                                                                       |
| [<span data-ttu-id="9e74b-116">**IWMDRMEncrypt**</span><span class="sxs-lookup"><span data-stu-id="9e74b-116">**IWMDRMEncrypt**</span></span>](iwmdrmencrypt.md)                                       | <span data-ttu-id="9e74b-117">Fournit une méthode pour chiffrer les données sur place.</span><span class="sxs-lookup"><span data-stu-id="9e74b-117">Provides a method for encrypting data in place.</span></span>                                                                 |
| [<span data-ttu-id="9e74b-118">**IWMDRMEncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="9e74b-118">**IWMDRMEncryptScatter**</span></span>](iwmdrmencryptscatter.md)                         | <span data-ttu-id="9e74b-119">Chiffre les données à partir de blocs non contigus.</span><span class="sxs-lookup"><span data-stu-id="9e74b-119">Encrypts data from non-contiguous blocks.</span></span>                                                                       |
| [<span data-ttu-id="9e74b-120">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="9e74b-120">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)                         | <span data-ttu-id="9e74b-121">Extension de l’interface **IMFMediaEventGenerator** qui fournit une méthode pour annuler des opérations asynchrones.</span><span class="sxs-lookup"><span data-stu-id="9e74b-121">Extension of the **IMFMediaEventGenerator** interface that provides a method to cancel asynchronous operations.</span></span> |
| [<span data-ttu-id="9e74b-122">**IWMDRMIndividualizationStatus**</span><span class="sxs-lookup"><span data-stu-id="9e74b-122">**IWMDRMIndividualizationStatus**</span></span>](iwmdrmindividualizationstatus.md)       | <span data-ttu-id="9e74b-123">Permet la récupération d’informations d’État avancées sur la progression de l’individualisation.</span><span class="sxs-lookup"><span data-stu-id="9e74b-123">Enables retrieval of advanced status information about the progress of individualization.</span></span>                       |
| [<span data-ttu-id="9e74b-124">**IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="9e74b-124">**IWMDRMLicense**</span></span>](iwmdrmlicense.md)                                       | <span data-ttu-id="9e74b-125">Représente une ou plusieurs licences dans le magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="9e74b-125">Represents one or more licenses in the local license store.</span></span>                                                     |
| [<span data-ttu-id="9e74b-126">**IWMDRMLicenseBackupRestoreStatus**</span><span class="sxs-lookup"><span data-stu-id="9e74b-126">**IWMDRMLicenseBackupRestoreStatus**</span></span>](iwmdrmlicensebackuprestorestatus.md) | <span data-ttu-id="9e74b-127">Permet la récupération d’informations d’État détaillées sur une opération de sauvegarde ou de restauration de licence.</span><span class="sxs-lookup"><span data-stu-id="9e74b-127">Enables retrieval of detailed status information about a license backup or restore operation.</span></span>                   |
| [<span data-ttu-id="9e74b-128">**IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="9e74b-128">**IWMDRMLicenseManagement**</span></span>](iwmdrmlicensemanagement.md)                   | <span data-ttu-id="9e74b-129">Active les opérations de gestion pour le magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="9e74b-129">Enables management operations for the local license store.</span></span>                                                      |
| [<span data-ttu-id="9e74b-130">**IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="9e74b-130">**IWMDRMLicenseManagement**</span></span>](iwmdrmlicensemanagement.md)                   | <span data-ttu-id="9e74b-131">Fournit des options de gestion supplémentaires pour le magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="9e74b-131">Provides additional management options for the local license store.</span></span>                                             |
| [<span data-ttu-id="9e74b-132">**IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="9e74b-132">**IWMDRMLicenseQuery**</span></span>](iwmdrmlicensequery.md)                             | <span data-ttu-id="9e74b-133">Permet aux applications d’interroger les droits et l’état de licence d’un fichier protégé.</span><span class="sxs-lookup"><span data-stu-id="9e74b-133">Enables applications to query the rights and license state for a protected file.</span></span>                                |
| [<span data-ttu-id="9e74b-134">**IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="9e74b-134">**IWMDRMNetReceiver**</span></span>](iwmdrmnetreceiver.md)                               | <span data-ttu-id="9e74b-135">Fournit les méthodes nécessaires pour créer une application de récepteur DRM Microsoft Windows Media pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="9e74b-135">Provides methods needed create a Microsoft Windows Media DRM for Network Devices receiver application.</span></span>          |
| [<span data-ttu-id="9e74b-136">**IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="9e74b-136">**IWMDRMNetTransmitter**</span></span>](iwmdrmnettransmitter.md)                         | <span data-ttu-id="9e74b-137">Fournit les méthodes nécessaires pour créer une application Microsoft Windows Media DRM pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="9e74b-137">Provides methods needed create a Microsoft Windows Media DRM for Network Devices transmitter application.</span></span>       |
| [<span data-ttu-id="9e74b-138">**IWMDRMNonSilentLicenseAquisition**</span><span class="sxs-lookup"><span data-stu-id="9e74b-138">**IWMDRMNonSilentLicenseAquisition**</span></span>](iwmdrmnonsilentlicenseaquisition.md) | <span data-ttu-id="9e74b-139">Fournit des méthodes qui permettent l’acquisition de licences avec intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9e74b-139">Provides methods that enable license acquisition with user intervention.</span></span>                                        |
| [<span data-ttu-id="9e74b-140">**IWMDRMProvider**</span><span class="sxs-lookup"><span data-stu-id="9e74b-140">**IWMDRMProvider**</span></span>](iwmdrmprovider.md)                                     | <span data-ttu-id="9e74b-141">Crée les autres objets des API étendues du client Microsoft Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="9e74b-141">Creates the other objects of the Microsoft Windows Media DRM Client Extended APIs.</span></span>                              |
| [<span data-ttu-id="9e74b-142">**IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="9e74b-142">**IWMDRMSecurity**</span></span>](iwmdrmsecurity.md)                                     | <span data-ttu-id="9e74b-143">Gère différents processus liés à la sécurité pour l’ordinateur client et le sous-système DRM.</span><span class="sxs-lookup"><span data-stu-id="9e74b-143">Manages various security-related processes for the client computer and DRM subsystem.</span></span>                           |
| [<span data-ttu-id="9e74b-144">**IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="9e74b-144">**IWMDRMSecurity**</span></span>](iwmdrmsecurity.md)                                     | <span data-ttu-id="9e74b-145">Gère la révocation et le renouvellement des composants.</span><span class="sxs-lookup"><span data-stu-id="9e74b-145">Manages component revocation and renewal.</span></span>                                                                       |
| [<span data-ttu-id="9e74b-146">**IWMSecureBuffer**</span><span class="sxs-lookup"><span data-stu-id="9e74b-146">**IWMSecureBuffer**</span></span>](iwmsecurebuffer.md)                                   | <span data-ttu-id="9e74b-147">Active le chiffrement et le déchiffrement des mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="9e74b-147">Enables encryption and decryption of buffers.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="9e74b-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9e74b-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e74b-149">**Guide de référence de programmation**</span><span class="sxs-lookup"><span data-stu-id="9e74b-149">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




