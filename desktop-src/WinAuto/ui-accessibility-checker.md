---
title: Outils d’accessibilité-AccChecker (vérificateur d’accessibilité de l’interface utilisateur)
description: Décrit AccChecker (UI Accessibility Checker), un outil de test de l’implémentation UI Automation ou Microsoft Active Accessibility (MSAA) d’une application.
ms.assetid: 92155984-356A-4774-A99D-35B15A3BB704
keywords:
- Vérificateur d’accessibilité de l’interface utilisateur
- AccChecker
- Implémentation d’UI Automation, test
- Implémentation de UIA, test
- Implémentation de Microsoft Active Accessibility, test
- Implémentation MSAA, test
- test de l’Automation d’interface utilisateur
- test de UIA
- test de Microsoft Active Accessibility
- test de MSAA
- Outils de test de UIA
- Outils de test UI Automation
- Outils de test MSAA
- Outils de test Microsoft Active Accessibility
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d2b85436735bfa08f8fc73cf4e465b11d71630
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "106510871"
---
# <a name="accessibility-tools---accchecker-ui-accessibility-checker"></a><span data-ttu-id="bf36d-117">Outils d’accessibilité-AccChecker (vérificateur d’accessibilité de l’interface utilisateur)</span><span class="sxs-lookup"><span data-stu-id="bf36d-117">Accessibility tools - AccChecker (UI Accessibility Checker)</span></span>

<span data-ttu-id="bf36d-118">**AccChecker** (outil d’analyse d’accessibilité de l’interface utilisateur) vérifie que les exigences d’accessibilité de l’interface utilisateur clés sont respectées dans la conception et l’implémentation d’UI Automation (UIA) ou de Microsoft Active Accessibility (MSAA) indépendamment de l’infrastructure d’interface utilisateur sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="bf36d-118">**AccChecker** (UI Accessibility Checker) verifies that key UI accessibility requirements are met in the design and implementation of UI Automation (UIA) or Microsoft Active Accessibility (MSAA) regardless of the underlying UI framework.</span></span> <span data-ttu-id="bf36d-119">**AccChecker** comprend également un ensemble de vérifications de l’accessibilité du Web.</span><span class="sxs-lookup"><span data-stu-id="bf36d-119">**AccChecker** also includes a set of web accessibility verifications.</span></span>

<span data-ttu-id="bf36d-120">**AccChecker** fournit les niveaux de fonctionnalité suivants :</span><span class="sxs-lookup"><span data-stu-id="bf36d-120">**AccChecker** provides the following levels of functionality:</span></span>

- <span data-ttu-id="bf36d-121">Application GUI Windows qui prend en charge les tests manuels, la journalisation des messages et la génération de suppressions.</span><span class="sxs-lookup"><span data-stu-id="bf36d-121">A Windows GUI application that supports manual testing, message logging, and suppression generation.</span></span>
- <span data-ttu-id="bf36d-122">API à utiliser dans les infrastructures de tests automatisés.</span><span class="sxs-lookup"><span data-stu-id="bf36d-122">An API for use in automated testing frameworks.</span></span>
- <span data-ttu-id="bf36d-123">Application console qui prend en charge les automations de test non managées pour les scénarios où l’API managée **AccChecker** ne peut pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="bf36d-123">A console application that supports unmanaged test automations for scenarios where the **AccChecker** managed API can't be used.</span></span>

<span data-ttu-id="bf36d-124">Tous les niveaux de fonctionnalités **AccChecker** fournissent des routines pour vérifier l’accès par programme de Microsoft Active Accessibility, la génération d’événements par programme, la disposition des contrôles et la navigation au clavier.</span><span class="sxs-lookup"><span data-stu-id="bf36d-124">All levels of **AccChecker** functionality provide routines for verifying Microsoft Active Accessibility programmatic access, programmatic event generation, control layout, and keyboard navigation.</span></span> <span data-ttu-id="bf36d-125">**AccChecker** fournit également un service de transcription de lecteur d’écran de base.</span><span class="sxs-lookup"><span data-stu-id="bf36d-125">**AccChecker** also provides a basic screen reader transcription service.</span></span>

