---
title: Test avec AccChecker
description: Décrit le flux de travail de test classique qui incorpore AccChecker.
ms.assetid: 18C2DDEE-D199-4C22-9ADF-1E07B1325A06
keywords:
- test avec AccChecker
- AccChecker, test du flux de travail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8bb90ce0d9fdde290bfb0f3ce0ee9f873f2b6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507071"
---
# <a name="testing-with-accchecker"></a><span data-ttu-id="e7ed2-105">Test avec AccChecker</span><span class="sxs-lookup"><span data-stu-id="e7ed2-105">Testing with AccChecker</span></span>

<span data-ttu-id="e7ed2-106">Le scénario suivant décrit les étapes que vous suivez généralement lors des tests avec AccChecker.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-106">The following scenario describes the steps that you typically follow when testing with AccChecker.</span></span>

> [!Note]  
> <span data-ttu-id="e7ed2-107">Lorsque les routines de vérification AccChecker sont en cours d’exécution, l’interaction de l’utilisateur avec l’ordinateur hôte peut interférer avec certaines routines.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-107">When AccChecker verification routines are running, user interaction with the host machine can interfere with some routines.</span></span> <span data-ttu-id="e7ed2-108">Nous vous recommandons de ne pas avoir d’interaction avec l’utilisateur tant que AccChecker n’a pas averti l’utilisateur que toutes les tâches sont terminées.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-108">We recommend that no further user interaction occur until AccChecker notifies the user that all tasks are complete.</span></span>

 

1.  <span data-ttu-id="e7ed2-109">Exécutez des vérifications AccChecker sur une application ou un contrôle cible spécifique.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-109">Run AccChecker verifications on a particular target application or control.</span></span> <span data-ttu-id="e7ed2-110">Pour plus d’informations, consultez l' [onglet vérifications](the-accchecker-graphical-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="e7ed2-110">For more information, see [Verifications Tab](the-accchecker-graphical-user-interface.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="e7ed2-111">AccChecker n’explore pas toutes les permutations d’interface utilisateur dans une application.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-111">AccChecker doesn't explore all UI permutations in an application.</span></span> <span data-ttu-id="e7ed2-112">Les éléments masqués dans des contrôles tels que des fenêtres, des volets, des onglets et des menus doivent être exposés manuellement.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-112">Elements hidden within controls such as windows, panes, tabs, and menus must be exposed manually.</span></span>

     

2.  <span data-ttu-id="e7ed2-113">Examinez le journal des erreurs AccChecker et évaluez ou triez les résultats.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-113">Examine the AccChecker error log and assess or triage the results.</span></span> <span data-ttu-id="e7ed2-114">Corrigez les problèmes noordinaires et consignez les bogues graves comme il convient.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-114">Fix trivial issues and log severe bugs as appropriate.</span></span>
3.  <span data-ttu-id="e7ed2-115">Générez un fichier de suppression pour les bogues et les erreurs qui peuvent être ignorés jusqu’au test de régression.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-115">Generate a suppression file for bugs and errors that can be ignored until regression testing.</span></span>
4.  <span data-ttu-id="e7ed2-116">Réexécutez les vérifications AccChecker avec le fichier de suppression et les correctifs de bogues initiaux.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-116">Re-run AccChecker verifications with the suppression file and initial bug fixes.</span></span> <span data-ttu-id="e7ed2-117">Cela fournit un instantané des problèmes de l’implémentation actuelle de Microsoft Active Accessibility et établit une ligne de base pour les tests de régression.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-117">This provides a snapshot of the issues in the current implementation of Microsoft Active Accessibility and establishes a baseline for regression testing.</span></span>
5.  <span data-ttu-id="e7ed2-118">Intégrez les API AccChecker et le fichier de suppression dans une infrastructure de tests automatisés pour le test de régression sur les bogues enregistrés à partir des vérifications AccChecker initiales.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-118">Integrate the AccChecker APIs and suppression file into an automated test framework for regression testing on bugs logged from the initial AccChecker verifications.</span></span>
    > [!Note]  
    > <span data-ttu-id="e7ed2-119">À mesure que les bogues sont résolus, le fichier de suppression doit être modifié en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-119">As bugs are fixed, the suppression file should be modified as required.</span></span>

     

6.  <span data-ttu-id="e7ed2-120">Confirmez qu’aucune régression ou nouveau bogue d’accessibilité n’a été introduit dans l’application ou le contrôle.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-120">Confirm that no regressions or new accessibility bugs have been introduced into the application or control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7ed2-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e7ed2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7ed2-122">Vérificateur d’accessibilité de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="e7ed2-122">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




