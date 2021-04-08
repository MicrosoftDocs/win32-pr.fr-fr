---
title: Outil de test de compatibilité avec la plateforme Microsoft (MPR, Microsoft Platform Ready)
description: Outil de test de compatibilité avec la plateforme Microsoft (MPR, Microsoft Platform Ready)
ms.assetid: C41FBE70-E392-4FD0-954B-6C24168CB93E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6286e7ed64f013a8ea002ea392ba0d3bcac67296
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730725"
---
# <a name="microsoft-platform-ready-test-tool"></a><span data-ttu-id="7ad15-103">Outil de test de compatibilité avec la plateforme Microsoft (MPR, Microsoft Platform Ready)</span><span class="sxs-lookup"><span data-stu-id="7ad15-103">Microsoft Platform Ready Test Tool</span></span>

## <a name="platform"></a><span data-ttu-id="7ad15-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="7ad15-104">Platform</span></span>

 <span data-ttu-id="7ad15-105">**Serveurs** – windows server 2012 \| Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7ad15-105">**Servers** – Windows Server 2012 \| Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="7ad15-106">Description</span><span class="sxs-lookup"><span data-stu-id="7ad15-106">Description</span></span>

<span data-ttu-id="7ad15-107">L’outil de test MPR (Microsoft Platform Ready) est utilisé pour la préparation des applications de plateforme et pour valider la conformité avec les exigences de certification pour les applications Windows Server 2012 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="7ad15-107">The Microsoft Platform Ready (MPR) Test Tool is used for platform application readiness and to validate compliance with certification requirements for Windows Server 2012 and Windows Server 2012 R2 applications.</span></span>

<span data-ttu-id="7ad15-108">Microsoft encourage vivement à incorporer l’outil de test MPR dans les processus de génération et de test de logiciels, garantissant ainsi la préparation des plateformes avant la publication des applications sur le marché.</span><span class="sxs-lookup"><span data-stu-id="7ad15-108">Microsoft strongly encourages incorporating the MPR Test Tool into the software build and test processes, thereby ensuring platform readiness before applications are released to market.</span></span> <span data-ttu-id="7ad15-109">L’outil de test MPR est également un outil recommandé pour tester la compatibilité des applications métier et pour évaluer les produits serveur pour la compatibilité de leurs plateformes avant de prendre des décisions d’achat.</span><span class="sxs-lookup"><span data-stu-id="7ad15-109">The MPR Test Tool is also a recommended tool to test line of business applications and for evaluating server products for their platform compatibility before making purchasing decisions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ad15-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ad15-110">Requirements</span></span>

<span data-ttu-id="7ad15-111">L’outil de test MPR comprend des tests automatisés pour :</span><span class="sxs-lookup"><span data-stu-id="7ad15-111">The MPR Test Tool includes automated tests for:</span></span>

-   <span data-ttu-id="7ad15-112">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="7ad15-112">Windows Installer</span></span>
-   <span data-ttu-id="7ad15-113">Configuration et fonctionnalités principales</span><span class="sxs-lookup"><span data-stu-id="7ad15-113">Setup and Primary Functionality</span></span>
-   <span data-ttu-id="7ad15-114">Pilotes et sécurité</span><span class="sxs-lookup"><span data-stu-id="7ad15-114">Drivers and Security</span></span>
-   <span data-ttu-id="7ad15-115">Bonnes pratiques</span><span class="sxs-lookup"><span data-stu-id="7ad15-115">Best Practices</span></span>

<span data-ttu-id="7ad15-116">L’auto-test et la soumission des résultats pour la plupart des applications serveur doivent durer 2 heures au maximum ; les applications plus complexes peuvent durer environ 4 heures.</span><span class="sxs-lookup"><span data-stu-id="7ad15-116">Self-testing and submission of results for most Server apps should take 2 hours or less; more complex apps can take around 4 hours.</span></span>

<span data-ttu-id="7ad15-117">Tous les pilotes doivent passer séparément le test de certification matérielle Windows et être signés par Microsoft pour Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="7ad15-117">All drivers must separately pass Windows Hardware Certification testing and be signed by Microsoft for Windows Server 2012.</span></span>

## <a name="usage"></a><span data-ttu-id="7ad15-118">Utilisation</span><span class="sxs-lookup"><span data-stu-id="7ad15-118">Usage</span></span>

<span data-ttu-id="7ad15-119">Pour tester vos applications :</span><span class="sxs-lookup"><span data-stu-id="7ad15-119">To test your apps:</span></span>

1.  <span data-ttu-id="7ad15-120">Installez la dernière configuration minimale de Windows Server 2012 (interface utilisateur graphique complète, interface serveur minimale ou Server Core), selon les besoins de votre application.</span><span class="sxs-lookup"><span data-stu-id="7ad15-120">Install the latest Windows Server 2012 minimum configuration (Full Server GUI, Minimal Server Interface, or Server Core) as required for your app.</span></span>
2.  <span data-ttu-id="7ad15-121">Passez en revue les conditions de certification.</span><span class="sxs-lookup"><span data-stu-id="7ad15-121">Review the certification requirements.</span></span>
3.  <span data-ttu-id="7ad15-122">Sur un système propre, exécutez l’outil de test MPR en mode d’interface utilisateur complet ou en mode de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7ad15-122">On a clean system, run the MPR Test Tool in either full UI mode or command line mode.</span></span>
4.  <span data-ttu-id="7ad15-123">Terminez le processus de test auto-guidé.</span><span class="sxs-lookup"><span data-stu-id="7ad15-123">Complete the self-guided testing process.</span></span>
5.  <span data-ttu-id="7ad15-124">Passez en revue les résultats et corrigez votre application selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="7ad15-124">Review results and fix your app as required.</span></span>
6.  <span data-ttu-id="7ad15-125">Connectez-vous et téléchargez les résultats réussis sur le portail Microsoft pour les plateformes prêtes à être répertoriés dans le catalogue Windows Server et l’utilisation du logo.</span><span class="sxs-lookup"><span data-stu-id="7ad15-125">Sign-in and upload successful results to Microsoft Platform Ready portal for listing in Windows Server Catalog and usage of the logo.</span></span>

## <a name="resources"></a><span data-ttu-id="7ad15-126">Ressources</span><span class="sxs-lookup"><span data-stu-id="7ad15-126">Resources</span></span>

-   [<span data-ttu-id="7ad15-127">Configuration requise pour le programme de certification des applications Windows Server</span><span class="sxs-lookup"><span data-stu-id="7ad15-127">Requirements for Windows Server App Certification Program</span></span>](../win_cert/certification-requirements-for-windows-desktop-apps.md)
-   [<span data-ttu-id="7ad15-128">Outil de test de compatibilité avec la plateforme Microsoft (MPR, Microsoft Platform Ready)</span><span class="sxs-lookup"><span data-stu-id="7ad15-128">Microsoft Platform Ready (MPR) Test Tool</span></span>](https://www.microsoft.com/download/details.aspx?id=37143)
-   [<span data-ttu-id="7ad15-129">Programme de certification des applications Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ad15-129">Windows Server 2012 Application Certification Program</span></span>](https://azure.microsoft.com/overview/commercial-marketplace/)
-   [<span data-ttu-id="7ad15-130">Commentaires sur le logo Windows Server</span><span class="sxs-lookup"><span data-stu-id="7ad15-130">Windows Server Logo Feedback</span></span>](mailto:WSLogoFB@microsoft.com)

 

 