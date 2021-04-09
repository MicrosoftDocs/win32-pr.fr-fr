---
title: Utilisation d’IMAPi
description: Les rubriques suivantes illustrent l’utilisation de l’API de mastérisation d’image.
ms.assetid: c42043db-612f-488f-a6ae-a8caea8ac42b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccd44d01e925d07d251e93a29c5268cc7e9c5076
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840833"
---
# <a name="using-imapi"></a><span data-ttu-id="4317a-103">Utilisation d’IMAPi</span><span class="sxs-lookup"><span data-stu-id="4317a-103">Using IMAPI</span></span>

<span data-ttu-id="4317a-104">Les rubriques suivantes illustrent l’utilisation de l’API de mastérisation d’image.</span><span class="sxs-lookup"><span data-stu-id="4317a-104">The following topics demonstrate the use of the image mastering API.</span></span>

## <a name="usage-scenarios"></a><span data-ttu-id="4317a-105">Scénarios d’utilisation</span><span class="sxs-lookup"><span data-stu-id="4317a-105">Usage Scenarios</span></span>

<span data-ttu-id="4317a-106">La documentation suivante fournit des conseils détaillés pour les scénarios IMAPi courants.</span><span class="sxs-lookup"><span data-stu-id="4317a-106">The following documentation provides detailed guidance for common IMAPI scenarios.</span></span>



| <span data-ttu-id="4317a-107">Scénario</span><span class="sxs-lookup"><span data-stu-id="4317a-107">Scenario</span></span>                                                                                                         | <span data-ttu-id="4317a-108">Description</span><span class="sxs-lookup"><span data-stu-id="4317a-108">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4317a-109">Vérification de la prise en charge du lecteur</span><span class="sxs-lookup"><span data-stu-id="4317a-109">Checking Drive Support</span></span>](checking-drive-support.md)                                                             | <span data-ttu-id="4317a-110">Illustre la détection de la prise en charge d’un lecteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="4317a-110">Demonstrates the detection of support for a media drive.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="4317a-111">Vérification de la prise en charge des supports</span><span class="sxs-lookup"><span data-stu-id="4317a-111">Checking Media Support</span></span>](checking-media-support.md)                                                             | <span data-ttu-id="4317a-112">Illustre la détection de la prise en charge des médias.</span><span class="sxs-lookup"><span data-stu-id="4317a-112">Demonstrates the detection of support for media.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="4317a-113">Gravure d’une image de disque</span><span class="sxs-lookup"><span data-stu-id="4317a-113">Burning a Disc Image</span></span>](burning-a-disc.md)                                                                       | <span data-ttu-id="4317a-114">Illustre la maîtrise (gravure d’un disque) à l’aide d’IMAPi.</span><span class="sxs-lookup"><span data-stu-id="4317a-114">Demonstrates mastering (burning a disc) using IMAPI.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="4317a-115">Ajout d’une image de démarrage</span><span class="sxs-lookup"><span data-stu-id="4317a-115">Adding a Boot Image</span></span>](adding-a-boot-image.md)                                                                   | <span data-ttu-id="4317a-116">S’appuie sur l’exemple [gravure d’une image de disque](burning-a-disc.md) en ajoutant du code pour inclure une image de démarrage dans la section de démarrage du disque.</span><span class="sxs-lookup"><span data-stu-id="4317a-116">Builds on the [Burning a Disc Image](burning-a-disc.md) example by adding code to include a bootable image in the boot section of the disc.</span></span><br/>               |
| [<span data-ttu-id="4317a-117">Création d’un disque multisession</span><span class="sxs-lookup"><span data-stu-id="4317a-117">Creating a Multisession Disc</span></span>](creating-a-multisession-disc.md)                                                 | <span data-ttu-id="4317a-118">Illustre la création d’un disque multisession à l’aide d’IMAPi.</span><span class="sxs-lookup"><span data-stu-id="4317a-118">Demonstrates the creation of a multisession disc using IMAPI.</span></span><br/>                                                                                              |
| [<span data-ttu-id="4317a-119">Surveillance de la progression avec des événements</span><span class="sxs-lookup"><span data-stu-id="4317a-119">Monitoring Progress With Events</span></span>](monitoring-progress-with-events.md)                                           | <span data-ttu-id="4317a-120">Illustre l’utilisation d’interfaces spécifiques pour permettre l’implémentation d’un gestionnaire d’événements afin que les informations de progression puissent être reçues.</span><span class="sxs-lookup"><span data-stu-id="4317a-120">Demonstrates the use of specific interfaces in order to allow the implementation of an event handler so that progress information may be received.</span></span> <br/>        |
| [<span data-ttu-id="4317a-121">Empêcher la déconnexion ou la suspension pendant une gravure</span><span class="sxs-lookup"><span data-stu-id="4317a-121">Preventing Logoff or Suspend During a Burn</span></span>](preventing-logoff-or-suspend-during-a-burn.md)                     | <span data-ttu-id="4317a-122">Contient des informations détaillant les considérations relatives au développement d’applications en ce qui concerne les scénarios impliquant l’utilisateur « Logoff » et « suspend » dans Windows.</span><span class="sxs-lookup"><span data-stu-id="4317a-122">Contains information detailing application development considerations to be made in regards to scenarios involving user 'Logoff' and 'Suspend' in Windows.</span></span><br/> |
| [<span data-ttu-id="4317a-123">Fournir des autorisations utilisateur pour les appareils de gravure de médias</span><span class="sxs-lookup"><span data-stu-id="4317a-123">Providing User Permissions for Media Burning Devices</span></span>](providing-user-permissions-for-media-burning-devices.md) | <span data-ttu-id="4317a-124">Détaille le processus nécessaire pour s’assurer qu’un utilisateur dispose des autorisations adéquates pour utiliser des appareils de gravure de contenu multimédia sur Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4317a-124">Details the process required to ensure a user has adequate permissions to utilize media burning devices on Windows XP and Windows Server 2003.</span></span><br/>             |



 

