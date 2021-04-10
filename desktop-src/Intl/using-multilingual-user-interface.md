---
description: Utilisation de l’interface utilisateur multilingue
ms.assetid: caf167ad-f9a8-4093-9581-57bc507d1f6a
title: Utilisation de l’interface utilisateur multilingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287acc88d144c7775d2125cbb4a055784370d87f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210936"
---
# <a name="using-multilingual-user-interface"></a><span data-ttu-id="e9dcf-103">Utilisation de l’interface utilisateur multilingue</span><span class="sxs-lookup"><span data-stu-id="e9dcf-103">Using Multilingual User Interface</span></span>

<span data-ttu-id="e9dcf-104">Cette section décrit comment utiliser les fonctionnalités de l’interface utilisateur multilingue (MUI) pour concevoir et implémenter vos applications.</span><span class="sxs-lookup"><span data-stu-id="e9dcf-104">This section describes how to use Multilingual User Interface (MUI) functionality to design and implement your applications.</span></span> <span data-ttu-id="e9dcf-105">Vous trouverez ci-dessous des aspects de la technologie MUI qui vont être joués à la plupart des étapes du cycle de vie de l’application.</span><span class="sxs-lookup"><span data-stu-id="e9dcf-105">The following are aspects of MUI technology that will come into play at most stages of the application lifecycle.</span></span>

-   <span data-ttu-id="e9dcf-106">Développement d’applications, notamment la préparation des ressources, le paramétrage des préférences linguistiques de l’application, la recherche et le chargement des ressources</span><span class="sxs-lookup"><span data-stu-id="e9dcf-106">Application development, including resource preparation, setting of application language preferences, finding and loading of resources</span></span>
-   <span data-ttu-id="e9dcf-107">Génération et localisation de l’application</span><span class="sxs-lookup"><span data-stu-id="e9dcf-107">Building and localizing the application</span></span>
-   <span data-ttu-id="e9dcf-108">Déploiement de l’application</span><span class="sxs-lookup"><span data-stu-id="e9dcf-108">Deploying the application</span></span>

<span data-ttu-id="e9dcf-109">Voici quelques questions à prendre en compte lors de la conception et de l’implémentation d’une application MUI.</span><span class="sxs-lookup"><span data-stu-id="e9dcf-109">Here are some questions to consider when designing and implementing a MUI application.</span></span>

-   <span data-ttu-id="e9dcf-110">Quelles sont les versions de Windows prises en charge par l’application ?</span><span class="sxs-lookup"><span data-stu-id="e9dcf-110">What are the versions of Windows that the application will support?</span></span>
-   <span data-ttu-id="e9dcf-111">Dans quelles langues l’application sera-t-elle localisée ?</span><span class="sxs-lookup"><span data-stu-id="e9dcf-111">In what languages will the application be localized?</span></span>
-   <span data-ttu-id="e9dcf-112">Les paramètres de langue de l’application doivent-ils toujours suivre les paramètres de langue du système d’exploitation ou l’utilisateur de l’application est-il en mesure de définir des langues spécifiques ?</span><span class="sxs-lookup"><span data-stu-id="e9dcf-112">Should the application language settings always follow language settings for the operating system, or should the application user be able to set specific languages?</span></span>
-   <span data-ttu-id="e9dcf-113">Quels types de ressources d’interface utilisateur l’application utilise-t-elle et où sont-elles stockées ?</span><span class="sxs-lookup"><span data-stu-id="e9dcf-113">What type of user interface resources does the application use and where are they stored?</span></span>

<span data-ttu-id="e9dcf-114">Cette section comprend les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="e9dcf-114">This section includes the following topics.</span></span> <span data-ttu-id="e9dcf-115">Les descriptions supposent une application MUI ciblée sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e9dcf-115">The descriptions assume a MUI application targeted at Windows Vista and later.</span></span> <span data-ttu-id="e9dcf-116">Les ressources de cette application sont des ressources Win32, avec des ressources spécifiques à la langue et du code exécutable résidant dans des fichiers PE Win32 distincts.</span><span class="sxs-lookup"><span data-stu-id="e9dcf-116">The resources for this application are Win32 resources, with language-specific resources and executable code residing in separate Win32 PE files.</span></span> <span data-ttu-id="e9dcf-117">Des considérations spéciales pour la prise en charge des systèmes d’exploitation antérieurs à Windows Vista ou pour différents types de ressources sont ajoutées, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="e9dcf-117">Special considerations for support of pre-Windows Vista operating systems or for different types of resources are added as appropriate.</span></span>

-   [<span data-ttu-id="e9dcf-118">Préparation des ressources</span><span class="sxs-lookup"><span data-stu-id="e9dcf-118">Preparing Resources</span></span>](preparing-resources.md)
-   [<span data-ttu-id="e9dcf-119">Définition des préférences linguistiques de l’application</span><span class="sxs-lookup"><span data-stu-id="e9dcf-119">Setting Application Language Preferences</span></span>](setting-application-language-preferences.md)
-   [<span data-ttu-id="e9dcf-120">Recherche de ressources Win32 PE</span><span class="sxs-lookup"><span data-stu-id="e9dcf-120">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
-   [<span data-ttu-id="e9dcf-121">Recherche de ressources PE non Win32</span><span class="sxs-lookup"><span data-stu-id="e9dcf-121">Locating Non-Win32 PE Resources</span></span>](locating-non-win32-pe-resources.md)
-   [<span data-ttu-id="e9dcf-122">Localisation des ressources et génération de l’application</span><span class="sxs-lookup"><span data-stu-id="e9dcf-122">Localizing Resources and Building the Application</span></span>](localizing-resources-and-building-the-application.md)
-   [<span data-ttu-id="e9dcf-123">MUI : exemple d’application de paramètres système</span><span class="sxs-lookup"><span data-stu-id="e9dcf-123">MUI: System Settings Application Sample</span></span>](mui-system-settings-application-sample.md)
-   [<span data-ttu-id="e9dcf-124">MUI : exemple de paramètres Application-Specific (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="e9dcf-124">MUI: Application-Specific Settings Sample (Windows Vista)</span></span>](mui-application-specific-settings-sample-vista.md)
-   [<span data-ttu-id="e9dcf-125">MUI : exemple de paramètres de Application-Specific (antérieur à Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="e9dcf-125">MUI: Application-Specific Settings Sample (Pre-Windows Vista)</span></span>](mui-application-specific-settings-sample-pre-vista.md)

 

 



