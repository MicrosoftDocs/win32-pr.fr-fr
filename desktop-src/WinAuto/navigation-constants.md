---
title: Constantes de navigation (oleacc. h)
description: Cette rubrique décrit les valeurs constantes, définies dans oleacc. h, qui indiquent le sens spatial (haut, bas, gauche et droit) ou logique (premier enfant, dernier, suivant et précédent) observé lorsque les clients utilisent IAccessible accNavigate pour naviguer d’un élément d’interface utilisateur à un autre dans le même conteneur.
ms.assetid: 5859a7a3-bcd3-443e-8ff0-4952f4639517
topic_type:
- apiref
api_name:
- NAVDIR_DOWN
- NAVDIR_FIRSTCHILD
- NAVDIR_LASTCHILD
- NAVDIR_LEFT
- NAVDIR_NEXT
- NAVDIR_PREVIOUS
- NAVDIR_RIGHT
- NAVDIR_UP
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8de5f4eaa3fc7fb24583e49bdd14acb9633b2bd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535968"
---
# <a name="navigation-constants"></a><span data-ttu-id="94dad-103">Constantes de navigation</span><span class="sxs-lookup"><span data-stu-id="94dad-103">Navigation Constants</span></span>

<span data-ttu-id="94dad-104">Cette rubrique décrit les valeurs constantes, définies dans oleacc. h, qui indiquent le sens *spatial* (haut, bas, gauche et droit) ou *logique* (premier enfant, dernier, suivant et précédent) observé lorsque les clients utilisent [**IAccessible :: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) pour naviguer d’un élément d’interface utilisateur à un autre dans le même conteneur.</span><span class="sxs-lookup"><span data-stu-id="94dad-104">This topic describes the constant values, defined in oleacc.h, that indicate the *spatial* (up, down, left, and right) or *logical* (first child, last, next, and previous) direction observed when clients use [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) to navigate from one user interface element to another within the same container.</span></span> <span data-ttu-id="94dad-105">Pour plus d’informations, consultez [Propriétés et méthodes de navigation entre les objets](object-navigation-properties-and-methods.md).</span><span class="sxs-lookup"><span data-stu-id="94dad-105">For more information, see [Object Navigation Properties and Methods](object-navigation-properties-and-methods.md).</span></span>

<span data-ttu-id="94dad-106">Les constantes de navigation Microsoft Active Accessibility sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="94dad-106">The Microsoft Active Accessibility navigation constants are as follows:</span></span>



