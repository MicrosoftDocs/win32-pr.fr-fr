---
title: Accès aux serveurs Microsoft Active Accessibility
description: Le proxy Microsoft Active Accessibility vers UI Automation est un composant logiciel qui permet aux clients Microsoft UI Automation d’interagir avec les serveurs Microsoft Active Accessibility qui implémentent l’interface IAccessible en mode natif.
ms.assetid: 44690b16-4a9d-4e8b-865a-b428ad616b1e
keywords:
- UI Automation, accès Active Accessibility
- UI Automation, Active Accessibility
- Proxy UI Automation
- UI Automation, proxy UI Automation
- Modèle de contrôle LegacyIAccessible
- UI Automation, modèle de contrôle LegacyIAccessible
- Microsoft Active Accessibility
- Active Accessibility
- clients, accès aux serveurs de Active Accessibility
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97319028203351cd9f45b39d133fa38727d6861e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028909"
---
# <a name="accessing-microsoft-active-accessibility-servers"></a><span data-ttu-id="dc5af-112">Accès aux serveurs Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="dc5af-112">Accessing Microsoft Active Accessibility Servers</span></span>

<span data-ttu-id="dc5af-113">Le proxy Microsoft Active Accessibility vers UI Automation est un composant logiciel qui permet aux clients Microsoft UI Automation d’interagir avec les serveurs Microsoft Active Accessibility qui implémentent l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en mode natif.</span><span class="sxs-lookup"><span data-stu-id="dc5af-113">The Microsoft Active Accessibility to UI Automation Proxy is a software component that enables Microsoft UI Automation clients to interact with Microsoft Active Accessibility servers that implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface natively.</span></span> <span data-ttu-id="dc5af-114">Le proxy prend en charge le modèle de contrôle [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) et fournit une instance de l’interface [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) pour chaque serveur Microsoft Active Accessibility détecté.</span><span class="sxs-lookup"><span data-stu-id="dc5af-114">The proxy supports the [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) control pattern, and supplies an instance of the [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface for each Microsoft Active Accessibility server detected.</span></span> <span data-ttu-id="dc5af-115">Les clients UI Automation utilisent les méthodes exposées par **IUIAutomationLegacyIAccessiblePattern** pour accéder aux propriétés et objets Microsoft Active Accessibility pris en charge par le serveur.</span><span class="sxs-lookup"><span data-stu-id="dc5af-115">UI Automation clients use the methods exposed by **IUIAutomationLegacyIAccessiblePattern** to access the Microsoft Active Accessibility properties and objects supported by the server.</span></span>

<span data-ttu-id="dc5af-116">Si un élément UI Automation a une implémentation sous-jacente de Microsoft Active Accessibility, un client peut obtenir un pointeur d’interface [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) pour l’élément en passant l’ID du modèle de contrôle [**UIA \_ LegacyIAccessiblePatternId**](uiauto-controlpattern-ids.md) à l’une des méthodes [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) suivantes :</span><span class="sxs-lookup"><span data-stu-id="dc5af-116">If a UI Automation element has an underlying Microsoft Active Accessibility implementation, a client can obtain an [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface pointer for the element by passing the [**UIA\_LegacyIAccessiblePatternId**](uiauto-controlpattern-ids.md) control pattern ID to one of the following [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) methods:</span></span>

-   [<span data-ttu-id="dc5af-117">**GetCachedPattern**</span><span class="sxs-lookup"><span data-stu-id="dc5af-117">**GetCachedPattern**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)
-   [<span data-ttu-id="dc5af-118">**GetCachedPatternAs**</span><span class="sxs-lookup"><span data-stu-id="dc5af-118">**GetCachedPatternAs**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas)
-   [<span data-ttu-id="dc5af-119">**GetCurrentPattern**</span><span class="sxs-lookup"><span data-stu-id="dc5af-119">**GetCurrentPattern**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)
-   [<span data-ttu-id="dc5af-120">**GetCurrentPatternAs**</span><span class="sxs-lookup"><span data-stu-id="dc5af-120">**GetCurrentPatternAs**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas)

<span data-ttu-id="dc5af-121">L’interface [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) n’est pas disponible pour les contrôles basés sur UI Automation.</span><span class="sxs-lookup"><span data-stu-id="dc5af-121">The [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface is not available for controls based on UI Automation.</span></span>

<span data-ttu-id="dc5af-122">L’interface [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) permet aux clients UI Automation d’accéder à l’implémentation [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sous-jacente d’un élément Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="dc5af-122">The [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface enables UI Automation clients to access the underlying [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation of an Microsoft Active Accessibility element.</span></span> <span data-ttu-id="dc5af-123">Toutefois, l’interface ne prend pas en charge les méthodes obsolètes ou redondantes avec les fonctionnalités UI Automation.</span><span class="sxs-lookup"><span data-stu-id="dc5af-123">However, the interface does not support methods that are obsolete or redundant with UI Automation features.</span></span> <span data-ttu-id="dc5af-124">Par exemple, **IUIAutomationLegacyIAccessiblePattern** n’a pas de méthode équivalente à [**IAccessible :: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) , car l’emplacement actuel d’un élément d’interface utilisateur est disponible à partir de la propriété UI Automation BoundingRectangle.</span><span class="sxs-lookup"><span data-stu-id="dc5af-124">For example, **IUIAutomationLegacyIAccessiblePattern** does not have a method that is equivalent to [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) because the current location of a UI element is available from the UI Automation BoundingRectangle property.</span></span>

<span data-ttu-id="dc5af-125">La méthode [**IUIAutomationLegacyIAccessiblePattern :: GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) permet à un client de récupérer un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) à partir d’un élément UI Automation.</span><span class="sxs-lookup"><span data-stu-id="dc5af-125">The [**IUIAutomationLegacyIAccessiblePattern::GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) method enables a client to retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer from an UI Automation element.</span></span> <span data-ttu-id="dc5af-126">L’inverse est également possible à l’aide des méthodes [**IUIAutomation :: ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) et [**IUIAutomation :: ElementFromIAccessibleBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) .</span><span class="sxs-lookup"><span data-stu-id="dc5af-126">The reverse is also possible by using the [**IUIAutomation::ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) and [**IUIAutomation::ElementFromIAccessibleBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) methods.</span></span>

<span data-ttu-id="dc5af-127">[**IUIAutomationLegacyIAccessiblePattern :: GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) retourne la **valeur null** si l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour l’élément est fournie par un objet proxy à partir de OLEACC.dll ou du pont UI Automation au pont Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="dc5af-127">[**IUIAutomationLegacyIAccessiblePattern::GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) returns **NULL** if the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for the element is provided by a proxy object from OLEACC.dll or from the UI Automation to Microsoft Active Accessibility Bridge.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc5af-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dc5af-128">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="dc5af-129">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="dc5af-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dc5af-130">UI Automation et Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="dc5af-130">UI Automation and Active Accessibility</span></span>](uiauto-msaa.md)
</dt> <dt>

[<span data-ttu-id="dc5af-131">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="dc5af-131">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




