---
title: Nouveautés (contrôles Windows)
description: Cette rubrique décrit les différences de prise en charge pour les thèmes et les styles visuels entre Windows 8 et les versions antérieures de Windows.
ms.assetid: 866C2E0B-D3AF-4DA0-8B45-D5FF1335C350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b203152c8fae5b844eeab334870bf8efb04ac20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464043"
---
# <a name="whats-new-windows-controls"></a><span data-ttu-id="aabf0-103">Nouveautés (contrôles Windows)</span><span class="sxs-lookup"><span data-stu-id="aabf0-103">What's New (Windows Controls)</span></span>

<span data-ttu-id="aabf0-104">Cette rubrique décrit les différences de prise en charge pour les thèmes et les styles visuels entre Windows 8 et les versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="aabf0-104">This topic describes the differences in support for theming and visual styles between Windows 8 and previous versions of Windows .</span></span>

## <a name="through-windows-7"></a><span data-ttu-id="aabf0-105">Via Windows 7</span><span class="sxs-lookup"><span data-stu-id="aabf0-105">Through Windows 7</span></span>

<span data-ttu-id="aabf0-106">À l’aide de Windows 7, les styles visuels sont activés par défaut, mais l’utilisateur peut les désactiver en sélectionnant thème Windows classique ou en désactivant le service thèmes.</span><span class="sxs-lookup"><span data-stu-id="aabf0-106">Through Windows 7, visual styles are on by default but the user can turn them off by selecting Windows Classic theme or by turning off the Themes service.</span></span> <span data-ttu-id="aabf0-107">Lorsque les styles visuels sont désactivés, toute l’interface utilisateur obtient l’apparence classique, et la plupart des API de styles visuels ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="aabf0-107">When visual styles are off, all UI gets the classic look, and most visual styles APIs are not available.</span></span> <span data-ttu-id="aabf0-108">Le mode de désactivation des styles visuels a été conservé par le biais de Windows 7 pour prendre en charge les différents thèmes à contraste élevé, ainsi que le thème Windows classique.</span><span class="sxs-lookup"><span data-stu-id="aabf0-108">Visual styles off mode has been retained through Windows 7 to support the various high contrast themes, as well as Windows Classic theme.</span></span> <span data-ttu-id="aabf0-109">Si vous souhaitez prendre en charge à la fois les styles visuels et les thèmes à contraste élevé dans la même application, vous devez généralement gérer deux chemins de code distincts pour le rendu des contrôles.</span><span class="sxs-lookup"><span data-stu-id="aabf0-109">If you want to support both visual styles and high contrast themes in the same application, you typically need to maintain two separate code paths for rendering controls.</span></span>

## <a name="windows-8-and-later"></a><span data-ttu-id="aabf0-110">Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="aabf0-110">Windows 8 and Later</span></span>

<span data-ttu-id="aabf0-111">Dans Windows 8, les styles visuels ne peuvent pas être désactivés via la page de **personnalisation** des **paramètres du PC** ou en désactivant le service thèmes.</span><span class="sxs-lookup"><span data-stu-id="aabf0-111">In Windows 8, visual styles can't be turned off through the **Personalization** page of **PC Settings** or by turning off the Themes service.</span></span> <span data-ttu-id="aabf0-112">Le mode Windows classique n’existe plus et le mode contraste élevé a été modifié pour fonctionner avec les styles visuels.</span><span class="sxs-lookup"><span data-stu-id="aabf0-112">Windows Classic mode no longer exists, and high contrast mode has been modified to work with visual styles.</span></span> <span data-ttu-id="aabf0-113">En raison de ces modifications, les applications qui ciblent uniquement Windows 8 n’ont plus besoin de deux chemins de code distincts pour prendre en charge les styles visuels et les thèmes à contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="aabf0-113">Because of these changes, applications that target only Windows 8 no longer need two separate code paths to support visual styles and high contrast themes.</span></span>

<span data-ttu-id="aabf0-114">Les styles visuels dans Windows 8 incluent la prise en charge de la compatibilité descendante pour le mode Windows classique.</span><span class="sxs-lookup"><span data-stu-id="aabf0-114">Visual styles in Windows 8 includes backward compatibility support for Windows Classic theming mode.</span></span> <span data-ttu-id="aabf0-115">Tout code de rendu d’interface utilisateur qui fonctionne sur les versions précédentes continuera à fonctionner sur Windows 8 sans modification.</span><span class="sxs-lookup"><span data-stu-id="aabf0-115">Any UI rendering code that works on previous versions will continue to work on Windows 8 without modifications.</span></span>

<span data-ttu-id="aabf0-116">Dans Windows 8, si vous souhaitez que votre application prenne en charge les thèmes à contraste élevé basés sur des styles visuels, vous devez inclure le GUID Windows 8 dans la section compatibilité de votre manifeste d’application.</span><span class="sxs-lookup"><span data-stu-id="aabf0-116">In Windows 8, if you want your application to support the high contrast themes that are based on visual styles, you need to include the Windows 8 GUID in the compatibility section of your application manifest.</span></span> <span data-ttu-id="aabf0-117">Dans le cas contraire, le système suppose que l’application est conçue pour une version antérieure et restitue la zone cliente en simulant les thèmes à contraste élevé Windows classique.</span><span class="sxs-lookup"><span data-stu-id="aabf0-117">Otherwise, the system assumes that the application is designed for a previous version and renders the client area by simulating Windows classic high contrast themes.</span></span> <span data-ttu-id="aabf0-118">Pour plus d’informations, consultez [prise en charge des thèmes de contraste élevé](supporting-high-contrast-themes.md).</span><span class="sxs-lookup"><span data-stu-id="aabf0-118">For more information, see [Supporting High Contrast Themes](supporting-high-contrast-themes.md).</span></span>

<span data-ttu-id="aabf0-119">Comme dans les versions précédentes, Windows 8 prend en charge la version 5 et la version 6 des contrôles communs, la version 5 étant la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="aabf0-119">As in previous versions, Windows 8 supports both version 5 and version 6 of the common controls, with version 5 being the default.</span></span> <span data-ttu-id="aabf0-120">Étant donné que seule la version 6 prend en charge les styles visuels, vous devez spécifier la version 6 dans votre manifeste d’application si vous souhaitez que les styles visuels soient appliqués aux contrôles communs dans la zone cliente de votre application.</span><span class="sxs-lookup"><span data-stu-id="aabf0-120">Because only version 6 supports visual styles, you must specify version 6 in your application manifest if you want visual styles to be applied to the common controls in your application's client area.</span></span> <span data-ttu-id="aabf0-121">Pour plus d’informations, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="aabf0-121">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aabf0-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aabf0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aabf0-123">Activation des styles visuels</span><span class="sxs-lookup"><span data-stu-id="aabf0-123">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="aabf0-124">Prise en charge des thèmes de contraste élevé</span><span class="sxs-lookup"><span data-stu-id="aabf0-124">Supporting High Contrast Themes</span></span>](supporting-high-contrast-themes.md)
</dt> <dt>

[<span data-ttu-id="aabf0-125">Styles visuels</span><span class="sxs-lookup"><span data-stu-id="aabf0-125">Visual Styles</span></span>](themes-overview.md)
</dt> <dt>

[<span data-ttu-id="aabf0-126">Vue d’ensemble des styles visuels</span><span class="sxs-lookup"><span data-stu-id="aabf0-126">Visual Styles Overview</span></span>](visual-styles-overview.md)
</dt> </dl>

 

 