| <span data-ttu-id="94dad-107">Constante</span><span class="sxs-lookup"><span data-stu-id="94dad-107">Constant</span></span>                                                                                                                                                                  | <span data-ttu-id="94dad-108">Description</span><span class="sxs-lookup"><span data-stu-id="94dad-108">Description</span></span>                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NAVDIR_DOWN"></span><span id="navdir_down"></span><dl> <span data-ttu-id="94dad-109"><dt>**NAVDIR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="94dad-109"><dt>**NAVDIR\_DOWN**</dt></span></span> </dl>                   | <span data-ttu-id="94dad-110">Accédez à l’objet frère situé sous l’objet de départ.</span><span class="sxs-lookup"><span data-stu-id="94dad-110">Navigate to the sibling object that is located below the starting object.</span></span><br/>                                                                  |
| <span id="NAVDIR_FIRSTCHILD"></span><span id="navdir_firstchild"></span><dl> <span data-ttu-id="94dad-111"><dt>**NAVDIR \_ firstChild**</dt></span><span class="sxs-lookup"><span data-stu-id="94dad-111"><dt>**NAVDIR\_FIRSTCHILD**</dt></span></span> </dl> | <span data-ttu-id="94dad-112">Naviguez jusqu’au premier enfant de cet objet.</span><span class="sxs-lookup"><span data-stu-id="94dad-112">Navigate to the first child of this object.</span></span> <span data-ttu-id="94dad-113">Lorsque cet indicateur est utilisé, le membre **lVal** du paramètre *VARSTART* doit être CHILDID \_ self.</span><span class="sxs-lookup"><span data-stu-id="94dad-113">When this flag is used, the **lVal** member of the *varStart* parameter must be CHILDID\_SELF.</span></span><br/> |
| <span id="NAVDIR_LASTCHILD"></span><span id="navdir_lastchild"></span><dl> <span data-ttu-id="94dad-114"><dt>**NAVDIR \_ LastChild**</dt></span><span class="sxs-lookup"><span data-stu-id="94dad-114"><dt>**NAVDIR\_LASTCHILD**</dt></span></span> </dl>    | <span data-ttu-id="94dad-115">Naviguez jusqu’au dernier enfant de cet objet.</span><span class="sxs-lookup"><span data-stu-id="94dad-115">Navigate to the last child of this object.</span></span> <span data-ttu-id="94dad-116">Lors de l’utilisation de cet indicateur, le membre **lVal** du paramètre *VARSTART* doit être CHILDID \_ self.</span><span class="sxs-lookup"><span data-stu-id="94dad-116">When using this flag, the **lVal** member of the *varStart* parameter must be CHILDID\_SELF.</span></span><br/>    |
| <span id="NAVDIR_LEFT"></span><span id="navdir_left"></span><dl> <span data-ttu-id="94dad-117"><dt>**NAVDIR \_ gauche**</dt></span><span class="sxs-lookup"><span data-stu-id="94dad-117"><dt>**NAVDIR\_LEFT**</dt></span></span> </dl>                   | <span data-ttu-id="94dad-118">Accédez à l’objet frère situé à gauche de l’objet de départ.</span><span class="sxs-lookup"><span data-stu-id="94dad-118">Navigate to the sibling object located to the left of the starting object.</span></span><br/>                                                                 |
| <span id="NAVDIR_NEXT"></span><span id="navdir_next"></span><dl> <span data-ttu-id="94dad-119"><dt>**NAVDIR \_ suivant**</dt></span><span class="sxs-lookup"><span data-stu-id="94dad-119"><dt>**NAVDIR\_NEXT**</dt></span></span> </dl>                   | <span data-ttu-id="94dad-120">Accédez à l’objet logique suivant ; en règle générale, il s’agit d’un frère de l’objet de départ.</span><span class="sxs-lookup"><span data-stu-id="94dad-120">Navigate to the next logical object; generally, it is a sibling of the starting object.</span></span><br/>                                                    |
| <span id="NAVDIR_PREVIOUS"></span><span id="navdir_previous"></span><dl> <span data-ttu-id="94dad-121"><dt>**NAVDIR \_ précédent**</dt></span><span class="sxs-lookup"><span data-stu-id="94dad-121"><dt>**NAVDIR\_PREVIOUS**</dt></span></span> </dl>       | <span data-ttu-id="94dad-122">Accédez à l’objet logique précédent ; en règle générale, il s’agit d’un frère de l’objet de départ.</span><span class="sxs-lookup"><span data-stu-id="94dad-122">Navigate to the previous logical object; generally, it is a sibling of the starting object.</span></span><br/>                                                |
| <span id="NAVDIR_RIGHT"></span><span id="navdir_right"></span><dl> <span data-ttu-id="94dad-123"><dt>**NAVDIR \_ droit**</dt></span><span class="sxs-lookup"><span data-stu-id="94dad-123"><dt>**NAVDIR\_RIGHT**</dt></span></span> </dl>                | <span data-ttu-id="94dad-124">Accédez à l’objet frère situé à droite de l’objet de départ.</span><span class="sxs-lookup"><span data-stu-id="94dad-124">Navigate to the sibling object that is located to the right of the starting object.</span></span><br/>                                                        |
| <span id="NAVDIR_UP"></span><span id="navdir_up"></span><dl> <span data-ttu-id="94dad-125"><dt>**NAVDIR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="94dad-125"><dt>**NAVDIR\_UP**</dt></span></span> </dl>                         | <span data-ttu-id="94dad-126">Accédez à l’objet frère situé au-dessus de l’objet de départ.</span><span class="sxs-lookup"><span data-stu-id="94dad-126">Navigate to the sibling object that is located above the starting object.</span></span><br/>                                                                  |



## <a name="requirements"></a><span data-ttu-id="94dad-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94dad-127">Requirements</span></span>



| <span data-ttu-id="94dad-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94dad-128">Requirement</span></span> | <span data-ttu-id="94dad-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="94dad-129">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="94dad-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="94dad-130">Header</span></span><br/> | <dl> <span data-ttu-id="94dad-131"><dt>Oleacc. h</dt></span><span class="sxs-lookup"><span data-stu-id="94dad-131"><dt>Oleacc.h</dt></span></span> </dl> |



 

 





