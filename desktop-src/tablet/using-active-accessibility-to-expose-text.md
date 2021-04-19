---
description: Vue d’ensemble de l’utilisation d’Active Accessibility pour exposer du texte.
ms.assetid: c04ade90-5f17-4e16-b82b-c99230000954
title: Utilisation de Active Accessibility pour exposer du texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d475a8c576e109f47be7b5a3d61cddf543038d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516863"
---
# <a name="using-active-accessibility-to-expose-text"></a><span data-ttu-id="31667-103">Utilisation de Active Accessibility pour exposer du texte</span><span class="sxs-lookup"><span data-stu-id="31667-103">Using Active Accessibility to Expose Text</span></span>

<span data-ttu-id="31667-104">Les applications peuvent utiliser Microsoft Active Accessibility pour exposer du texte.</span><span class="sxs-lookup"><span data-stu-id="31667-104">Applications can use Microsoft Active Accessibility to expose text.</span></span> <span data-ttu-id="31667-105">Toutefois, l’interface [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) définie par les versions antérieures de Active Accessibility n’est pas optimisée pour exposer de grandes quantités de texte enrichi.</span><span class="sxs-lookup"><span data-stu-id="31667-105">However, the [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) interface defined by earlier versions of Active Accessibility is not optimized for exposing large amounts of rich text.</span></span> <span data-ttu-id="31667-106">Les versions ultérieures définissent des interfaces qui sont optimisées pour exposer de grandes quantités de texte et d’attributs textuels.</span><span class="sxs-lookup"><span data-stu-id="31667-106">Later versions define interfaces that are optimized for exposing large amounts of text and textual attributes.</span></span>

<span data-ttu-id="31667-107">Pour exposer un texte de grandes quantités, créez des objets COM (Component Object Model) distincts qui prennent en charge [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible), ou éléments enfants, pour représenter chaque exécution de texte.</span><span class="sxs-lookup"><span data-stu-id="31667-107">To expose large amounts text, create separate Component Object Model (COM) objects that support [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible), or child elements, to represent each run of text.</span></span> <span data-ttu-id="31667-108">Une exécution est une ligne ou une partie d’une ligne qui partage la même mise en forme.</span><span class="sxs-lookup"><span data-stu-id="31667-108">A run is a line, or portion of a line, that shares the same formatting.</span></span>

<span data-ttu-id="31667-109">Active Accessibility expose uniquement le texte et son emplacement, mais n’a aucun mécanisme pour exposer la mise en forme du texte.</span><span class="sxs-lookup"><span data-stu-id="31667-109">Active Accessibility exposes only the text and its location, but has no mechanism for exposing the formatting of the text.</span></span> <span data-ttu-id="31667-110">Malgré ces limitations, certains programmes utilisent Active Accessibility pour exposer du texte.</span><span class="sxs-lookup"><span data-stu-id="31667-110">Despite these limitations, some programs use Active Accessibility to expose text.</span></span> <span data-ttu-id="31667-111">Par exemple, Microsoft Internet Explorer et Microsoft Visual Studio utilisent tous les deux Active Accessibility pour exposer de grandes quantités de texte.</span><span class="sxs-lookup"><span data-stu-id="31667-111">For example, Microsoft Internet Explorer and Microsoft Visual Studio both use Active Accessibility to expose large amounts of text.</span></span>

<span data-ttu-id="31667-112">Pour plus d’informations sur l’exposition de texte à l’aide de Active Accessibility, consultez [accessibilité](../accessibility/accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="31667-112">For more information about exposing text by using Active Accessibility, see [Accessibility](../accessibility/accessibility.md).</span></span>

 

 
