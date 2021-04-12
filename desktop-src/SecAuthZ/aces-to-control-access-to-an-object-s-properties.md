---
description: Entrées de contrôle d’accès pour contrôler l’accès aux propriétés d’objets
ms.assetid: 79dd4a45-c42c-4775-93ce-6e3206894d63
title: Entrées de contrôle d’accès pour contrôler l’accès aux propriétés d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1068ceb994e72deedcb795586ddf712fe9c1893
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202530"
---
# <a name="aces-to-control-access-to-an-objects-properties"></a><span data-ttu-id="024b2-103">Entrées de contrôle d’accès pour contrôler l’accès aux propriétés d’un objet</span><span class="sxs-lookup"><span data-stu-id="024b2-103">ACEs to Control Access to an Object's Properties</span></span>

<span data-ttu-id="024b2-104">La [*liste de contrôle d’accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) d’un objet de service d’annuaire peut contenir une hiérarchie d’entrées de contrôle d’accès (ACE, [*Access Control Entries*](/windows/desktop/SecGloss/a-gly) ), comme suit :</span><span class="sxs-lookup"><span data-stu-id="024b2-104">The [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of a directory service (DS) object can contain a hierarchy of [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), as follows:</span></span>

1.  <span data-ttu-id="024b2-105">ACE qui protègent l’objet lui-même</span><span class="sxs-lookup"><span data-stu-id="024b2-105">ACEs that protect the object itself</span></span>
2.  <span data-ttu-id="024b2-106">[ACE spécifiques](object-specific-aces.md) à l’objet qui protègent un jeu de propriétés spécifié sur l’objet</span><span class="sxs-lookup"><span data-stu-id="024b2-106">[Object-specific ACEs](object-specific-aces.md) that protect a specified property set on the object</span></span>
3.  <span data-ttu-id="024b2-107">ACE spécifiques à l’objet qui protègent une propriété spécifiée sur l’objet</span><span class="sxs-lookup"><span data-stu-id="024b2-107">Object-specific ACEs that protect a specified property on the object</span></span>

<span data-ttu-id="024b2-108">Au sein de cette hiérarchie, les droits accordés ou refusés à un niveau supérieur s’appliquent également aux niveaux inférieurs.</span><span class="sxs-lookup"><span data-stu-id="024b2-108">Within this hierarchy, the rights granted or denied at a higher level apply also to the lower levels.</span></span> <span data-ttu-id="024b2-109">Par exemple, si une entrée de contrôle d’accès spécifique à un objet sur un jeu de propriétés autorise un tiers de confiance \_ \_ à lire la propriété DS \_ Read \_ prop, le tiers de confiance dispose d’un accès en lecture implicite à toutes les propriétés de ce jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="024b2-109">For example, if an object-specific ACE on a property set allows a trustee the ADS\_RIGHT\_DS\_READ\_PROP right, the trustee has implicit read access to all of the properties of that property set.</span></span> <span data-ttu-id="024b2-110">De la même façon, une entrée de contrôle d’accès sur l’objet lui-même qui autorise les publicités \_ appropriées \_ pour l' \_ accès en lecture DS permet \_ au tiers de confiance d’accéder en lecture à toutes les propriétés de l’objet.</span><span class="sxs-lookup"><span data-stu-id="024b2-110">Similarly, an ACE on the object itself that allows ADS\_RIGHT\_DS\_READ\_PROP access gives the trustee read access to all of the object's properties.</span></span>

<span data-ttu-id="024b2-111">L’illustration suivante montre l’arborescence d’un objet de service d’annuaire hypothétique et de ses jeux de propriétés et propriétés.</span><span class="sxs-lookup"><span data-stu-id="024b2-111">The following illustration shows the tree of a hypothetical DS object and its property sets and properties.</span></span>

![hiérarchie d’objets de service d’annuaire](images/accctrl2.png)

<span data-ttu-id="024b2-113">Supposons que vous souhaitez autoriser l’accès suivant aux propriétés de cet objet DS :</span><span class="sxs-lookup"><span data-stu-id="024b2-113">Suppose you want to allow the following access to the properties of this DS object:</span></span>

-   <span data-ttu-id="024b2-114">Autoriser le groupe A une autorisation de lecture/écriture sur toutes les propriétés de l’objet</span><span class="sxs-lookup"><span data-stu-id="024b2-114">Allow Group A read/write permission to all of the object's properties</span></span>
-   <span data-ttu-id="024b2-115">Autoriser tout le monde à accéder en lecture/écriture à toutes les propriétés, à l’exception de la propriété D</span><span class="sxs-lookup"><span data-stu-id="024b2-115">Allow everyone else read/write permission to all properties except Property D</span></span>

<span data-ttu-id="024b2-116">Pour ce faire, définissez les ACE dans la liste DACL de l’objet, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="024b2-116">To do this, set the ACEs in the object's DACL as shown in the following table.</span></span>



| <span data-ttu-id="024b2-117">Tiers</span><span class="sxs-lookup"><span data-stu-id="024b2-117">Trustee</span></span>  | <span data-ttu-id="024b2-118">GUID de l’objet</span><span class="sxs-lookup"><span data-stu-id="024b2-118">Object GUID</span></span>    | <span data-ttu-id="024b2-119">Type d’entrée de contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="024b2-119">ACE type</span></span>                  | <span data-ttu-id="024b2-120">Droits d’accès</span><span class="sxs-lookup"><span data-stu-id="024b2-120">Access rights</span></span>                                             |
|----------|----------------|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="024b2-121">Group A</span><span class="sxs-lookup"><span data-stu-id="024b2-121">Group A</span></span>  | <span data-ttu-id="024b2-122">Aucun</span><span class="sxs-lookup"><span data-stu-id="024b2-122">None</span></span>           | <span data-ttu-id="024b2-123">Accès-ACE autorisé</span><span class="sxs-lookup"><span data-stu-id="024b2-123">Access-allowed ACE</span></span>        | <span data-ttu-id="024b2-124">droits \_ d' \_ \_ \_ \| \_ \_ \_ écriture DS \_ de lecture de la prop.</span><span class="sxs-lookup"><span data-stu-id="024b2-124">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="024b2-125">Tout le monde</span><span class="sxs-lookup"><span data-stu-id="024b2-125">Everyone</span></span> | <span data-ttu-id="024b2-126">Jeu de propriétés 1</span><span class="sxs-lookup"><span data-stu-id="024b2-126">Property Set 1</span></span> | <span data-ttu-id="024b2-127">ACE de l’objet Access-allowed</span><span class="sxs-lookup"><span data-stu-id="024b2-127">Access-allowed object ACE</span></span> | <span data-ttu-id="024b2-128">droits \_ d' \_ \_ \_ \| \_ \_ \_ écriture DS \_ de lecture de la prop.</span><span class="sxs-lookup"><span data-stu-id="024b2-128">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="024b2-129">Tout le monde</span><span class="sxs-lookup"><span data-stu-id="024b2-129">Everyone</span></span> | <span data-ttu-id="024b2-130">Propriété C</span><span class="sxs-lookup"><span data-stu-id="024b2-130">Property C</span></span>     | <span data-ttu-id="024b2-131">ACE de l’objet Access-allowed</span><span class="sxs-lookup"><span data-stu-id="024b2-131">Access-allowed object ACE</span></span> | <span data-ttu-id="024b2-132">droits \_ d' \_ \_ \_ \| \_ \_ \_ écriture DS \_ de lecture de la prop.</span><span class="sxs-lookup"><span data-stu-id="024b2-132">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |



 

<span data-ttu-id="024b2-133">L’entrée du contrôle d’accès pour le groupe A n’a pas de GUID d’objet, ce qui signifie qu’elle autorise l’accès à toutes les propriétés de l’objet.</span><span class="sxs-lookup"><span data-stu-id="024b2-133">The ACE for Group A does not have an object GUID, which means that it allows access to all the object's properties.</span></span> <span data-ttu-id="024b2-134">L’ACE spécifique à l’objet pour le jeu de propriétés 1 autorise tout le monde à accéder aux propriétés A et B. L’autre entrée du contrôle d’accès spécifique à l’objet permet à tout le monde d’accéder à la propriété C. Notez que même si cette liste DACL n’a pas d’ACE d’accès refusé, elle refuse implicitement l’accès à la propriété D à tout le monde, sauf le groupe A.</span><span class="sxs-lookup"><span data-stu-id="024b2-134">The object-specific ACE for Property Set 1 allows everyone access to Properties A and B. The other object-specific ACE allows everyone access to Property C. Note that although this DACL does not have any access-denied ACEs, it implicitly denies Property D access to everyone except Group A.</span></span>

<span data-ttu-id="024b2-135">Lorsqu’un utilisateur tente d’accéder à la propriété d’un objet, le système vérifie les ACE, dans l’ordre, jusqu’à ce que l’accès demandé soit explicitement accordé, refusé ou qu’il n’y ait plus d’entrées de contrôle d’accès, auquel cas l’accès est refusé implicitement.</span><span class="sxs-lookup"><span data-stu-id="024b2-135">When a user tries to access an object's property, the system checks the ACEs, in order, until the requested access is explicitly granted, denied, or there are no more ACEs, in which case, access is implicitly denied.</span></span>

<span data-ttu-id="024b2-136">Le système évalue les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="024b2-136">The system evaluates:</span></span>

-   <span data-ttu-id="024b2-137">ACE qui s’appliquent à l’objet lui-même</span><span class="sxs-lookup"><span data-stu-id="024b2-137">ACEs that apply to the object itself</span></span>
-   <span data-ttu-id="024b2-138">ACE spécifiques à l’objet qui s’appliquent au jeu de propriétés qui contient la propriété en cours d’accès</span><span class="sxs-lookup"><span data-stu-id="024b2-138">Object-specific ACEs that apply to the property set that contains the property being accessed</span></span>
-   <span data-ttu-id="024b2-139">ACE spécifiques aux objets qui s’appliquent à la propriété faisant l’objet d’un accès</span><span class="sxs-lookup"><span data-stu-id="024b2-139">Object-specific ACEs that apply to the property being accessed</span></span>

<span data-ttu-id="024b2-140">Le système ignore les ACE spécifiques aux objets qui s’appliquent à d’autres jeux de propriétés ou propriétés.</span><span class="sxs-lookup"><span data-stu-id="024b2-140">The system ignores object-specific ACEs that apply to other property sets or properties.</span></span>

 

 
