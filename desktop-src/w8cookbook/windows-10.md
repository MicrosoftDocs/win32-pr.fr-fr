---
title: Windows 10
description: Ce livre de recettes fournit aux développeurs des informations sur les modifications apportées aux plateformes sur les systèmes d’exploitation Windows 10.
ms.assetid: bf8d7d10-bab6-4711-b65f-5393d906e47b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03fce627969573deb395fda356564a85a3573682
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382547"
---
# <a name="windows-10"></a><span data-ttu-id="e2fe8-103">Windows 10</span><span class="sxs-lookup"><span data-stu-id="e2fe8-103">Windows 10</span></span>

<span data-ttu-id="e2fe8-104">Ce livre de recettes fournit aux développeurs des informations sur les modifications apportées aux plateformes sur les systèmes d’exploitation Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e2fe8-104">This Cookbook provides info for developers about platform changes to the Windows 10 operating systems (OS).</span></span> <span data-ttu-id="e2fe8-105">Nous vous proposons également des instructions pour vérifier la compatibilité de vos applications existantes et planifiées avec la dernière version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e2fe8-105">We also provide guidelines for you to verify the compatibility of your existing and planned apps with the latest version of the OS.</span></span> <span data-ttu-id="e2fe8-106">Nous partons du principe que vous connaissez les versions précédentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="e2fe8-106">We assume that you are familiar with previous versions of Windows.</span></span>

<span data-ttu-id="e2fe8-107">Le contenu s’applique à : Windows 10</span><span class="sxs-lookup"><span data-stu-id="e2fe8-107">The content applies to: Windows 10</span></span>

<span data-ttu-id="e2fe8-108">Le livre de recettes est destiné aux développeurs tiers d’applications et d’appareils conçus pour être utilisés dans l’environnement Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e2fe8-108">The Cookbook is for third party developers of apps and devices that are designed to be used in the Microsoft Windows environment.</span></span>

## <a name="introduction"></a><span data-ttu-id="e2fe8-109">Introduction</span><span class="sxs-lookup"><span data-stu-id="e2fe8-109">Introduction</span></span>

<span data-ttu-id="e2fe8-110">Windows 10 introduit la dernière technologie de système d’exploitation et les plateformes de développement logiciel pour une utilisation par les développeurs d’applications et de pilotes dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="e2fe8-110">Windows 10 introduces the latest OS technology and software development platforms for use by app and driver developers and enterprises worldwide.</span></span> <span data-ttu-id="e2fe8-111">Pour améliorer la sécurité, la fiabilité, les performances et l’expérience utilisateur de Windows, Microsoft a introduit de nombreuses nouvelles fonctionnalités, amélioré les fonctionnalités existantes et supprimé d’autres.</span><span class="sxs-lookup"><span data-stu-id="e2fe8-111">To further enhance the security, reliability, performance, and user experience of Windows, Microsoft has introduced many new features, improved existing features, and removed others.</span></span>

<span data-ttu-id="e2fe8-112">Bien que l’objectif de Windows 10 est de maintenir la compatibilité avec les applications écrites pour les versions antérieures du système d’exploitation Windows, certains arrêts de compatibilité sont inévitables en raison des innovations, de la sécurité renforcée et de la fiabilité accrue.</span><span class="sxs-lookup"><span data-stu-id="e2fe8-112">While the goal of Windows 10 is to maintain compatibility with apps written for previously released versions of the Windows OS, some compatibility breaks are inevitable due to innovations, tightened security, and increased reliability.</span></span> <span data-ttu-id="e2fe8-113">Globalement, la compatibilité de la dernière version du système d’exploitation Windows avec les applications et les appareils existants est élevée.</span><span class="sxs-lookup"><span data-stu-id="e2fe8-113">Overall, the compatibility of the latest version of the Windows OS with existing apps and devices is high.</span></span>

<span data-ttu-id="e2fe8-114">Ce document vous montre comment vérifier que vos applications et appareils sont compatibles avec la dernière version du système d’exploitation et fournit une vue d’ensemble des problèmes d’incompatibilité d’applications connus.</span><span class="sxs-lookup"><span data-stu-id="e2fe8-114">This document shows you how to verify that your apps and devices are compatible with the latest version of the OS and provides an overview of known app incompatibility issues.</span></span>

<span data-ttu-id="e2fe8-115">Nous vous invitons à consulter ces rubriques pour savoir comment optimiser vos applications et tirer parti de ce que cette version plus récente de Windows a à offrir.</span><span class="sxs-lookup"><span data-stu-id="e2fe8-115">We invite you to check out these topics to learn how to optimize your apps and take advantage of what this newest release of Windows has to offer.</span></span>

## <a name="contents"></a><span data-ttu-id="e2fe8-116">Contenu</span><span class="sxs-lookup"><span data-stu-id="e2fe8-116">Contents</span></span>

