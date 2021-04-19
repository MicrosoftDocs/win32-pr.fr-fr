---
description: Découvrez comment utiliser l’outil d’analyse d’utilisateur standard (SUA) et l’Assistant SUA pour tester vos applications et détecter les problèmes de compatibilité potentiels.
ms.assetid: 229ee531-32b9-4e11-b64c-3ce5b5ab6530
title: Outil SUA (Standard User Analyzer) et Assistant SUA (Standard User Analyzer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a897c603f185db775c059e4b3dd4a040cba9ad
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314582"
---
# <a name="standard-user-analyzer-sua-tool-and-standard-user-analyzer-wizard-sua-wizard"></a><span data-ttu-id="0e4f3-103">Outil SUA (Standard User Analyzer) et Assistant SUA (Standard User Analyzer)</span><span class="sxs-lookup"><span data-stu-id="0e4f3-103">Standard User Analyzer (SUA) Tool and Standard User Analyzer Wizard (SUA Wizard)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="0e4f3-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="0e4f3-104">Affected Platforms</span></span>

<span data-ttu-id="0e4f3-105">**Clients :** Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e4f3-105">**Clients:** Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="0e4f3-106">**Serveurs :** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0e4f3-106">**Servers:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  

## <a name="description"></a><span data-ttu-id="0e4f3-107">Description</span><span class="sxs-lookup"><span data-stu-id="0e4f3-107">Description</span></span>

<span data-ttu-id="0e4f3-108">Application Compatibility Toolkit comprend l’outil Analyseur utilisateur standard (SUA) et l’Assistant analyseur utilisateur standard (Assistant SUA).</span><span class="sxs-lookup"><span data-stu-id="0e4f3-108">The Application Compatibility Toolkit includes the Standard User Analyzer (SUA) tool and the Standard User Analyzer Wizard (SUA Wizard).</span></span> <span data-ttu-id="0e4f3-109">Ces outils vous permettent de tester vos applications et de surveiller les appels d’API afin de détecter les problèmes de compatibilité potentiels en raison de la fonctionnalité de contrôle de compte utilisateur (UAC) du système d’exploitation Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-109">These tools enable you to test your applications and to monitor API calls in order to detect potential compatibility issues due to the User Account Control (UAC) feature in the Windows 7 operating system.</span></span>

<span data-ttu-id="0e4f3-110">Le contrôle de compte d’utilisateur, anciennement connu sous le nom de compte d’utilisateur limité, exige que tous les utilisateurs (y compris les membres du groupe administrateur) s’exécutent en tant qu’utilisateurs standard à l’aide de la boîte de dialogue d’invite de sécurité jusqu’à ce que l’application soit délibérément élevée.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-110">UAC, formerly known as Limited User Account (LUA), requires that all users (including members of the Administrator group) run as Standard Users by using the security prompt dialog box until the application is deliberately elevated.</span></span> <span data-ttu-id="0e4f3-111">Toutefois, les applications qui requièrent l’accès et les privilèges pour les emplacements qui ne sont pas disponibles pour un utilisateur standard ne peuvent pas s’exécuter correctement avec le rôle d’utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-111">However, applications that require access and privileges for locations that are unavailable to a Standard User cannot run properly with the Standard User role.</span></span>

## <a name="usage"></a><span data-ttu-id="0e4f3-112">Utilisation</span><span class="sxs-lookup"><span data-stu-id="0e4f3-112">Usage</span></span>

<span data-ttu-id="0e4f3-113">Les sections suivantes fournissent des informations détaillées sur l’utilisation des outils de l’Assistant SUA et SUA.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-113">The following sections provide detailed information about how to use the SUA and SUA Wizard tools.</span></span>

<span data-ttu-id="0e4f3-114">**Outil SUA**</span><span class="sxs-lookup"><span data-stu-id="0e4f3-114">**SUA Tool**</span></span>

<span data-ttu-id="0e4f3-115">L’outil SUA vous permet d’analyser une application, de consulter un rapport détaillé sur les problèmes liés au contrôle de compte d’utilisateur, puis d’appliquer les solutions d’atténuation d’application suggérées et sélectionnées, comme indiqué dans l’organigramme suivant.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-115">The SUA tool enables you to analyze an application, review a detailed report about the UAC-related issues, and then apply the suggested and selected application mitigations, as shown in the following flowchart.</span></span>

![Diagramme qui montre le déroulement du S U A Tool.](images/act-suaflowchart-appcookbook.gif)

<span data-ttu-id="0e4f3-117">*Outil et virtualisation SUA*</span><span class="sxs-lookup"><span data-stu-id="0e4f3-117">*SUA Tool and Virtualization*</span></span>

<span data-ttu-id="0e4f3-118">Seul l’outil SUA vous permet d’activer et de désactiver la fonctionnalité de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-118">Only the SUA tool enables you to turn on and off the virtualization feature.</span></span> <span data-ttu-id="0e4f3-119">En désactivant la fonctionnalité de virtualisation, l’application testée se comportera plus comme lorsqu’elle fonctionnera sur le système d’exploitation Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-119">By turning off the virtualization feature, the tested application will behave more like when it is functioning on the Windows XP operating system.</span></span>

<span data-ttu-id="0e4f3-120">*Outil SUA et privilèges élevés*</span><span class="sxs-lookup"><span data-stu-id="0e4f3-120">*SUA Tool and Elevated Privileges*</span></span>

<span data-ttu-id="0e4f3-121">Seul l’outil SUA vous permet d’activer et de désactiver la fonctionnalité **lancer des élévations de privilèges** .</span><span class="sxs-lookup"><span data-stu-id="0e4f3-121">Only the SUA tool enables you to turn on and off the **Launch Elevated** feature.</span></span> <span data-ttu-id="0e4f3-122">La fonctionnalité lancer des élévations de privilèges permet à l’application sélectionnée de s’exécuter en tant qu’administrateur ou en tant qu’utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-122">The Launch Elevated feature enables the selected application to run as an Administrator or as a Standard User.</span></span> <span data-ttu-id="0e4f3-123">Selon votre sélection, vous trouverez différents types de problèmes liés au contrôle de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-123">Depending on your selection, you will locate different types of UAC-related issues.</span></span> <span data-ttu-id="0e4f3-124">Si vous désactivez la case à cocher lancer des privilèges **élevés** , votre application s’exécute avec des privilèges d’administrateur complets, ce qui permet à sua de prédire les problèmes susceptibles de se produire pour un utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-124">If you clear the **Launch Elevated** check box, your application will run with full Administrator privileges, which enables SUA to predict the issues that might occur for a Standard User.</span></span> <span data-ttu-id="0e4f3-125">Si vous activez la case à cocher lancer avec des privilèges élevés, vous verrez des erreurs qui résultent de l’exécution de l’application et de la génération d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-125">If you select the Launch Elevated check box, you will see errors that result from the application actually running and generating errors.</span></span>

<span data-ttu-id="0e4f3-126">**Assistant SUA**</span><span class="sxs-lookup"><span data-stu-id="0e4f3-126">**SUA Wizard**</span></span>

<span data-ttu-id="0e4f3-127">L’Assistant SUA vous permet de suivre un processus étape par étape guidé qui vous permet d’analyser une application, puis d’appliquer les mesures d’atténuation d’application suggérées et sélectionnées, comme indiqué dans l’organigramme suivant.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-127">The SUA Wizard enables you to follow a guided, step-by-step process by which you can analyze an application and then apply the suggested and selected application mitigations, as shown in the following flowchart.</span></span> <span data-ttu-id="0e4f3-128">Contrairement à l’outil SUA, l’Assistant ne permet pas de passer en revue les problèmes détaillés relatifs au contrôle de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-128">Unlike the SUA tool, the wizard does not enable a review of the detailed UAC-related issues.</span></span>

![Diagramme qui montre le déroulement du S U d’un Assistant.](images/act-suaflowchart-appcookbook.gif)

## <a name="links-to-other-resources"></a><span data-ttu-id="0e4f3-130">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="0e4f3-130">Links to Other Resources</span></span>

-   [<span data-ttu-id="0e4f3-131">Téléchargement de l’outil Application Compatibility Toolkit</span><span class="sxs-lookup"><span data-stu-id="0e4f3-131">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="0e4f3-132">[Fonctionnement des outils de l’analyseur d’utilisateurs standard](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="0e4f3-132">[Understanding the Standard User Analyzer Tools](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))</span></span>
-   <span data-ttu-id="0e4f3-133">[Informations techniques de référence sur l’analyseur utilisateur standard](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="0e4f3-133">[Standard User Analyzer Technical Reference](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))</span></span>
-   <span data-ttu-id="0e4f3-134">[Test et atténuation des problèmes à l’aide des outils de développement](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="0e4f3-134">[Testing and Mitigating Issues by Using the Development Tools](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))</span></span>
-   [<span data-ttu-id="0e4f3-135">Compatibilité des applications et contrôle de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="0e4f3-135">Application Compatibility and User Account Control</span></span>](/previous-versions/windows/)

> [!Note]  
> <span data-ttu-id="0e4f3-136">Ces ressources peuvent ne pas être disponibles dans certaines langues et pays/régions.</span><span class="sxs-lookup"><span data-stu-id="0e4f3-136">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