## <a name="application-compatibility"></a><span data-ttu-id="4317a-125">Compatibilité des applications</span><span class="sxs-lookup"><span data-stu-id="4317a-125">Application Compatibility</span></span>

<span data-ttu-id="4317a-126">La documentation suivante contient des informations importantes à prendre en compte lors du développement d’une application qui utilise IMAPi.</span><span class="sxs-lookup"><span data-stu-id="4317a-126">The following documentation contains important information to take consideration while developing an application that utilizes IMAPI.</span></span>



| <span data-ttu-id="4317a-127">Instructions</span><span class="sxs-lookup"><span data-stu-id="4317a-127">Guidance</span></span>                                                   | <span data-ttu-id="4317a-128">Description</span><span class="sxs-lookup"><span data-stu-id="4317a-128">Description</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4317a-129">Présentation de la multisession IMAPi</span><span class="sxs-lookup"><span data-stu-id="4317a-129">IMAPI Multisession Layout</span></span>](imapi-multisession-layout.md) | <span data-ttu-id="4317a-130">Détaille la disposition du disque que IMAPi utilise pour implémenter la multisession.</span><span class="sxs-lookup"><span data-stu-id="4317a-130">Details the disc layout that IMAPI utilizes to implement multisession.</span></span> <span data-ttu-id="4317a-131">Ces informations sont utilisées pour garantir l’interopérabilité entre IMAPi et d’autres logiciels de gravure, ainsi que pour autoriser la création d’images de disque multisession compatibles IMAPi.</span><span class="sxs-lookup"><span data-stu-id="4317a-131">This information is used to ensure interoperability between IMAPI and other burning software, as well as allow the creation of IMAPI-compatible multisession disc images.</span></span><br/> |



 

 

 





