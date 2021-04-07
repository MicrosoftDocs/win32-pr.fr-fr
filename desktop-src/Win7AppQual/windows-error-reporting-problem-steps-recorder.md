---
description: .
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Rapport d’erreurs Windows l’enregistreur des étapes du problème
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25fb70acef867b878063bd6011fde6867f7f0e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759784"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a><span data-ttu-id="271b9-103">Rapport d’erreurs Windows l’enregistreur des étapes du problème</span><span class="sxs-lookup"><span data-stu-id="271b9-103">Windows Error Reporting Problem Steps Recorder</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="271b9-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="271b9-104">Affected Platforms</span></span>

<span data-ttu-id="271b9-105">**Clients** – Windows 7</span><span class="sxs-lookup"><span data-stu-id="271b9-105">**Clients** – Windows 7</span></span>  
<span data-ttu-id="271b9-106">**Serveurs** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="271b9-106">**Servers** – Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="271b9-107">Description</span><span class="sxs-lookup"><span data-stu-id="271b9-107">Description</span></span>

<span data-ttu-id="271b9-108">Avant Windows 7, Rapport d’erreurs Windows (WER) a collecté des rapports d’erreurs qui indiquaient des problèmes nécessitant une réparation.</span><span class="sxs-lookup"><span data-stu-id="271b9-108">Prior to Windows 7, Windows Error Reporting (WER) collected error reports that indicated problems in need of repair.</span></span> <span data-ttu-id="271b9-109">Ces rapports d’erreurs contiennent des informations utiles qui décrivent la nature générale d’un problème, mais pas suffisamment d’informations pour en déterminer la cause racine.</span><span class="sxs-lookup"><span data-stu-id="271b9-109">These error reports contain helpful information that describes the general nature of a problem, but not enough information to determine its root cause.</span></span> <span data-ttu-id="271b9-110">Pour cela, les développeurs ont besoin d’un outil pour reproduire le scénario de blocage/blocage du débogage.</span><span class="sxs-lookup"><span data-stu-id="271b9-110">For that, developers need a tool to reproduce the crash/hang scenario for debugging.</span></span>

<span data-ttu-id="271b9-111">Une nouvelle application, enregistreur des étapes du problème (PSR.exe), est livrée sur toutes les builds de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="271b9-111">A new application, Problem Steps Recorder (PSR.exe), is shipping on all builds of Windows 7.</span></span> <span data-ttu-id="271b9-112">Cette fonctionnalité active la collecte des actions effectuées par un utilisateur tout en rencontrant un incident afin que les testeurs et les développeurs puissent reproduire la situation pour l’analyse et le débogage.</span><span class="sxs-lookup"><span data-stu-id="271b9-112">This feature enables the collection of the actions performed by a user while encountering a crash so that testers and developers can reproduce the situation for analysis and debugging.</span></span>

## <a name="usage"></a><span data-ttu-id="271b9-113">Utilisation</span><span class="sxs-lookup"><span data-stu-id="271b9-113">Usage</span></span>

<span data-ttu-id="271b9-114">Actuellement, un développeur de service Rapport d’erreurs Windows doit demander l’activation d’un V.L.Q.P.R.D. pour une application ; Les organisations du support technique Microsoft utilisent également cet outil lors de la résolution des problèmes avec les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="271b9-114">Currently, a Windows Error Reporting service developer must request PSR enablement for an application; Microsoft support organizations also use this tool while troubleshooting with end users.</span></span> <span data-ttu-id="271b9-115">Des plans sont en place pour rendre les V.Q.P.R.D. disponibles dans Windows Quality Online Services (winqual) après la sortie de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="271b9-115">Plans are in place to make PSR available at Windows Quality Online Services (Winqual) after the release of Windows 7.</span></span>

<span data-ttu-id="271b9-116">**Remarque :** Avec les V.Q.P.R.D. activés pour une application, l’application peut constater une dégradation des performances.</span><span class="sxs-lookup"><span data-stu-id="271b9-116">**Note:** With PSR enabled for an application, the application may see some performance degradation.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="271b9-117">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="271b9-117">Links to Other Resources</span></span>

-   [<span data-ttu-id="271b9-118">Entrée de blog Rapport d’erreurs Windows</span><span class="sxs-lookup"><span data-stu-id="271b9-118">Windows Error Reporting blog entry</span></span>](/archive/blogs/wer/)
-   [<span data-ttu-id="271b9-119">Windows Quality Online Services (winqual)</span><span class="sxs-lookup"><span data-stu-id="271b9-119">Windows Quality Online Services (Winqual)</span></span>](https://winqual.microsoft.com)

 

 
