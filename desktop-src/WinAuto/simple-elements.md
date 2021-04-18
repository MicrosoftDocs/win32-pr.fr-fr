---
title: Éléments simples
description: Un élément simple est un élément d’interface utilisateur qui partage un objet IAccessible avec d’autres éléments et s’appuie sur cet objet IAccessible (généralement son parent) pour exposer ses propriétés.
ms.assetid: 3f6bd992-4e0a-4dba-b6e9-e70dca77c880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f8cb00b19719a4a8779a61f37b079633ada40c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509409"
---
# <a name="simple-elements"></a><span data-ttu-id="98e17-103">Éléments simples</span><span class="sxs-lookup"><span data-stu-id="98e17-103">Simple Elements</span></span>

<span data-ttu-id="98e17-104">Un *élément simple* est un élément d’interface utilisateur qui partage un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) avec d’autres éléments et s’appuie sur cet objet **IAccessible** (généralement son parent) pour exposer ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="98e17-104">A *simple element* is a UI element that shares an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object with other elements and relies on that **IAccessible** object (typically its parent) to expose its properties.</span></span> <span data-ttu-id="98e17-105">Pour faire la différence entre les éléments qui partagent un objet **IAccessible** , le serveur affecte un identificateur enfant positif unique à chaque élément simple.</span><span class="sxs-lookup"><span data-stu-id="98e17-105">To differentiate between the elements sharing an **IAccessible** object, the server assigns a unique, positive child identifier to each simple element.</span></span> <span data-ttu-id="98e17-106">Cette affectation est effectuée par instance d’interface, de sorte que les ID doivent être uniques dans ce contexte.</span><span class="sxs-lookup"><span data-stu-id="98e17-106">This assignment is done on a per-instance-of-interface basis, so the IDs must be unique within that context.</span></span> <span data-ttu-id="98e17-107">De nombreuses implémentations assignent ces ID de manière séquentielle, en commençant par 1.</span><span class="sxs-lookup"><span data-stu-id="98e17-107">Many implementations assign these IDs sequentially, beginning with 1.</span></span> <span data-ttu-id="98e17-108">Ce schéma n’autorise pas les éléments simples à avoir leurs propres enfants.</span><span class="sxs-lookup"><span data-stu-id="98e17-108">This scheme does not allow simple elements to have children of their own.</span></span> <span data-ttu-id="98e17-109">Les éléments simples sont également appelés *enfants*.</span><span class="sxs-lookup"><span data-stu-id="98e17-109">Simple elements are also known as *children*.</span></span>

<span data-ttu-id="98e17-110">Pour être identifié et exposé de manière unique, un élément simple requiert un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) et un ID enfant.</span><span class="sxs-lookup"><span data-stu-id="98e17-110">To be uniquely identified and exposed, a simple element requires an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object and child ID.</span></span> <span data-ttu-id="98e17-111">Par conséquent, lors de la communication avec un objet **IAccessible** , les clients doivent fournir l’ID enfant approprié.</span><span class="sxs-lookup"><span data-stu-id="98e17-111">Therefore, when communicating with an **IAccessible** object, the clients must supply the appropriate child ID.</span></span> <span data-ttu-id="98e17-112">Un identificateur spécial, **CHILDID \_ Self**, peut être utilisé pour faire référence à l’objet accessible lui-même, au lieu de l’un de ses enfants.</span><span class="sxs-lookup"><span data-stu-id="98e17-112">A special identifier, **CHILDID\_SELF**, can be used to refer to the accessible object itself, instead of one of its children.</span></span>

<span data-ttu-id="98e17-113">L’objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) partagé entre les éléments simples correspond souvent à un objet parent commun dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="98e17-113">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object shared among simple elements often corresponds to a common parent object in the user interface.</span></span> <span data-ttu-id="98e17-114">Par exemple, les zones de liste système exposent un objet accessible pour la zone de liste globale et des éléments simples pour chaque élément de zone de liste.</span><span class="sxs-lookup"><span data-stu-id="98e17-114">For example, system list boxes expose an accessible object for the overall list box and simple elements for each list box item.</span></span> <span data-ttu-id="98e17-115">Dans ce cas, l’objet **IAccessible** pour la zone de liste est également le parent ou le conteneur des éléments de liste.</span><span class="sxs-lookup"><span data-stu-id="98e17-115">In this case, the **IAccessible** object for the list box is also the parent or container of the list items.</span></span>

<span data-ttu-id="98e17-116">Pour plus d’informations sur les objets accessibles, consultez [objets accessibles](accessible-objects.md).</span><span class="sxs-lookup"><span data-stu-id="98e17-116">For more information about accessible objects, see [Accessible Objects](accessible-objects.md).</span></span>

 

 




