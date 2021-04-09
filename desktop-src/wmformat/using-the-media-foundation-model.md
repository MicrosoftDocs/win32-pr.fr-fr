---
title: Utilisation du modèle d’événement Media Foundation
description: Utilisation du modèle d’événement Media Foundation
ms.assetid: c07425dc-25d0-430b-a1f6-6373303a0cc7
keywords:
- Kit de développement logiciel (SDK) de format Windows Media, modèle d’événement DRM Media Foundation
- Kit de développement logiciel (SDK) Windows Media format, Media Foundation modèle d’événement
- Kit de développement logiciel (SDK) Windows Media format, modèle d’événement DRM
- gestion des droits numériques (DRM), Media Foundation modèle d’événement
- DRM (gestion des droits numériques), Media Foundation modèle d’événement
- gestion des droits numériques (DRM), modèle d’événement
- DRM (gestion des droits numériques), modèle d’événement
- gestion des droits numériques (DRM), interface IWMDRMEventGenerator
- DRM (gestion des droits numériques), interface IWMDRMEventGenerator
- Media Foundation
- IWMDRMEventGenerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58d48157072cf8814ff8ac74d97a965f9e772e3
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104030874"
---
# <a name="using-the-media-foundation-event-model"></a><span data-ttu-id="acb24-114">Utilisation du modèle d’événement Media Foundation</span><span class="sxs-lookup"><span data-stu-id="acb24-114">Using the Media Foundation Event Model</span></span>

<span data-ttu-id="acb24-115">Les méthodes asynchrones prises en charge par les API étendues du client Windows Media DRM utilisent le même modèle d’événement que celui utilisé par le kit de développement logiciel (SDK) Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="acb24-115">The asynchronous methods supported by the Windows Media DRM Client Extended APIs use the same event model that is used by the Media Foundation SDK.</span></span> <span data-ttu-id="acb24-116">Chaque objet qui prend en charge des méthodes asynchrones implémente l’interface [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md) , qui peut être utilisée pour récupérer un événement lorsqu’une opération asynchrone est terminée.</span><span class="sxs-lookup"><span data-stu-id="acb24-116">Each object that supports asynchronous methods implements the [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md) interface, which can be used to retrieve an event when an asynchronous operation is complete.</span></span>

<span data-ttu-id="acb24-117">L’interface **IWMDRMEventGenerator** hérite de l’interface **IMFMediaEventGenerator** , qui est décrite dans la documentation du kit de développement logiciel (SDK) Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="acb24-117">The **IWMDRMEventGenerator** interface inherits from the **IMFMediaEventGenerator** interface, which is documented in the Media Foundation SDK documentation.</span></span>

<span data-ttu-id="acb24-118">L’exemple de code de l’exemple de l' [individualisation DRM](drm-individualization-example.md) utilise la méthode **IMFMediaEventGenerator :: GetEvent** pour récupérer les événements de la file d’attente un par un.</span><span class="sxs-lookup"><span data-stu-id="acb24-118">The example code in the [DRM Individualization Example](drm-individualization-example.md) uses the **IMFMediaEventGenerator::GetEvent** method to retrieve events from the queue one at a time.</span></span> <span data-ttu-id="acb24-119">L’utilisation de **GetEvent** est plus simple que l’utilisation de **IMFMediaEventGenerator :: BeginGetEvent** et **IMFMediaEventGenerator :: EndGetEvent** avec un rappel, ce qui rend les exemples de code plus faciles à comprendre.</span><span class="sxs-lookup"><span data-stu-id="acb24-119">Using **GetEvent** is more straightforward than using **IMFMediaEventGenerator::BeginGetEvent** and **IMFMediaEventGenerator::EndGetEvent** with a callback, which makes the code examples easier to understand.</span></span> <span data-ttu-id="acb24-120">Que vous utilisiez **GetEvent** dans votre code ou implémentiez **IMFAsyncCallback** et que vous utilisiez **BeginGetEvent** et **EndGetEvent**, la logique de gestion de l’événement après sa réception est la même.</span><span class="sxs-lookup"><span data-stu-id="acb24-120">Whether you use **GetEvent** in your code or implement **IMFAsyncCallback** and use **BeginGetEvent** and **EndGetEvent**, the logic to handle the event after it has been received is the same.</span></span>

<span data-ttu-id="acb24-121">Plusieurs méthodes asynchrones génèrent des événements qui contiennent des références à des objets qui peuvent être utilisés pour obtenir des informations d’État plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="acb24-121">Several of the asynchronous methods generate events that contain references to objects that can be used to obtain more detailed status information.</span></span> <span data-ttu-id="acb24-122">Dans ces cas, l’événement généré a un pointeur **IUnknown** comme valeur, qui peut être interrogé pour récupérer l’interface d’État.</span><span class="sxs-lookup"><span data-stu-id="acb24-122">In these cases, the generated event has an **IUnknown** pointer as its value, which can be queried to retrieve the status interface.</span></span> <span data-ttu-id="acb24-123">La liste suivante résume les relations entre les appels asynchrones, les événements générés et d’autres interfaces.</span><span class="sxs-lookup"><span data-stu-id="acb24-123">The following list summarizes the relationships between asynchronous calls, generated events, and other interfaces.</span></span>

-   <span data-ttu-id="acb24-124">La méthode [**IWMDRMLicenseManagement :: BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) génère des événements **MEWMDRMLicenseBackupProgress** avec les interfaces [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) associées.</span><span class="sxs-lookup"><span data-stu-id="acb24-124">The [**IWMDRMLicenseManagement::BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) method generates **MEWMDRMLicenseBackupProgress** events with associated [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interfaces.</span></span>
-   <span data-ttu-id="acb24-125">La méthode [**IWMDRMLicenseManagement :: RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md) génère des événements **MEWMDRMLicenseRestoreProgress** avec les interfaces [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) associées.</span><span class="sxs-lookup"><span data-stu-id="acb24-125">The [**IWMDRMLicenseManagement::RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md) method generates **MEWMDRMLicenseRestoreProgress** events with associated [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interfaces.</span></span>
-   <span data-ttu-id="acb24-126">La méthode [**IWMDRMSecurity ::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) , lorsqu’elle est utilisée pour effectuer une individualisation, génère des événements **MEWMDRMIndividualizationProgress** avec les interfaces [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) associées.</span><span class="sxs-lookup"><span data-stu-id="acb24-126">The [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) method, when used to perform individualization, generates **MEWMDRMIndividualizationProgress** events with associated [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) interfaces.</span></span>
-   <span data-ttu-id="acb24-127">La méthode [**IWMDRMLicenseManagement :: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) , lorsqu’elle est utilisée pour préparer des données pour une acquisition de licence non silencieuse, génère un événement **MEWMDRMLicenseAcquisitionCompleted** avec une interface [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) associée.</span><span class="sxs-lookup"><span data-stu-id="acb24-127">The [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method, when used to prepare data for non-silent license acquisition, generates an **MEWMDRMLicenseAcquisitionCompleted** event with an associated [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="acb24-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="acb24-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acb24-129">**Exemple d’individualisation DRM**</span><span class="sxs-lookup"><span data-stu-id="acb24-129">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="acb24-130">**Prise en main**</span><span class="sxs-lookup"><span data-stu-id="acb24-130">**Getting Started**</span></span>](drm-getting-started.md)
</dt> <dt>

[<span data-ttu-id="acb24-131">Documentation du kit de développement logiciel Media Foundation</span><span class="sxs-lookup"><span data-stu-id="acb24-131">Media Foundation SDK Documentation</span></span>](https://www.microsoft.com/?ref=go)
</dt> </dl>

 

 




