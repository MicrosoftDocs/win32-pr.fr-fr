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
# <a name="accessing-microsoft-active-accessibility-servers"></a>Accès aux serveurs Microsoft Active Accessibility

Le proxy Microsoft Active Accessibility vers UI Automation est un composant logiciel qui permet aux clients Microsoft UI Automation d’interagir avec les serveurs Microsoft Active Accessibility qui implémentent l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en mode natif. Le proxy prend en charge le modèle de contrôle [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) et fournit une instance de l’interface [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) pour chaque serveur Microsoft Active Accessibility détecté. Les clients UI Automation utilisent les méthodes exposées par **IUIAutomationLegacyIAccessiblePattern** pour accéder aux propriétés et objets Microsoft Active Accessibility pris en charge par le serveur.

Si un élément UI Automation a une implémentation sous-jacente de Microsoft Active Accessibility, un client peut obtenir un pointeur d’interface [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) pour l’élément en passant l’ID du modèle de contrôle [**UIA \_ LegacyIAccessiblePatternId**](uiauto-controlpattern-ids.md) à l’une des méthodes [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) suivantes :

-   [**GetCachedPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)
-   [**GetCachedPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas)
-   [**GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)
-   [**GetCurrentPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas)

L’interface [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) n’est pas disponible pour les contrôles basés sur UI Automation.

L’interface [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) permet aux clients UI Automation d’accéder à l’implémentation [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sous-jacente d’un élément Microsoft Active Accessibility. Toutefois, l’interface ne prend pas en charge les méthodes obsolètes ou redondantes avec les fonctionnalités UI Automation. Par exemple, **IUIAutomationLegacyIAccessiblePattern** n’a pas de méthode équivalente à [**IAccessible :: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) , car l’emplacement actuel d’un élément d’interface utilisateur est disponible à partir de la propriété UI Automation BoundingRectangle.

La méthode [**IUIAutomationLegacyIAccessiblePattern :: GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) permet à un client de récupérer un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) à partir d’un élément UI Automation. L’inverse est également possible à l’aide des méthodes [**IUIAutomation :: ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) et [**IUIAutomation :: ElementFromIAccessibleBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) .

[**IUIAutomationLegacyIAccessiblePattern :: GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) retourne la **valeur null** si l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour l’élément est fournie par un objet proxy à partir de OLEACC.dll ou du pont UI Automation au pont Microsoft Active Accessibility.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[UI Automation et Active Accessibility](uiauto-msaa.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




