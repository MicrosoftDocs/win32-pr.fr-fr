---
title: Choix des propriétés à prendre en charge
description: Les propriétés IAccessible permettent aux développeurs de serveurs de décrire un large éventail d’éléments d’interface utilisateur.
ms.assetid: c51fd8a1-dc23-4d64-8921-e0a795c3ffb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c88a808889403f88d414f7ad950b3e431c00e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310501"
---
# <a name="choosing-which-properties-to-support"></a><span data-ttu-id="abc52-103">Choix des propriétés à prendre en charge</span><span class="sxs-lookup"><span data-stu-id="abc52-103">Choosing Which Properties to Support</span></span>

<span data-ttu-id="abc52-104">Les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) permettent aux développeurs de serveurs de décrire un large éventail d’éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="abc52-104">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties provide a way for server developers to describe a wide variety of user interface elements.</span></span> <span data-ttu-id="abc52-105">Toutefois, les propriétés ne sont pas toutes applicables pour chaque type d’élément d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="abc52-105">But not all of the properties are applicable for every kind of user interface element.</span></span> <span data-ttu-id="abc52-106">En outre, certaines propriétés fournissent des informations descriptives qui sont utiles, mais pas essentielles.</span><span class="sxs-lookup"><span data-stu-id="abc52-106">Additionally, some properties provide descriptive information that is useful but not essential.</span></span>

<span data-ttu-id="abc52-107">Les serveurs doivent prendre en charge les propriétés et méthodes suivantes pour chaque objet :</span><span class="sxs-lookup"><span data-stu-id="abc52-107">Servers must support the following properties and methods for every object:</span></span>

-   [<span data-ttu-id="abc52-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="abc52-108">**Name**</span></span>](name-property.md)
-   [<span data-ttu-id="abc52-109">**Rôle**</span><span class="sxs-lookup"><span data-stu-id="abc52-109">**Role**</span></span>](role-property.md)
-   [<span data-ttu-id="abc52-110">**State**</span><span class="sxs-lookup"><span data-stu-id="abc52-110">**State**</span></span>](state-property.md)
-   <span data-ttu-id="abc52-111">[**Emplacement**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) et [ **IAccessible :: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)</span><span class="sxs-lookup"><span data-stu-id="abc52-111">[**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) and [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)</span></span>
-   <span data-ttu-id="abc52-112">[**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) et [ **IAccessible :: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)</span><span class="sxs-lookup"><span data-stu-id="abc52-112">[**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) and [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)</span></span>

<span data-ttu-id="abc52-113">Les propriétés et la méthode suivantes doivent être prises en charge si elles s’appliquent à l’objet :</span><span class="sxs-lookup"><span data-stu-id="abc52-113">The following properties and method must be supported if they are applicable to the object:</span></span>

-   [<span data-ttu-id="abc52-114">**KeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="abc52-114">**KeyboardShortcut**</span></span>](keyboardshortcut-property.md)
-   [<span data-ttu-id="abc52-115">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="abc52-115">**Value**</span></span>](value-property.md)

<span data-ttu-id="abc52-116">Les propriétés et la méthode suivantes doivent être prises en charge si l’objet a des enfants :</span><span class="sxs-lookup"><span data-stu-id="abc52-116">The following properties and method must be supported if the object has children:</span></span>

-   <span data-ttu-id="abc52-117">[**Enfant**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) et [ **ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)</span><span class="sxs-lookup"><span data-stu-id="abc52-117">[**Child**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) and [**ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)</span></span>
-   <span data-ttu-id="abc52-118">[**Focus, sélection**](selection-and-focus-properties-and-methods.md)et [ **IAccessible :: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)</span><span class="sxs-lookup"><span data-stu-id="abc52-118">[**Focus, Selection**](selection-and-focus-properties-and-methods.md), and [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)</span></span>

<span data-ttu-id="abc52-119">Les propriétés suivantes sont facultatives, mais fournissent des informations descriptives utiles sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="abc52-119">The following properties are optional, but provide useful descriptive information about the object.</span></span> <span data-ttu-id="abc52-120">La propriété [**Description**](description-property.md) est implémentée pour décrire des bitmaps et d’autres images.</span><span class="sxs-lookup"><span data-stu-id="abc52-120">The [**Description**](description-property.md) property is implemented to describe bitmaps and other images.</span></span>

-   [<span data-ttu-id="abc52-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="abc52-121">**Description**</span></span>](description-property.md)
-   <span data-ttu-id="abc52-122">[**Nœuds DefaultAction**](defaultaction-property.md) et [ **IAccessible :: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)</span><span class="sxs-lookup"><span data-stu-id="abc52-122">[**DefaultAction**](defaultaction-property.md) and [**IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)</span></span>
-   [<span data-ttu-id="abc52-123">**Aide**</span><span class="sxs-lookup"><span data-stu-id="abc52-123">**Help**</span></span>](help-property.md)
-   [<span data-ttu-id="abc52-124">**HelpTopic**</span><span class="sxs-lookup"><span data-stu-id="abc52-124">**HelpTopic**</span></span>](helptopic-property.md)

 

 