-   [<span data-ttu-id="e2fe8-117">Modifications clés depuis Windows 7 pour garantir la compatibilité</span><span class="sxs-lookup"><span data-stu-id="e2fe8-117">Key changes since Windows 7 to ensure compatibility</span></span>](key-changes-since-windows-7-to-ensure-compatibility.md)
-   [<span data-ttu-id="e2fe8-118">Comment nous pouvons garantir la compatibilité de l’écosystème combiné</span><span class="sxs-lookup"><span data-stu-id="e2fe8-118">How we can ensure compatibility of the combined ecosystem</span></span>](how-we-can-ensure-compatibility-of-the-combined-ecosystem.md)
    -   [<span data-ttu-id="e2fe8-119">Vérification de la version de Windows</span><span class="sxs-lookup"><span data-stu-id="e2fe8-119">Windows version check</span></span>](windows-version-check.md)
    -   [<span data-ttu-id="e2fe8-120">API non documentées</span><span class="sxs-lookup"><span data-stu-id="e2fe8-120">Undocumented APIs</span></span>](undocumented-apis.md)
    -   [<span data-ttu-id="e2fe8-121">Développer des applications UWP et Desktop Bridge</span><span class="sxs-lookup"><span data-stu-id="e2fe8-121">Develop UWP and Desktop Bridge apps</span></span>](/windows/desktop/w8cookbook/develop-universal-windows-platform-apps)
    -   [<span data-ttu-id="e2fe8-122">Les fonctionnalités des applications de bureau modernes sont affectées si elles ne sont pas exécutées en mode fenêtre</span><span class="sxs-lookup"><span data-stu-id="e2fe8-122">Modern Desktop App functionality is impacted if not run in Windowed Mode</span></span>](modern-desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode.md)
    -   [<span data-ttu-id="e2fe8-123">Disponibilité des pilotes graphiques applicables sur Windows Update</span><span class="sxs-lookup"><span data-stu-id="e2fe8-123">Availability of applicable graphics drivers on Windows Update</span></span>](availability-of-applicable-graphics-drivers-on-windows-update.md)
    -   [<span data-ttu-id="e2fe8-124">Migration des pilotes Graphics vers Windows 10</span><span class="sxs-lookup"><span data-stu-id="e2fe8-124">Graphics driver migration to Windows 10</span></span>](graphics-driver-migration-to-windows-10.md)
    -   [<span data-ttu-id="e2fe8-125">Pilotes Bluetooth</span><span class="sxs-lookup"><span data-stu-id="e2fe8-125">Bluetooth drivers</span></span>](bluetooth-drivers.md)

## <a name="download-the-cookbook"></a><span data-ttu-id="e2fe8-126">Téléchargez le livre de recettes</span><span class="sxs-lookup"><span data-stu-id="e2fe8-126">Download the cookbook</span></span>

<span data-ttu-id="e2fe8-127">Pour obtenir une référence rapide à toutes ces informations, ainsi que des informations sur Windows en tant que service, sur la prise en charge des applications dans Windows et sur les stratégies optimisées pour le test de votre application, [Téléchargez le Guide de compatibilité de Windows 10](https://download.microsoft.com/download/3/D/3/3D36E358-A7E4-4DA3-9FC4-6E85C850A6C6/Windows%2010%20Compatibility%20Cookbook.docx).</span><span class="sxs-lookup"><span data-stu-id="e2fe8-127">For a quick reference to all this information, as well as information on Windows as a service, supporting apps in Windows, and optimized strategies for testing your app, [download the Windows 10 Compatibility Cookbook](https://download.microsoft.com/download/3/D/3/3D36E358-A7E4-4DA3-9FC4-6E85C850A6C6/Windows%2010%20Compatibility%20Cookbook.docx).</span></span>

## <a name="see-also"></a><span data-ttu-id="e2fe8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2fe8-128">See Also</span></span>

-   <span data-ttu-id="e2fe8-129">[Windows en tant que service](/windows/deployment/update/), pour plus d’informations sur les types de version et la prise en charge des applications Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e2fe8-129">[Windows as a service](/windows/deployment/update/), for information about Windows 10 release types and app support.</span></span>
-   <span data-ttu-id="e2fe8-130">[Windows Insider](https://insider.windows.com/), pour accéder aux builds en version préliminaire, tester et fournir des commentaires.</span><span class="sxs-lookup"><span data-stu-id="e2fe8-130">[Windows Insider](https://insider.windows.com/), to access preview builds, test, and provide feedback.</span></span>
-   <span data-ttu-id="e2fe8-131">[Prêt pour Windows 10](https://www.readyfor10.com/), envoyer les informations de votre entreprise à une ressource pour les responsables informatiques.</span><span class="sxs-lookup"><span data-stu-id="e2fe8-131">[Ready for Windows 10](https://www.readyfor10.com/), to submit your company's information to a resource for IT managers.</span></span>

 

 