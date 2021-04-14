---
title: Vérification d’UI Automation (UIA Verify)
description: Vérification d’UI Automation (UIA Verify) est une infrastructure de test pour les tests manuels et automatisés de l’implémentation d’un contrôle ou d’une application de Microsoft UI Automation.
ms.assetid: C66AF411-2746-4695-A893-1552B3ED1066
keywords:
- UI Automation Verify
- Vérification de UIA
- Implémentation d’UI Automation, test
- test de l’Automation d’interface utilisateur
- Outils de test de UIA
- Outils de test UI Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b794e5d191c07a9c0db602ebac0f908bbdf960bf
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104381591"
---
# <a name="accessibility-tools---ui-automation-verify-uia-verify"></a><span data-ttu-id="3a7c8-109">Outils d’accessibilité-vérification de l’UI Automation (UIA Verify)</span><span class="sxs-lookup"><span data-stu-id="3a7c8-109">Accessibility tools - UI Automation Verify (UIA Verify)</span></span>

<span data-ttu-id="3a7c8-110">**Vérification d’UI Automation (UIA Verify)** est une infrastructure de test pour les tests manuels et automatisés de l’implémentation d’un contrôle ou d’une application de Microsoft UI Automation.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-110">**UI Automation Verify (UIA Verify)** is a testing framework for manual and automated testing of a control's or application's implementation of Microsoft UI Automation.</span></span> <span data-ttu-id="3a7c8-111">La plupart des fonctionnalités de l’infrastructure de test proviennent d’une DLL appelée WUIATestLibrary.dll.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-111">Most of the testing framework's functionality comes from a DLL called WUIATestLibrary.dll.</span></span> <span data-ttu-id="3a7c8-112">Cette DLL contient le code permettant de tester des fonctionnalités d’automatisation d’interface utilisateur spécifiques et prend également en charge la journalisation des résultats des tests.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-112">This DLL contains the code for testing specific UI Automation functionality, and it also supports logging of the test results.</span></span> <span data-ttu-id="3a7c8-113">Vous pouvez intégrer votre application dans le code de test et procéder à des tests réguliers, automatisés ou à des contrôles ponctuels de vos scénarios d’automatisation d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-113">You can integrate your application into the test code and conduct regular, automated testing or spot checks of your UI Automation scenarios.</span></span>

<span data-ttu-id="3a7c8-114">**UIA Verify** est installé avec le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-114">**UIA Verify** is installed with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3a7c8-115">Il se trouve dans le \\ dossier bin \\ < *version* > \\ < *Platform* > \\ UIAVerify du chemin d’installation du kit de développement logiciel (VisualUIAVerifyNative.exe).</span><span class="sxs-lookup"><span data-stu-id="3a7c8-115">It is located in the \\bin\\<*version*>\\<*platform*>\\UIAVerify folder of the SDK installation path (VisualUIAVerifyNative.exe).</span></span>

<span data-ttu-id="3a7c8-116">**UIA Verify** se compose d’une API appelée bibliothèque de test UI Automation et d’une interface GUI appelée **vérification** de l’interface utilisateur de Visual UI.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-116">**UIA Verify** consists of an API called the UI Automation Test Library, and a GUI interface called Visual **UI Automation Verify**.</span></span> <span data-ttu-id="3a7c8-117">Celles-ci sont décrites dans les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-117">These are described in the following topics.</span></span>

> [!NOTE]
> <span data-ttu-id="3a7c8-118">**UI Automation Verify** est un outil hérité.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-118">**UI Automation Verify** is a legacy tool.</span></span> <span data-ttu-id="3a7c8-119">Nous vous recommandons d’utiliser à la place [Accessibility Insights](https://accessibilityinsights.io/) .</span><span class="sxs-lookup"><span data-stu-id="3a7c8-119">We recommend using [Accessibility Insights](https://accessibilityinsights.io/) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a7c8-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a7c8-120">Requirements</span></span>

<span data-ttu-id="3a7c8-121">UI Automation doit être présent sur le système.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-121">UI Automation must be present on the system.</span></span> <span data-ttu-id="3a7c8-122">Pour plus d’informations, consultez la section « Configuration requise » d' [UI Automation](entry-uiauto-win32.md).</span><span class="sxs-lookup"><span data-stu-id="3a7c8-122">For more information, see the "Requirements" section of [UI Automation](entry-uiauto-win32.md).</span></span>

<span data-ttu-id="3a7c8-123">**UIA Verify** est installé dans le cadre de l’ensemble d’outils de la SDK Windows, il n’est pas distribué en tant que téléchargement séparé.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-123">**UIA Verify** is installed as part of the overall set of tools in the Windows SDK, it is not distributed as a separate download.</span></span> <span data-ttu-id="3a7c8-124">Le SDK Windows comprend tous les outils liés à l’accessibilité documentés dans cette section.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-124">The Windows SDK includes all of the accessibility-related tools documented in this section.</span></span> [<span data-ttu-id="3a7c8-125">Obtient le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="3a7c8-125">Get the Windows SDK.</span></span>](https://developer.microsoft.com/) <span data-ttu-id="3a7c8-126">(Il existe également un kit de développement logiciel (SDK) à partir de cette page, si vous avez besoin d’une version précédente.)</span><span class="sxs-lookup"><span data-stu-id="3a7c8-126">(There's also an SDK download archive linked from that page, if you need a previous version.)</span></span>

<span data-ttu-id="3a7c8-127">Pour exécuter **UIA Verify** comme outil visuel, recherchez VisualUIAVerifyNative.exe dans le \\ dossier bin \\ < *Platform* > \\ UIAVerify et exécutez-le (vous n’êtes généralement pas obligé d’exécuter en tant qu’administrateur).</span><span class="sxs-lookup"><span data-stu-id="3a7c8-127">To run **UIA Verify** as a visual tool, find VisualUIAVerifyNative.exe in the \\bin\\<*platform*>\\UIAVerify folder and run it (you don't typically have to run as administrator).</span></span> <span data-ttu-id="3a7c8-128">Pour plus d’informations, voir [Visual UI Automation Verify](visual-ui-automation-verify.md).</span><span class="sxs-lookup"><span data-stu-id="3a7c8-128">For more information, see [Visual UI Automation Verify](visual-ui-automation-verify.md).</span></span> <span data-ttu-id="3a7c8-129">Pour utiliser les bibliothèques, consultez [UI Automation test Library](ui-automation-test-library.md).</span><span class="sxs-lookup"><span data-stu-id="3a7c8-129">To use the libraries, see [UI Automation Test Library](ui-automation-test-library.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a7c8-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a7c8-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a7c8-131">Accessible Event Watcher</span><span class="sxs-lookup"><span data-stu-id="3a7c8-131">Accessible Event Watcher</span></span>](accessible-event-watcher.md)
</dt> <dt>

[<span data-ttu-id="3a7c8-132">Inspecter</span><span class="sxs-lookup"><span data-stu-id="3a7c8-132">Inspect</span></span>](inspect-objects.md)
</dt> <dt>

[<span data-ttu-id="3a7c8-133">Outils de test</span><span class="sxs-lookup"><span data-stu-id="3a7c8-133">Testing Tools</span></span>](testing-tools.md)
</dt> <dt>

[<span data-ttu-id="3a7c8-134">Vérificateur d’accessibilité de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="3a7c8-134">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




