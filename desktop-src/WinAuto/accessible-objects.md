---
title: Objets accessibles
description: Avec Microsoft Active Accessibility, les éléments d’interface utilisateur sont exposés aux clients sous la forme d’objets COM (Component Object Model).
ms.assetid: ab5669c3-33ce-4d56-a028-e36db25c0b28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba496e011d42fac9a3c4b047a7d8c3b9e0ecf84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380358"
---
# <a name="accessible-objects"></a><span data-ttu-id="098ab-103">Objets accessibles</span><span class="sxs-lookup"><span data-stu-id="098ab-103">Accessible Objects</span></span>

<span data-ttu-id="098ab-104">Avec Microsoft Active Accessibility, les éléments d’interface utilisateur sont exposés aux clients sous la forme d’objets COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="098ab-104">With Microsoft Active Accessibility, UI elements are exposed to clients as Component Object Model (COM) objects.</span></span> <span data-ttu-id="098ab-105">Ces *objets accessibles* maintiennent des informations, appelées *Propriétés*, qui décrivent le nom de l’objet, l’emplacement de l’écran et d’autres informations requises par les aides à l’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="098ab-105">These *accessible objects* maintain pieces of information, called *properties*, which describe the object's name, screen location, and other information needed by accessibility aids.</span></span> <span data-ttu-id="098ab-106">Les objets accessibles fournissent également des *méthodes* que les clients appellent pour faire en sorte que l’objet effectue une action.</span><span class="sxs-lookup"><span data-stu-id="098ab-106">Accessible objects also provide *methods* that clients call to cause the object to perform some action.</span></span> <span data-ttu-id="098ab-107">Les objets accessibles qui ont des éléments simples qui leur sont associés sont également appelés *parents*, ou *conteneurs*.</span><span class="sxs-lookup"><span data-stu-id="098ab-107">Accessible objects that have simple elements associated with them are also called *parents*, or *containers*.</span></span>

<span data-ttu-id="098ab-108">Les objets accessibles sont implémentés à l’aide de l’interface [**IACCESSIBLE**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) com de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="098ab-108">Accessible objects are implemented using Microsoft Active Accessibility's COM-based [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="098ab-109">Les méthodes et propriétés **IAccessible** permettent aux applications clientes d’obtenir des informations sur les éléments d’interface utilisateur requis par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="098ab-109">The **IAccessible** methods and properties enable client applications to get information about UI elements needed by users.</span></span> <span data-ttu-id="098ab-110">Par exemple, [**IAccessible :: obtenir \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) retourne un pointeur d’interface vers le parent d’un objet accessible, et [**IAccessible :: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) permet aux clients d’obtenir des informations sur d’autres objets au sein d’un conteneur.</span><span class="sxs-lookup"><span data-stu-id="098ab-110">For example, [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) returns an interface pointer to an accessible object's parent, and [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) provides a means for clients to get information about other objects within a container.</span></span>

<span data-ttu-id="098ab-111">Pour plus d’informations sur la façon dont les objets accessibles et les éléments simples sont liés, consultez [éléments simples](simple-elements.md).</span><span class="sxs-lookup"><span data-stu-id="098ab-111">For more information about how accessible objects and simple elements are related, see [Simple Elements](simple-elements.md).</span></span>

 

 




