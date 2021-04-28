---
description: Outils de développement Internet Explorer 8
ms.assetid: D721167E-B04B-4B06-A9EE-56711A7A1942
title: Outils de développement Internet Explorer 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a4314d5d0392b9bc4933b945f7da32040e1570
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088207"
---
# <a name="internet-explorer-8-developer-tools"></a><span data-ttu-id="13379-103">Outils de développement Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="13379-103">Internet Explorer 8 Developer Tools</span></span>

<span data-ttu-id="13379-104">Windows Internet Explorer 8 comprend la fonctionnalité Outils de développement.</span><span class="sxs-lookup"><span data-stu-id="13379-104">Windows Internet Explorer 8 includes the Developer Tools feature.</span></span> <span data-ttu-id="13379-105">Cette fonctionnalité vous permet de déboguer rapidement Microsoft JScript, d’examiner un comportement spécifique à Windows Internet Explorer ou d’effectuer des itérations rapides pour créer un prototype ou tester une nouvelle solution de conception.</span><span class="sxs-lookup"><span data-stu-id="13379-105">This feature enables you to debug Microsoft JScript quickly, investigate a Windows Internet Explorer-specific behavior, or iterate rapidly to prototype or test a new design solution.</span></span>

<span data-ttu-id="13379-106">Les sections suivantes décrivent les caractéristiques importantes de la Outils de développement dans Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="13379-106">The following sections describe the important characteristics of the Developer Tools in Internet Explorer 8.</span></span>

## <a name="integrated-and-simple-to-use"></a><span data-ttu-id="13379-107">Intégré et simple à utiliser</span><span class="sxs-lookup"><span data-stu-id="13379-107">Integrated and Simple to Use</span></span>

<span data-ttu-id="13379-108">Les Outils de développement sont inclus avec chaque installation d’Internet Explorer 8, ce qui vous permet de déboguer les problèmes sur tout ordinateur qui exécute Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="13379-108">The Developer Tools are included with every installation of Internet Explorer 8, so you can debug issues on any computer that is running Internet Explorer 8.</span></span> <span data-ttu-id="13379-109">En outre, les outils se chargent uniquement lorsque vous en avez besoin pour limiter la manière dont ils ont un impact sur les performances du navigateur.</span><span class="sxs-lookup"><span data-stu-id="13379-109">In addition, the tools load only when you need them to limit how they impact the browser's performance.</span></span> <span data-ttu-id="13379-110">À l’aide de l’Outils de développement, vous pouvez rapidement déboguer le processus Internet Explorer actuel au lieu de déboguer tous les services Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="13379-110">By using the Developer Tools, you can rapidly debug only the current Internet Explorer process, instead of debugging for all of Internet Explorer.</span></span>

## <a name="provide-a-visual-interface-to-the-platform"></a><span data-ttu-id="13379-111">Fournir une interface visuelle à la plateforme</span><span class="sxs-lookup"><span data-stu-id="13379-111">Provide a Visual Interface to the Platform</span></span>

<span data-ttu-id="13379-112">Au lieu d’inverser le fonctionnement de votre site Web ou de modifier votre site pour générer des informations de débogage, les Outils de développement vous permettent de consulter la représentation de votre site dans Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="13379-112">Instead of reverse engineering how your website works or modifying your site to output debug information, the Developer Tools let you look into Internet Explorer to view its representation of your site.</span></span> <span data-ttu-id="13379-113">Cette vue réduit le temps que vous consacrez au débogage de sites dynamiques, où l’inspection de la source n’est pas utile, ou l’examen d’un comportement spécifique à Internet Explorer, où un outil générique de création ne peut pas vous aider.</span><span class="sxs-lookup"><span data-stu-id="13379-113">This view reduces the time that you spend debugging dynamic sites, where source inspection is not useful, or investigating an Internet Explorer-specific behavior, where a generic authoring tool cannot help.</span></span>

## <a name="enable-fast-experimentation"></a><span data-ttu-id="13379-114">Activer l’expérimentation rapide</span><span class="sxs-lookup"><span data-stu-id="13379-114">Enable Fast Experimentation</span></span>

<span data-ttu-id="13379-115">Lorsque vous prototypagez une nouvelle conception ou des correctifs de test dans les versions précédentes d’Internet Explorer, vous modifiez probablement votre source, vous l’enregistrez, actualisez votre page dans le navigateur, puis répétez la procédure.</span><span class="sxs-lookup"><span data-stu-id="13379-115">When you are prototyping a new design or testing fixes in previous versions of Internet Explorer, you likely edit your source, save it, refresh your page in the browser, and repeat.</span></span> <span data-ttu-id="13379-116">La Outils de développement simplifier ce scénario en vous permettant de modifier votre site dans le navigateur et d’afficher immédiatement les modifications.</span><span class="sxs-lookup"><span data-stu-id="13379-116">The Developer Tools streamline this scenario by enabling you to edit your site within the browser and see changes immediately.</span></span>

## <a name="optimize-application-performance"></a><span data-ttu-id="13379-117">Optimiser les performances de l’application</span><span class="sxs-lookup"><span data-stu-id="13379-117">Optimize Application Performance</span></span>

<span data-ttu-id="13379-118">Pour identifier et résoudre les problèmes de performances, vous devez probablement vous concentrer sur un scénario à la fois.</span><span class="sxs-lookup"><span data-stu-id="13379-118">To identify and fix performance issues, you likely iterate by focusing on one scenario at a time.</span></span> <span data-ttu-id="13379-119">En utilisant le profileur de script dans le Outils de développement, vous pouvez collecter des statistiques, notamment la durée d’exécution et le nombre de fois qu’une fonction JavaScript est appelée.</span><span class="sxs-lookup"><span data-stu-id="13379-119">By using the script profiler in the Developer Tools, you can collect statistics, including execution time and the number of times that a JavaScript function is called.</span></span> <span data-ttu-id="13379-120">Vous pouvez utiliser ces informations lorsque vous testez votre application et utilisez le rapport de profil pour identifier et résoudre rapidement les goulots d’étranglement des performances.</span><span class="sxs-lookup"><span data-stu-id="13379-120">You can use this information as you test your application and use the profile report to quickly identify and fix performance bottlenecks.</span></span>

<span data-ttu-id="13379-121">Pour accéder à la Outils de développement, appuyez sur F12 pendant que vous affichez une page Web ou cliquez sur **outils de développement** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="13379-121">To access the Developer Tools, press F12 while you are viewing a webpage or click **Developer Tools** on the **Tools** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13379-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="13379-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13379-123">Outils de débogage d’applications Web et de modules complémentaires</span><span class="sxs-lookup"><span data-stu-id="13379-123">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 



