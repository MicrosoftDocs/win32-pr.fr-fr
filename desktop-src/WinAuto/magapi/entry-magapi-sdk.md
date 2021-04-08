---
title: API de grossissement
description: L’API d’agrandissement permet aux applications d’agrandir la totalité de l’écran ou des parties de l’écran, et d’appliquer des effets de couleur.
ms.assetid: 644af100-82ec-4450-b809-cede9b388cb4
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 7e6c652c2cca8e3c5675b390e93b70ad0b522a44
ms.sourcegitcommit: 541c08d5d36109b754f39bf89e57404f007c5f63
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/08/2020
ms.locfileid: "103841861"
---
# <a name="magnification-api"></a><span data-ttu-id="be051-103">API de grossissement</span><span class="sxs-lookup"><span data-stu-id="be051-103">Magnification API</span></span>

## <a name="purpose"></a><span data-ttu-id="be051-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="be051-104">Purpose</span></span>

<span data-ttu-id="be051-105">L’API d’agrandissement permet aux applications d’agrandir la totalité de l’écran ou des parties de l’écran, et d’appliquer des effets de couleur.</span><span class="sxs-lookup"><span data-stu-id="be051-105">The Magnification API enables applications to magnify the entire screen or portions of the screen, and to apply color effects.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="be051-106">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="be051-106">Where applicable</span></span>

<span data-ttu-id="be051-107">Grâce à l’API d’agrandissement, les développeurs peuvent créer des applications de technologie d’assistance Windows qui agrandissent l’écran et appliquent des effets de couleur au contenu de l’écran agrandi.</span><span class="sxs-lookup"><span data-stu-id="be051-107">By using the Magnification API, developers can create Windows-based assistive-technology applications that magnify the screen and apply color effects to the magnified screen content.</span></span> <span data-ttu-id="be051-108">Pour les utilisateurs dont la vision est faible, la taille de l’image agrandie et les effets de couleur peuvent faciliter l’utilisation et l’utilisation de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="be051-108">For users with low vision, the enlarged image size and color effects can help make the computer easier to see and use.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="be051-109">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="be051-109">Developer audience</span></span>

<span data-ttu-id="be051-110">L’API d’agrandissement est conçue principalement pour les développeurs C et C++ qui comprennent la programmation Windows et qui sont familiarisés avec les concepts de la programmation graphique.</span><span class="sxs-lookup"><span data-stu-id="be051-110">The Magnification API is designed primarily for C and C++ developers who understand Windows programming and who are familiar with graphics programming concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="be051-111">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="be051-111">Run-time requirements</span></span>

<span data-ttu-id="be051-112">La version initiale de l’API d’agrandissement est prise en charge sur Windows Vista et les systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="be051-112">The initial release of the Magnification API is supported on Windows Vista and later operating systems.</span></span> <span data-ttu-id="be051-113">Une deuxième version ajoute des fonctionnalités d’agrandissement plein écran et est prise en charge sur Windows 8 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="be051-113">A second release adds fullscreen magnification capabilities and is supported on Windows 8 and later.</span></span>

<span data-ttu-id="be051-114">L’API est prise en charge par Magnification.dll.</span><span class="sxs-lookup"><span data-stu-id="be051-114">The API is supported by Magnification.dll.</span></span> <span data-ttu-id="be051-115">Pour compiler votre application, incluez grossissement. h et un lien vers grossissement. lib.</span><span class="sxs-lookup"><span data-stu-id="be051-115">To compile your application, include Magnification.h and link to Magnification.lib.</span></span>

> [!Note]  
> <span data-ttu-id="be051-116">L’API d’agrandissement n’est pas prise en charge sous WOW64 ; autrement dit, une application de loupe 32 bits ne s’exécutera pas correctement sous Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="be051-116">The Magnification API is not supported under WOW64; that is, a 32-bit magnifier application will not run correctly on 64-bit Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="be051-117">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="be051-117">In this section</span></span>

| <span data-ttu-id="be051-118">Rubrique</span><span class="sxs-lookup"><span data-stu-id="be051-118">Topic</span></span> | <span data-ttu-id="be051-119">Description</span><span class="sxs-lookup"><span data-stu-id="be051-119">Description</span></span> |
|:---|:---|
| [<span data-ttu-id="be051-120">Vue d’ensemble de l’API zoom</span><span class="sxs-lookup"><span data-stu-id="be051-120">Magnification API Overview</span></span>](magapi-intro.md)<br/> | <span data-ttu-id="be051-121">Cette rubrique décrit l’API d’agrandissement et explique comment l’utiliser dans une application.</span><span class="sxs-lookup"><span data-stu-id="be051-121">This topic describes the Magnification API and explains how to use it in an application.</span></span><br/> |
| [<span data-ttu-id="be051-122">Référence</span><span class="sxs-lookup"><span data-stu-id="be051-122">Reference</span></span>](entry-magapi-ref.md)<br/>  | <span data-ttu-id="be051-123">Cette section contient des informations de référence sur l’API d’agrandissement.</span><span class="sxs-lookup"><span data-stu-id="be051-123">This section contains reference information for the Magnification API.</span></span><br/>|
| [<span data-ttu-id="be051-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="be051-124">Samples</span></span>](magapi-samples-entry.md)<br/> | <span data-ttu-id="be051-125">L’exemple d’application suivant montre comment utiliser l’API de grossissement pour créer une loupe plein écran qui agrandit la totalité de l’écran et une loupe avec fenêtres qui agrandit et affiche une partie de l’écran dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="be051-125">The following sample application demonstrates how to use the Magnification API to create a full screen magnifier that magnifies the entire screen, and a windowed magnifier that magnifies and displays a portion of the screen in a window.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="be051-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be051-126">Related topics</span></span>

<span data-ttu-id="be051-127">[Site Web Microsoft Accessibility](https://www.microsoft.com/accessibility/), [accessibilité dans Windows 10](/windows/apps/accessibility)</span><span class="sxs-lookup"><span data-stu-id="be051-127">[Microsoft Accessibility website](https://www.microsoft.com/accessibility/), [Accessibility in Windows 10](/windows/apps/accessibility)</span></span>
