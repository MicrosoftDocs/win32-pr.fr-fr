---
title: Styles visuels
description: Cette section fournit une vue d’ensemble des styles visuels et explique comment configurer votre application pour qu’elle les utilise.
ms.assetid: 9b135ccb-5e36-4657-b79c-689201047430
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38bb1f8ff84f2c9f4d268ec8b50f8e7688519ed3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029049"
---
# <a name="visual-styles"></a><span data-ttu-id="54e12-103">Styles visuels</span><span class="sxs-lookup"><span data-stu-id="54e12-103">Visual Styles</span></span>

## <a name="purpose"></a><span data-ttu-id="54e12-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="54e12-104">Purpose</span></span>

<span data-ttu-id="54e12-105">Les *styles visuels* modifient l’apparence des contrôles communs en fonction du thème choisi par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="54e12-105">*Visual styles* changes the appearance of common controls based on the theme chosen by the user.</span></span> <span data-ttu-id="54e12-106">Avant Windows 8, vous devez configurer votre application pour qu’elle utilise des styles visuels spécifiques. Sinon, les contrôles communs de l’application sont toujours rendus dans le style associé au thème Windows classique, quel que soit le thème actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="54e12-106">Prior to Windows 8, you must specifically configure your application to use visual styles; otherwise, the application's common controls are always rendered in the style associated with the Windows Classic theme, regardless of the currently selected theme.</span></span> <span data-ttu-id="54e12-107">Dans Windows 8, les styles visuels ne peuvent pas être désactivés, le mode Windows classique n’existe plus et le mode contraste élevé a été modifié pour fonctionner avec les styles visuels.</span><span class="sxs-lookup"><span data-stu-id="54e12-107">In Windows 8, visual styles can't be turned off, Windows Classic mode no longer exists, and high contrast mode has been modified to work with visual styles.</span></span>

<span data-ttu-id="54e12-108">Cette section fournit une vue d’ensemble des styles visuels et explique comment configurer votre application pour qu’elle les utilise.</span><span class="sxs-lookup"><span data-stu-id="54e12-108">This section provides an overview of visual styles and explains how to configure your application to use them.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="54e12-109">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="54e12-109">Developer audience</span></span>

<span data-ttu-id="54e12-110">Les styles visuels sont conçus pour être utilisés par les développeurs C/C++ et les concepteurs d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="54e12-110">Visual styles are designed for use by C/C++ developers and UI designers.</span></span> <span data-ttu-id="54e12-111">En général, les développeurs ont besoin d’un niveau modéré de compréhension des concepts de programmation d’interface utilisateur, de la programmation d’API Windows et d’Unicode.</span><span class="sxs-lookup"><span data-stu-id="54e12-111">In general, developers need a moderate level of understanding about UI programming concepts, Windows API programming, and Unicode.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="54e12-112">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="54e12-112">Run-time requirements</span></span>

<span data-ttu-id="54e12-113">Windows Vista et systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="54e12-113">Windows Vista and later operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="54e12-114">Les styles visuels ne sont pas pris en charge en mode 256-Color.</span><span class="sxs-lookup"><span data-stu-id="54e12-114">Visual Styles are not supported in 256-color mode.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="54e12-115">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="54e12-115">In this section</span></span>

-   [<span data-ttu-id="54e12-116">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="54e12-116">What's New</span></span>](what-s-new-for-windows-8.md)
-   [<span data-ttu-id="54e12-117">Vue d’ensemble des styles visuels</span><span class="sxs-lookup"><span data-stu-id="54e12-117">Visual Styles Overview</span></span>](visual-styles-overview.md)
-   [<span data-ttu-id="54e12-118">Activation des styles visuels</span><span class="sxs-lookup"><span data-stu-id="54e12-118">Enabling Visual Styles</span></span>](cookbook-overview.md)
-   [<span data-ttu-id="54e12-119">Utilisation de styles visuels avec des contrôles personnalisés et Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="54e12-119">Using Visual Styles with Custom and Owner-Drawn Controls</span></span>](using-visual-styles.md)
-   [<span data-ttu-id="54e12-120">Prise en charge des thèmes de contraste élevé</span><span class="sxs-lookup"><span data-stu-id="54e12-120">Supporting High Contrast Themes</span></span>](supporting-high-contrast-themes.md)
-   [<span data-ttu-id="54e12-121">Référence des styles visuels</span><span class="sxs-lookup"><span data-stu-id="54e12-121">Visual Styles Reference</span></span>](uxctl-ref.md)

## <a name="related-topics"></a><span data-ttu-id="54e12-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="54e12-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54e12-123">Format du fichier de thème</span><span class="sxs-lookup"><span data-stu-id="54e12-123">Theme File Format</span></span>](themesfileformat-overview.md)
</dt> <dt>

[<span data-ttu-id="54e12-124">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="54e12-124">Windows Controls</span></span>](window-controls.md)
</dt> </dl>

 

 




