---
title: Haute résolution pour les applications de bureau dans Windows 8.1
description: Haute résolution pour les applications de bureau dans Windows 8.1
ms.assetid: 1E92D3C8-C117-463A-AF31-12D3CAA31E2A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6c223e9dc39cda9a109280926a5eb47a8fffcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509860"
---
# <a name="high-dpi-for-desktop-apps-in-windows-81"></a><span data-ttu-id="9e781-103">Haute résolution pour les applications de bureau dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9e781-103">High DPI for desktop apps in Windows 8.1</span></span>

## <a name="platforms"></a><span data-ttu-id="9e781-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="9e781-104">Platforms</span></span>

<dl> <span data-ttu-id="9e781-105">Clients-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9e781-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="9e781-106">Serveurs-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9e781-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="9e781-107">Description</span><span class="sxs-lookup"><span data-stu-id="9e781-107">Description</span></span>

<span data-ttu-id="9e781-108">Dans Windows 8.1 les applications de bureau sont censées s’exécuter sur des affichages avec une mise à l’échelle de 200% en plus des 100%, 125% et 150% de mise à l’échelle pris en charge dans Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9e781-108">In Windows 8.1 desktop applications are expected to run on displays with 200% scaling in addition to the 100%, 125%, and 150% scaling that is supported in Windows 8.</span></span> <span data-ttu-id="9e781-109">En outre, les applications de bureau sont mises à l’échelle sur une base par moniteur plutôt que sur un seul facteur d’échelle appliqué à tous les affichages.</span><span class="sxs-lookup"><span data-stu-id="9e781-109">In addition, desktop applications are scaled on a per-monitor basis rather than to a single scale factor applied to all displays.</span></span> <span data-ttu-id="9e781-110">Les développeurs peuvent également appeler de nouvelles API dans Windows 8.1 pour bénéficier de facteurs d’échelle par moniteur.</span><span class="sxs-lookup"><span data-stu-id="9e781-110">Developers can also call new APIs in Windows 8.1 to get per-monitor scale factors.</span></span>

## <a name="manifestations"></a><span data-ttu-id="9e781-111">Manifestations</span><span class="sxs-lookup"><span data-stu-id="9e781-111">Manifestations</span></span>

<span data-ttu-id="9e781-112">Les utilisateurs peuvent utiliser de nouveaux affichages à haute densité avec Windows 8.1 pour une expérience visuelle formidable qui tire parti des données de pixel supérieures.</span><span class="sxs-lookup"><span data-stu-id="9e781-112">Users can use new high density displays with Windows 8.1 for a terrific visual experience that takes advantage of the higher pixel data.</span></span> <span data-ttu-id="9e781-113">Si les applications ne gèrent pas les résolutions élevées, Windows les met à l’échelle pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9e781-113">If applications don’t handle high DPI, Windows will scale them for the user.</span></span> <span data-ttu-id="9e781-114">En outre, les utilisateurs peuvent utiliser un mélange d’affichages haute densité et à faible densité sur le même ordinateur, et Windows met à l’échelle le contenu de manière appropriée pour chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="9e781-114">In addition, users can use a mix of high and low density displays on the same computer, and Windows will scale content appropriately for each display.</span></span> <span data-ttu-id="9e781-115">Il s’agit d’une amélioration par rapport à Windows 8, où le contenu peut être trop volumineux sur certains affichages.</span><span class="sxs-lookup"><span data-stu-id="9e781-115">This is an improvement over Windows 8, where content can be too large on some displays.</span></span>

## <a name="mitigation"></a><span data-ttu-id="9e781-116">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="9e781-116">Mitigation</span></span>

<span data-ttu-id="9e781-117">Étant donné que Windows mettra à l’échelle les applications qui ne sont pas mises à l’échelle, les développeurs n’ont généralement pas à effectuer d’autres tâches, mais les développeurs qui investissent dans l’écriture d’applications prenant en charge la haute résolution auront un avantage concurrentiel, car ces applications s’apprendront mieux sur les nouveaux ordinateurs portables haute résolution et les moniteurs de bureau.</span><span class="sxs-lookup"><span data-stu-id="9e781-117">Since Windows will scale apps that don’t scale themselves, developers generally do not have to do additional work, but developers who do invest in writing applications that support high DPI will have a competitive advantage, as those applications will look better on new high DPI laptops and desktop monitors.</span></span>

## <a name="solution"></a><span data-ttu-id="9e781-118">Solution</span><span class="sxs-lookup"><span data-stu-id="9e781-118">Solution</span></span>

<span data-ttu-id="9e781-119">La création d’une application qui peut tirer parti de la haute résolution est une tâche de conception et d’implémentation complexe.</span><span class="sxs-lookup"><span data-stu-id="9e781-119">Making an application that can take advantage of high DPI is a complex design and implementation task.</span></span> <span data-ttu-id="9e781-120">Consultez les liens ci-dessous pour obtenir des informations sur les didacticiels, créer du contenu de présentation et une prise en charge similaire.</span><span class="sxs-lookup"><span data-stu-id="9e781-120">See the links below for tutorial information, BUILD presentation content, and similar support.</span></span>

## <a name="tests"></a><span data-ttu-id="9e781-121">Tests</span><span class="sxs-lookup"><span data-stu-id="9e781-121">Tests</span></span>

<span data-ttu-id="9e781-122">Même si les développeurs choisissent de faire en sorte que leurs applications tirent parti de la haute résolution, ils doivent tester leur application à 100%, 125%, 150% et 200% de mise à l’échelle pour s’assurer que l’expérience de l’utilisateur final est satisfaisante et concurrentielle.</span><span class="sxs-lookup"><span data-stu-id="9e781-122">Even if developers do not choose to make their applications take advantage of high DPI, they should test their application at 100%, 125%, 150%, and 200% scaling to be sure the end-user experience is satisfactory and competitive.</span></span>

## <a name="resources"></a><span data-ttu-id="9e781-123">Ressources</span><span class="sxs-lookup"><span data-stu-id="9e781-123">Resources</span></span>

-   [<span data-ttu-id="9e781-124">Livre blanc et didacticiel sur les résolutions élevées en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9e781-124">White paper and tutorial on high DPI in Windows 8.1</span></span>](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   [<span data-ttu-id="9e781-125">Exemples de programmes de bureau Windows</span><span class="sxs-lookup"><span data-stu-id="9e781-125">Windows desktop sample programs</span></span>](https://www.microsoft.com/?ref=go)
-   [<span data-ttu-id="9e781-126">GÉNÉRATION d’une session de disjoncteur 2013 sur des résolutions élevées en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9e781-126">BUILD 2013 break-out session on high DPI in Windows 8.1</span></span>](https://channel9.msdn.com/Events/Build/2013/4-184)

 

 