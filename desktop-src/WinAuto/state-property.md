---
title: Propriété State
description: La propriété State décrit l’état d’un objet à un moment donné. Tous les objets prennent en charge la propriété State.
ms.assetid: 6a56070f-7913-45b2-b693-3c0a8b7fa2f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151f09fca6c31abaaa98a19139d3e22eb28ec90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840745"
---
# <a name="state-property"></a><span data-ttu-id="f482c-104">Propriété State</span><span class="sxs-lookup"><span data-stu-id="f482c-104">State Property</span></span>

<span data-ttu-id="f482c-105">La propriété **State** décrit l’état d’un objet à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="f482c-105">The **State** property describes an object's status at a moment in time.</span></span> <span data-ttu-id="f482c-106">Tous les objets prennent en charge la propriété **State** .</span><span class="sxs-lookup"><span data-stu-id="f482c-106">All objects support the **State** property.</span></span>

<span data-ttu-id="f482c-107">La propriété **State** est récupérée en appelant [**IAccessible :: \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).</span><span class="sxs-lookup"><span data-stu-id="f482c-107">The **State** property is retrieved by calling [**IAccessible::get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).</span></span>

<span data-ttu-id="f482c-108">Microsoft Active Accessibility fournit des [constantes d’état d’objet](object-state-constants.md), définies dans oleacc. h, qui sont combinées pour identifier l’état d’un objet.</span><span class="sxs-lookup"><span data-stu-id="f482c-108">Microsoft Active Accessibility provides [object state constants](object-state-constants.md), defined in oleacc.h, that are combined to identify an object's state.</span></span> <span data-ttu-id="f482c-109">Il est recommandé que les développeurs de serveur utilisent ces valeurs d’État prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="f482c-109">It is recommended that server developers use these predefined state values.</span></span> <span data-ttu-id="f482c-110">Si des valeurs d’État prédéfinies sont retournées, les clients utilisent [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) pour récupérer une chaîne localisée qui décrit l’État.</span><span class="sxs-lookup"><span data-stu-id="f482c-110">If predefined state values are returned, clients use [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) to retrieve a localized string that describes the state.</span></span>

<span data-ttu-id="f482c-111">Les graphiques qui sont parfois animés doivent avoir la propriété **État** définie sur [**état \_ système \_ animé**](object-state-constants.md) et la propriété [**rôle**](role-property.md) définie sur [**\_ \_ graphique système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="f482c-111">Graphics that are occasionally animated should have the **State** property set to [**STATE\_SYSTEM\_ANIMATED**](object-state-constants.md) and the [**Role**](role-property.md) property set to [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

 

 




