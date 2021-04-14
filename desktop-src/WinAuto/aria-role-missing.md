---
title: Erreur de rôle ARIA pour les éléments avec gestionnaires d’événements
description: Erreur de rôle ARIA pour les éléments avec gestionnaires d’événements
ms.assetid: 20BB874A-874B-4266-9C7B-49C07D4146DA
keywords:
- AriaContainerRoleErrorMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eede416392e8b4cb644938242a9975238118ff07
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383143"
---
# <a name="aria-role-error-for-elements-with-event-handlers"></a><span data-ttu-id="e4e8c-104">Erreur de rôle ARIA pour les éléments avec gestionnaires d’événements</span><span class="sxs-lookup"><span data-stu-id="e4e8c-104">ARIA Role Error for elements with event handlers</span></span>

## <a name="text"></a><span data-ttu-id="e4e8c-105">Texte</span><span class="sxs-lookup"><span data-stu-id="e4e8c-105">Text</span></span>

<span data-ttu-id="e4e8c-106">L’élément a un gestionnaire d’événements mais le rôle WAI-ARIA valide n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="e4e8c-106">Element has an event handler but valid WAI-ARIA role is not defined.</span></span>

## <a name="type"></a><span data-ttu-id="e4e8c-107">Type</span><span class="sxs-lookup"><span data-stu-id="e4e8c-107">Type</span></span>

<span data-ttu-id="e4e8c-108">Error</span><span class="sxs-lookup"><span data-stu-id="e4e8c-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="e4e8c-109">Description</span><span class="sxs-lookup"><span data-stu-id="e4e8c-109">Description</span></span>

<span data-ttu-id="e4e8c-110">Cette erreur s’applique aux éléments qui ne disposent pas d’une initiative d’accessibilité Web implicite, accessible via le rôle WAI-ARIA.</span><span class="sxs-lookup"><span data-stu-id="e4e8c-110">This error applies to elements that do not have an implicit Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role.</span></span>

<span data-ttu-id="e4e8c-111">Cette erreur indique qu’un élément a un gestionnaire d’événements de souris ou de clavier (**clic**, **MouseDown**, **MouseUp**, **MouseMove**, **mouseout**, **MouseOver**, **KeyUp**, **keyverser** ou **touche**), mais ne dispose pas de l’attribut de [**rôle**](https://developer.mozilla.org/docs/Web/HTML/Reference) défini et ne fait pas partie des balises HTML qui ont un rôle WAI-ARIA implicite (par exemple, **un, un** **bouton**, **img**, **entrée**, **Sélectionner**</span><span class="sxs-lookup"><span data-stu-id="e4e8c-111">This error indicates that an element has a mouse or keyboard event handler (**click**, **mousedown**, **mouseup**, **mousemove**, **mouseout**, **mouseover**, **keyup**, **keydown**, or **keypress**), but doesn’t have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute set, and is not one of the HTML tags that has an implicit WAI-ARIA role (for example, **a**, **button**, **img**, **input**, **select** and so on).</span></span>

<span data-ttu-id="e4e8c-112">La définition de l’attribut [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) pour les éléments interactifs qui n’ont pas de rôle implicite (par exemple, une balise **div** ) est nécessaire pour exposer les modèles de comportement de l’élément aux lecteurs d’écran et autres technologies d’assistance.</span><span class="sxs-lookup"><span data-stu-id="e4e8c-112">Setting the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute for interactive elements that have no implicit role (such as a **div** tag) is necessary to expose the element's behavior patterns to screen readers and other assistive technologies.</span></span>

<span data-ttu-id="e4e8c-113">Pour corriger cette erreur, définissez l’attribut de [**rôle**](https://developer.mozilla.org/docs/Web/HTML/Reference) sur un rôle WAI-ARIA valide qui correspond au mieux aux modèles de comportement de cet élément et aux attributs requis.</span><span class="sxs-lookup"><span data-stu-id="e4e8c-113">To fix this error, set the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute to a valid WAI-ARIA role that best fits this element's behavior patterns and required attributes.</span></span> <span data-ttu-id="e4e8c-114">Par exemple, si une balise **div** fonctionne comme un bouton, affectez à l’attribut Role la valeur « Button ».</span><span class="sxs-lookup"><span data-stu-id="e4e8c-114">For example, if a **div** tag functions as a button, set the role attribute to "button".</span></span>

## <a name="example"></a><span data-ttu-id="e4e8c-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="e4e8c-115">Example</span></span>


```HTML
<!-- Setting role attribute allows screen readers to know it can be clicked -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




