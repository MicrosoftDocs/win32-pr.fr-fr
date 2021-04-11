---
title: Navigation hiérarchique
description: Les clients doivent souvent se déplacer entre des objets en fonction de leurs relations parent-enfant. Par exemple, un client a peut-être déjà des informations sur un contrôle de barre d’outils, mais pas d’informations sur les boutons qu’il contient.
ms.assetid: 7adf803c-140a-4f7d-8dc5-71abca706800
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c48ae366f2dd1caba4dfa6ff69aa1f57a23cbf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196753"
---
# <a name="hierarchical-navigation"></a><span data-ttu-id="422d5-104">Navigation hiérarchique</span><span class="sxs-lookup"><span data-stu-id="422d5-104">Hierarchical Navigation</span></span>

<span data-ttu-id="422d5-105">Les clients doivent souvent se déplacer entre des objets en fonction de leurs relations parent-enfant.</span><span class="sxs-lookup"><span data-stu-id="422d5-105">Often clients must move between objects based on their parent-child relationships.</span></span> <span data-ttu-id="422d5-106">Par exemple, un client a peut-être déjà des informations sur un contrôle de barre d’outils, mais pas d’informations sur les boutons qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="422d5-106">For example, a client might already have information about a toolbar control, but not have information about the buttons contained within it.</span></span>

<span data-ttu-id="422d5-107">L’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) expose les relations hiérarchiques entre les objets.</span><span class="sxs-lookup"><span data-stu-id="422d5-107">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface exposes the hierarchical relationships between objects.</span></span> <span data-ttu-id="422d5-108">Les clients peuvent naviguer d’un objet parent à ses enfants ou d’un objet enfant vers son parent en appelant [**IAccessible :: obtenir \_ AccParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) ou [**IAccessible :: obtenir \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild).</span><span class="sxs-lookup"><span data-stu-id="422d5-108">Clients can navigate from a parent object to its children or from a child object to its parent by calling [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) or [**IAccessible::get\_accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild).</span></span>

 

 




