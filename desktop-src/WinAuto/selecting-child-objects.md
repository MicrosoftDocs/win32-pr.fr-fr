---
title: Sélection des objets enfants
description: Les clients appellent la méthode IAccessible accSelect pour modifier la sélection ou le focus clavier parmi les enfants d’un objet. Les constantes SELFLAG spécifiées avec l’appel définissent l’opération à effectuer.
ms.assetid: 5e7ad1e9-b1b2-4e76-93e8-b58251930621
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d6f898f7da7beb047d3e781ad46cf383b3dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309497"
---
# <a name="selecting-child-objects"></a><span data-ttu-id="170ed-104">Sélection des objets enfants</span><span class="sxs-lookup"><span data-stu-id="170ed-104">Selecting Child Objects</span></span>

<span data-ttu-id="170ed-105">Les clients appellent la méthode [**IAccessible :: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) pour modifier la sélection ou le focus clavier parmi les enfants d’un objet.</span><span class="sxs-lookup"><span data-stu-id="170ed-105">Clients call the [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method to modify selection or keyboard focus among the children in an object.</span></span> <span data-ttu-id="170ed-106">Les [constantes SELFLAG](selflag.md) spécifiées avec l’appel définissent l’opération à effectuer.</span><span class="sxs-lookup"><span data-stu-id="170ed-106">The [SELFLAG Constants](selflag.md) specified with the call define the operation to perform.</span></span>

<span data-ttu-id="170ed-107">Si [**IAccessible :: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) est appelé avec l’indicateur [**SELFLAG \_ TAKEFOCUS**](selflag.md) sur un objet enfant qui a un **HWND**, l’indicateur prend effet uniquement si le parent de l’objet a le focus.</span><span class="sxs-lookup"><span data-stu-id="170ed-107">If [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) is called with the [**SELFLAG\_TAKEFOCUS**](selflag.md) flag on a child object that has an **HWND**, the flag takes effect only if the object's parent has the focus.</span></span>

## <a name="performing-complex-selection-operations"></a><span data-ttu-id="170ed-108">Exécution d’opérations de sélection complexes</span><span class="sxs-lookup"><span data-stu-id="170ed-108">Performing Complex Selection Operations</span></span>

<span data-ttu-id="170ed-109">Les éléments suivants décrivent les valeurs SELFLAG à spécifier lors de l’appel de [**IAccessible :: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) pour effectuer des opérations de sélection complexes.</span><span class="sxs-lookup"><span data-stu-id="170ed-109">The following describes which SELFLAG values to specify when calling [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) to perform complex selection operations.</span></span>

<span data-ttu-id="170ed-110">**Pour simuler un clic**</span><span class="sxs-lookup"><span data-stu-id="170ed-110">**To simulate a click**</span></span>

-   <span data-ttu-id="170ed-111">[**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ TAKESELECTION**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="170ed-111">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_TAKESELECTION**](selflag.md)</span></span>

<span data-ttu-id="170ed-112">**Pour sélectionner un élément cible en simulant CTRL + clic**</span><span class="sxs-lookup"><span data-stu-id="170ed-112">**To select a target item by simulating CTRL + click**</span></span>

-   <span data-ttu-id="170ed-113">[**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ ADDSELECTION**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="170ed-113">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_ADDSELECTION**](selflag.md)</span></span>

<span data-ttu-id="170ed-114">**Pour annuler la sélection d’un élément cible en simulant CTRL + clic**</span><span class="sxs-lookup"><span data-stu-id="170ed-114">**To cancel selection of a target item by simulating CTRL + click**</span></span>

-   <span data-ttu-id="170ed-115">[**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ REMOVESELECTION**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="170ed-115">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_REMOVESELECTION**](selflag.md)</span></span>

<span data-ttu-id="170ed-116">**Pour simuler MAJ + clic**</span><span class="sxs-lookup"><span data-stu-id="170ed-116">**To simulate SHIFT + click**</span></span>

-   <span data-ttu-id="170ed-117">[**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ EXTENDSELECTION**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="170ed-117">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_EXTENDSELECTION**](selflag.md)</span></span>

<span data-ttu-id="170ed-118">**Pour sélectionner une plage d’objets et placer le focus sur le dernier objet**</span><span class="sxs-lookup"><span data-stu-id="170ed-118">**To select a range of objects and put focus on the last object**</span></span>

1.  <span data-ttu-id="170ed-119">Spécifiez [**SELFLAG \_ TAKEFOCUS**](selflag.md) sur l’objet de départ pour définir l’ancre de sélection.</span><span class="sxs-lookup"><span data-stu-id="170ed-119">Specify [**SELFLAG\_TAKEFOCUS**](selflag.md) on the starting object to set the selection anchor.</span></span>
2.  <span data-ttu-id="170ed-120">Appelez à nouveau [**IAccessible :: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) et spécifiez [**SELFLAG \_ EXTENDSELECTION**](selflag.md) \| [**SELFLAG \_ TAKEFOCUS**](selflag.md) sur le dernier objet.</span><span class="sxs-lookup"><span data-stu-id="170ed-120">Call [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) again and specify [**SELFLAG\_EXTENDSELECTION**](selflag.md) \| [**SELFLAG\_TAKEFOCUS**](selflag.md) on the last object.</span></span>

<span data-ttu-id="170ed-121">**Pour désélectionner tous les objets**</span><span class="sxs-lookup"><span data-stu-id="170ed-121">**To deselect all objects**</span></span>

1.  <span data-ttu-id="170ed-122">Spécifiez [**SELFLAG \_ TAKESELECTION**](selflag.md) sur n’importe quel objet.</span><span class="sxs-lookup"><span data-stu-id="170ed-122">Specify [**SELFLAG\_TAKESELECTION**](selflag.md) on any object.</span></span> <span data-ttu-id="170ed-123">Cet indicateur Désélectionne tous les objets sélectionnés, à l’exception de ceux que vous venez de sélectionner.</span><span class="sxs-lookup"><span data-stu-id="170ed-123">This flag deselects all selected objects except the one just selected.</span></span>
2.  <span data-ttu-id="170ed-124">Appelez à nouveau [**IAccessible :: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) et spécifiez [**SELFLAG \_ REMOVESELECTION**](selflag.md) sur l’objet restant.</span><span class="sxs-lookup"><span data-stu-id="170ed-124">Call [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) again and specify [**SELFLAG\_REMOVESELECTION**](selflag.md) on the remaining object.</span></span>

 

 




