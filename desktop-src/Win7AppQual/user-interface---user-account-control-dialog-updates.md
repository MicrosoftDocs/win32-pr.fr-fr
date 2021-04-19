---
description: .
ms.assetid: f2d4b82d-a84a-4fc1-b7ad-cdc92a24f889
title: Interface utilisateur-mises à jour de la boîte de dialogue contrôle de compte d’utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5711f8bbed029102bea81e0f4cfcbd4649b5a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535071"
---
# <a name="user-interface---user-account-control-dialog-updates"></a><span data-ttu-id="d12e6-103">Interface utilisateur-mises à jour de la boîte de dialogue contrôle de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="d12e6-103">User Interface - User Account Control Dialog Updates</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="d12e6-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="d12e6-104">Affected Platforms</span></span>

<span data-ttu-id="d12e6-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="d12e6-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="d12e6-106">**Serveurs** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d12e6-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="d12e6-107">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="d12e6-107">Feature Impact</span></span>

<span data-ttu-id="d12e6-108">**Gravité** -faible</span><span class="sxs-lookup"><span data-stu-id="d12e6-108">**Severity** - Low</span></span>  
<span data-ttu-id="d12e6-109">**Fréquence** -moyenne</span><span class="sxs-lookup"><span data-stu-id="d12e6-109">**Frequency** - Medium</span></span>  











## <a name="description"></a><span data-ttu-id="d12e6-110">Description</span><span class="sxs-lookup"><span data-stu-id="d12e6-110">Description</span></span>

<span data-ttu-id="d12e6-111">Dans Windows 7, nous avons standardisé les options de la boîte de dialogue UAC.</span><span class="sxs-lookup"><span data-stu-id="d12e6-111">In Windows 7, we have standardized the UAC dialog box choices.</span></span> <span data-ttu-id="d12e6-112">Auparavant, les utilisateurs devaient sélectionner plusieurs options, par exemple « continuer », « annuler », et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="d12e6-112">Previously, users had to select from multiple options, for example, "Continue," "Cancel," and so on.</span></span> <span data-ttu-id="d12e6-113">Désormais, toutes les boîtes de dialogue donnent aux utilisateurs un simple « oui » ou « non ».</span><span class="sxs-lookup"><span data-stu-id="d12e6-113">Now all dialog boxes give users a simple "Yes" or "No."</span></span> <span data-ttu-id="d12e6-114">La disposition de la boîte de dialogue affiche maintenant également clairement le nom du programme, l’éditeur et l’origine.</span><span class="sxs-lookup"><span data-stu-id="d12e6-114">The dialog layout now also clearly shows the program name, publisher, and origin.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="d12e6-115">Exploitation des fonctionnalités de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="d12e6-115">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="d12e6-116">Les exigences en matière de développement d’applications dans Windows 7 pour la compatibilité avec le contrôle de compte d’utilisateur sont les mêmes que dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d12e6-116">The application development requirements in Windows 7 for UAC compatibility are the same as in Windows Vista.</span></span> <span data-ttu-id="d12e6-117">Les applications compatibles Windows Vista interagissent avec le contrôle de compte d’utilisateur dans Windows 7 sans aucune modification.</span><span class="sxs-lookup"><span data-stu-id="d12e6-117">Windows Vista-compatible applications will interact with UAC in Windows 7 without any modifications.</span></span> <span data-ttu-id="d12e6-118">Pour plus d’informations sur la façon de faire fonctionner correctement les applications Windows XP sur Windows 7, consultez les rubriques relatives au contrôle de compte d’utilisateur dans le Guide de *compatibilité des applications Windows Vista* .</span><span class="sxs-lookup"><span data-stu-id="d12e6-118">See the User Account Control topics in the *Windows Vista Application Compatibility Cookbook* for information about how to make Windows XP applications work correctly on Windows 7.</span></span> <span data-ttu-id="d12e6-119">Alors que les améliorations du contrôle de compte d’utilisateur pour Windows 7 ont un impact sur l’expérience de l’utilisateur, elles n’ont pas d’impact sur l’interface de l’application.</span><span class="sxs-lookup"><span data-stu-id="d12e6-119">While the UAC improvements for Windows 7 will impact the user's experience, they will not impact the application interface.</span></span> <span data-ttu-id="d12e6-120">Toutefois, si un contenu d’aide est lié aux boîtes de dialogue UAC, vous devrez peut-être mettre à jour les captures d’écran.</span><span class="sxs-lookup"><span data-stu-id="d12e6-120">However, if there is any help content linked to the UAC dialogs, you may need to update the screenshots.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="d12e6-121">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="d12e6-121">Links to Other Resources</span></span>

-   <span data-ttu-id="d12e6-122">[Guide de compatibilité des applications Windows Vista](/previous-versions/bb757005(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="d12e6-122">[Windows Vista Application Compatibility Cookbook](/previous-versions/bb757005(v=msdn.10))</span></span>
-   [<span data-ttu-id="d12e6-123">Téléchargement de l’outil Application Compatibility Toolkit</span><span class="sxs-lookup"><span data-stu-id="d12e6-123">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="d12e6-124">[Standard User Analyzer (Analyseur pour utilisateur standard)](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="d12e6-124">[Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span></span>

> [!Note]  
> <span data-ttu-id="d12e6-125">Ces ressources peuvent ne pas être disponibles dans certaines langues et pays/régions.</span><span class="sxs-lookup"><span data-stu-id="d12e6-125">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
