---
title: Éléments d’interface utilisateur personnalisés
description: Les développeurs de serveurs conçoivent des objets accessibles en fonction de l’interface utilisateur d’une application.
ms.assetid: d9453fb0-9b4a-4103-81e3-1255091255a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b32a086b977a1737a17206261aaaa94faa754d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839533"
---
# <a name="custom-user-interface-elements"></a><span data-ttu-id="b5cf5-103">Éléments d’interface utilisateur personnalisés</span><span class="sxs-lookup"><span data-stu-id="b5cf5-103">Custom User Interface Elements</span></span>

<span data-ttu-id="b5cf5-104">Les développeurs de serveurs conçoivent des objets accessibles en fonction de l’interface utilisateur d’une application.</span><span class="sxs-lookup"><span data-stu-id="b5cf5-104">Server developers design accessible objects based on an application's UI.</span></span> <span data-ttu-id="b5cf5-105">Étant donné que [Active Accessibility implémente l’interface IAccessible pour le compte des éléments d’interface utilisateur fournis par le système](appendix-a--supported-user-interface-elements-reference.md) , tels que les zones de liste, les menus et les contrôles TrackBar, vous devez implémenter l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) uniquement pour les types d’éléments d’interface utilisateur personnalisés suivants :</span><span class="sxs-lookup"><span data-stu-id="b5cf5-105">Because [Active Accessibility implements the IAccessible interface on behalf of system-provided user interface elements](appendix-a--supported-user-interface-elements-reference.md) such as list boxes, menus, and trackbar controls, you need to implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface only for the following kinds of custom UI elements:</span></span>

-   <span data-ttu-id="b5cf5-106">Contrôles personnalisés créés en inscrivant une classe de fenêtre définie par l’application</span><span class="sxs-lookup"><span data-stu-id="b5cf5-106">Custom controls created by registering an application-defined window class</span></span>
-   <span data-ttu-id="b5cf5-107">Contrôles personnalisés dessinés directement à l’écran qui n’ont pas de **HWND** associé</span><span class="sxs-lookup"><span data-stu-id="b5cf5-107">Custom controls drawn directly on the screen that do not have an associated **HWND**</span></span>
-   <span data-ttu-id="b5cf5-108">Contrôles personnalisés tels que les contrôles Microsoft ActiveX et Java</span><span class="sxs-lookup"><span data-stu-id="b5cf5-108">Custom controls such as Microsoft ActiveX and Java controls</span></span>
-   <span data-ttu-id="b5cf5-109">Les contrôles ou les objets de la fenêtre client de l’application qui ne sont pas déjà exposés</span><span class="sxs-lookup"><span data-stu-id="b5cf5-109">Controls or objects in the application's client window that aren't already exposed</span></span>

<span data-ttu-id="b5cf5-110">Les contrôles et menus owner-drawn sont accessibles tant que vous suivez les instructions présentées dans [raccourcis pour exposer des éléments d’interface utilisateur personnalisés](shortcuts-for-exposing-custom-user-interface-elements.md).</span><span class="sxs-lookup"><span data-stu-id="b5cf5-110">Owner-drawn controls and menus are accessible as long as you follow the guidelines discussed in [Shortcuts for Exposing Custom User Interface Elements](shortcuts-for-exposing-custom-user-interface-elements.md).</span></span> <span data-ttu-id="b5cf5-111">Si vous suivez ces instructions, vous n’avez pas besoin d’implémenter l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour les contrôles et les menus owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="b5cf5-111">If you follow these guidelines, then you do not need to implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for owner-drawn controls and menus.</span></span>

<span data-ttu-id="b5cf5-112">Dans la plupart des cas, les contrôles superclassé et sous-classé sont accessibles car le système gère les fonctionnalités de base du contrôle.</span><span class="sxs-lookup"><span data-stu-id="b5cf5-112">In most cases, superclassed and subclassed controls are accessible because the system handles the basic functionality of the control.</span></span> <span data-ttu-id="b5cf5-113">Toutefois, si un contrôle sous-classé ou sous-classé modifie considérablement le comportement du contrôle fourni par le système sur lequel il est basé, vous devez implémenter l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="b5cf5-113">However, if a superclassed or subclassed control significantly modifies the behavior of the system-provided control on which it is based, then you must implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="b5cf5-114">Pour plus d’informations, consultez [exposition de contrôles basés sur des contrôles système](exposing-controls-based-on-system-controls.md).</span><span class="sxs-lookup"><span data-stu-id="b5cf5-114">For more information, see [Exposing Controls Based on System Controls](exposing-controls-based-on-system-controls.md).</span></span>

<span data-ttu-id="b5cf5-115">Si une application utilise uniquement des éléments d’interface utilisateur fournis par le système, elle n’a pas besoin d’implémenter [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), à l’exception de sa fenêtre cliente.</span><span class="sxs-lookup"><span data-stu-id="b5cf5-115">If an application uses only system-provided user interface elements, then it does not need to implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), except for its client window.</span></span> <span data-ttu-id="b5cf5-116">Par exemple, une application qui comprend un éditeur de texte, qui n’est pas implémentée à l’aide d’un contrôle d’édition, expose des lignes de texte sous forme d’objets accessibles.</span><span class="sxs-lookup"><span data-stu-id="b5cf5-116">For example, an application that includes a text editor, not implemented using an edit control, exposes lines of text as accessible objects.</span></span> <span data-ttu-id="b5cf5-117">Notez que Microsoft Active Accessibility expose automatiquement le texte des contrôles Edit et Rich Edit sous la forme d’une chaîne de texte unique dans la propriété [**value**](value-property.md) du contrôle.</span><span class="sxs-lookup"><span data-stu-id="b5cf5-117">Note that Microsoft Active Accessibility automatically exposes the text in edit and rich edit controls as a single string of text in the [**Value**](value-property.md) property of the control.</span></span>

 

 




