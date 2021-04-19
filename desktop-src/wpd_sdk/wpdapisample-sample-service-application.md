---
description: Application WpdServicesApiSample
ms.assetid: 857753f7-bca1-4f4a-a8f9-0b2232e2f0dc
title: Application WpdServicesApiSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54cbf6c6e4647744ae45f43b5d4139cbf7f9dc55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525068"
---
# <a name="wpdservicesapisample-application"></a><span data-ttu-id="b7cb8-103">Application WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="b7cb8-103">WpdServicesApiSample Application</span></span>

<span data-ttu-id="b7cb8-104">Un service d’appareil est une extension d’un objet fonctionnel : outre le regroupement logique des fonctionnalités de l’appareil, un service d’appareil fournit aux applications la possibilité de découvrir ces fonctionnalités par programmation.</span><span class="sxs-lookup"><span data-stu-id="b7cb8-104">A device service is an extension of a functional object: In addition to logically grouping device capabilities, a device service provides applications with the ability to programmatically discover those capabilities.</span></span>

<span data-ttu-id="b7cb8-105">L’exemple d’application WpdServicesApiSample est une application de bureau en ligne de commande que vous pouvez utiliser pour explorer les services de contacts sur les appareils connectés à votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b7cb8-105">The WpdServicesApiSample sample application is a command-line desktop application that you can use to explore Contacts services on devices attached to your computer.</span></span> <span data-ttu-id="b7cb8-106">Vous pouvez explorer ces services en répertoriant les formats, les événements, les méthodes et les services abstraits pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b7cb8-106">You can explore these services by listing supported: formats, events, methods, and abstract services.</span></span> <span data-ttu-id="b7cb8-107">Vous pouvez également utiliser cette application pour récupérer les propriétés sur un service de contact donné et appeler les méthodes prises en charge par ce service.</span><span class="sxs-lookup"><span data-stu-id="b7cb8-107">You can also use this application retrieve the properties on a given Contact service and to invoke methods supported by that service.</span></span>

<span data-ttu-id="b7cb8-108">Si vous n’avez pas encore un appareil qui prend en charge les services de contacts, vous pouvez toujours exécuter le WpdServicesApiSample si vous installez pour la première fois le WpdServiceSampleDriver inclus dans le kit de pilotes Windows.</span><span class="sxs-lookup"><span data-stu-id="b7cb8-108">If you don't yet have a device that supports Contacts services, you can still run the WpdServicesApiSample if you first install the WpdServiceSampleDriver that is included in the Windows Driver Kit.</span></span>

<span data-ttu-id="b7cb8-109">L’exemple d’application WpdServicesApiSample comprend les fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="b7cb8-109">The WpdServicesApiSample sample application includes the following files:</span></span>



| <span data-ttu-id="b7cb8-110">**File**</span><span class="sxs-lookup"><span data-stu-id="b7cb8-110">**File**</span></span>                | <span data-ttu-id="b7cb8-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="b7cb8-111">**Description**</span></span>                                                                                                                                                                                           |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7cb8-112">ContentEnumeration. cpp</span><span class="sxs-lookup"><span data-stu-id="b7cb8-112">ContentEnumeration.cpp</span></span>  | <span data-ttu-id="b7cb8-113">Contient des méthodes qui énumèrent le contenu d’un service de contacts donné.</span><span class="sxs-lookup"><span data-stu-id="b7cb8-113">Contains methods that enumerate the content on a given Contacts service.</span></span>                                                                                                                                  |
| <span data-ttu-id="b7cb8-114">ContentProperties. cpp</span><span class="sxs-lookup"><span data-stu-id="b7cb8-114">ContentProperties.cpp</span></span>   | <span data-ttu-id="b7cb8-115">Contient des méthodes qui lisent et écrivent des propriétés sur un service de contacts donné.</span><span class="sxs-lookup"><span data-stu-id="b7cb8-115">Contains methods that read and write properties on a given Contacts service.</span></span>                                                                                                                              |
| <span data-ttu-id="b7cb8-116">ServiceCapabilities. cpp</span><span class="sxs-lookup"><span data-stu-id="b7cb8-116">ServiceCapabilities.cpp</span></span> | <span data-ttu-id="b7cb8-117">Contient les méthodes qui récupèrent les formats, événements et services abstraits pris en charge par un service de contacts donné.</span><span class="sxs-lookup"><span data-stu-id="b7cb8-117">Contains the methods that retrieve the supported formats, events, and abstract services that are supported by a given Contacts service.</span></span>                                                                   |
| <span data-ttu-id="b7cb8-118">ServiceEnumeration. cpp</span><span class="sxs-lookup"><span data-stu-id="b7cb8-118">ServiceEnumeration.cpp</span></span>  | <span data-ttu-id="b7cb8-119">Contient les fonctions d’assistance qui récupèrent des informations sur l’appareil, telles que le nom convivial du périphérique ou les services de contacts pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b7cb8-119">Contains the helper functions that retrieve device information such as the device-friendly name or the supported Contacts services.</span></span>                                                                       |
| <span data-ttu-id="b7cb8-120">ServiceMethods. cpp</span><span class="sxs-lookup"><span data-stu-id="b7cb8-120">ServiceMethods.cpp</span></span>      | <span data-ttu-id="b7cb8-121">Contient les méthodes qui récupèrent et appellent les méthodes prises en charge par un service de contacts donné.</span><span class="sxs-lookup"><span data-stu-id="b7cb8-121">Contains the methods that retrieve and invoke methods supported by a given Contacts service.</span></span>                                                                                                              |
| <span data-ttu-id="b7cb8-122">stdafx.cpp</span><span class="sxs-lookup"><span data-stu-id="b7cb8-122">Stdafx.cpp</span></span>              | <span data-ttu-id="b7cb8-123">Comprend les fichiers standard.</span><span class="sxs-lookup"><span data-stu-id="b7cb8-123">Includes the standard files.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="b7cb8-124">WpdServiceApiSample. cpp</span><span class="sxs-lookup"><span data-stu-id="b7cb8-124">WpdServiceApiSample.cpp</span></span> | <span data-ttu-id="b7cb8-125">Héberge la fonction de démarrage **\_ tmain** , qui appelle la fonction de **menu contextuel** locale, qui affiche une liste des périphériques et des tâches disponibles et appelle la fonction appropriée pour la sélection de menu de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b7cb8-125">Hosts the **\_tmain** startup function, which calls the local **DoMenu** function, which displays a list of available devices and tasks and calls the function appropriate for the user's menu selection.</span></span> |



 


## <a name="related-topics"></a><span data-ttu-id="b7cb8-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7cb8-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7cb8-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="b7cb8-127">Samples</span></span>](sample.md)
</dt> </dl>

 

 