<span data-ttu-id="bf36d-126">**AccChecker** est installé avec le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="bf36d-126">**AccChecker** is installed with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bf36d-127">Il se trouve dans le \\ dossier bin \\ < *version* > \\ < *Platform* > \\ AccChecker du chemin d’installation du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="bf36d-127">It is located in the \\bin\\<*version*>\\<*platform*>\\AccChecker folder of the SDK installation path.</span></span>

> [!NOTE]
> <span data-ttu-id="bf36d-128">**AccChecker** est un outil hérité.</span><span class="sxs-lookup"><span data-stu-id="bf36d-128">**AccChecker** is a legacy tool.</span></span> <span data-ttu-id="bf36d-129">Nous vous recommandons d’utiliser à la place [Accessibility Insights](https://accessibilityinsights.io/) .</span><span class="sxs-lookup"><span data-stu-id="bf36d-129">We recommend using [Accessibility Insights](https://accessibilityinsights.io/) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf36d-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf36d-130">Requirements</span></span>

<span data-ttu-id="bf36d-131">Requiert .NET Framework 2,0 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bf36d-131">Requires .NET Framework 2.0 or later.</span></span>

<span data-ttu-id="bf36d-132">**AccChecker** peut être utilisé pour examiner les données d’accessibilité sur les systèmes qui n’ont pas Microsoft UI Automation, mais qui peuvent uniquement examiner les propriétés de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="bf36d-132">**AccChecker** can be used to examine accessibility data on systems that don't have Microsoft UI Automation, but can only examine the Microsoft Active Accessibility properties.</span></span> <span data-ttu-id="bf36d-133">Pour examiner l’Automation d’interface utilisateur, UI Automation doit être présent sur le système.</span><span class="sxs-lookup"><span data-stu-id="bf36d-133">To examine UI Automation, UI Automation must be present on the system.</span></span> <span data-ttu-id="bf36d-134">Pour plus d’informations, consultez la section « Configuration requise » d' [UI Automation](entry-uiauto-win32.md).</span><span class="sxs-lookup"><span data-stu-id="bf36d-134">For more information, see the "Requirements" section of [UI Automation](entry-uiauto-win32.md).</span></span>

<span data-ttu-id="bf36d-135">**AccChecker** est installé dans le cadre du jeu d’outils global dans le kit de développement logiciel (SDK) le, il n’est pas distribué en tant que téléchargement de fichier exécutable distinct.</span><span class="sxs-lookup"><span data-stu-id="bf36d-135">**AccChecker** is installed as part of the overall set of tools in theWindows SDK, it is not distributed as a separate exe download.</span></span> <span data-ttu-id="bf36d-136">Le SDK Windows comprend tous les outils liés à l’accessibilité documentés dans cette section.</span><span class="sxs-lookup"><span data-stu-id="bf36d-136">The Windows SDK includes all of the accessibility-related tools documented in this section.</span></span> [<span data-ttu-id="bf36d-137">Obtient le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="bf36d-137">Get the Windows SDK.</span></span>](https://developer.microsoft.com/) <span data-ttu-id="bf36d-138">(Il existe également un kit de développement logiciel (SDK) à partir de cette page, si vous avez besoin d’une version précédente.)</span><span class="sxs-lookup"><span data-stu-id="bf36d-138">(There's also an SDK download archive linked from that page, if you need a previous version.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf36d-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bf36d-139">Related topics</span></span>

- [<span data-ttu-id="bf36d-140">Accessible Event Watcher</span><span class="sxs-lookup"><span data-stu-id="bf36d-140">Accessible Event Watcher</span></span>](accessible-event-watcher.md)
- [<span data-ttu-id="bf36d-141">Inspecter</span><span class="sxs-lookup"><span data-stu-id="bf36d-141">Inspect</span></span>](inspect-objects.md)
- [<span data-ttu-id="bf36d-142">Outils de test</span><span class="sxs-lookup"><span data-stu-id="bf36d-142">Testing Tools</span></span>](testing-tools.md)
- [<span data-ttu-id="bf36d-143">UI Automation Verify</span><span class="sxs-lookup"><span data-stu-id="bf36d-143">UI Automation Verify</span></span>](ui-automation-verify.md)
