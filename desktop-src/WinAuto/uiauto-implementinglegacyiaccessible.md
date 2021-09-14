---
title: Modèle de contrôle LegacyIAccessible
description: Fournit des instructions et des conventions pour l’utilisation de ILegacyIAccessibleProvider, notamment des informations sur les propriétés, les méthodes et les événements.
ms.assetid: 4d66b9b8-ddbe-4bbc-b475-72dad1fe9393
keywords:
- UI Automation, implémentation du modèle de contrôle LegacyIAccessible
- UI Automation, modèle de contrôle LegacyIAccessible
- UI Automation, ILegacyIAccessibleProvider
- ILegacyIAccessibleProvider
- implémentation des modèles de contrôle LegacyIAccessible d’UI Automation
- Modèles de contrôle LegacyIAccessible
- modèles de contrôle, ILegacyIAccessibleProvider
- modèles de contrôle, implémenter des LegacyIAccessible UI Automation
- modèles de contrôle, LegacyIAccessible
- interfaces, ILegacyIAccessibleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cffbd205b072f6f900ea5b5eb5a9f6ddfb5ddc5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010494"
---
# <a name="legacyiaccessible-control-pattern"></a>Modèle de contrôle LegacyIAccessible

Fournit des instructions et des conventions pour l’utilisation de [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider), notamment des informations sur les propriétés, les méthodes et les événements. Le modèle de contrôle **LegacyIAccessible** est pris en charge par Microsoft Active Accessibility au proxy Microsoft UI Automation.

Les fournisseurs d’applications et de contrôles n’implémentent jamais l’interface [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider) .

Le modèle de contrôle **LegacyIAccessible** expose l’interface [**IUIAUTOMATIONLEGACYIACCESSIBLEPATTERN**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) aux clients UI Automation, ce qui leur permet d’accéder à l’implémentation [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sous-jacente de certains éléments d’interface utilisateur. Toutefois, **IUIAutomationLegacyIAccessiblePattern** ne prend pas en charge les méthodes obsolètes ou redondantes avec les fonctionnalités d’UI Automation.

Cette rubrique contient les sections suivantes :

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres du modèle de contrôle **LegacyIAccessible**](#members-of-the-legacyiaccessible-control-pattern)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Aucune application ou aucun contrôle n’implémente [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider). L’infrastructure UI Automation fournit automatiquement l’implémentation du fournisseur pour un serveur Microsoft Active Accessibility natif.

Le modèle de contrôle **LegacyIAccessible** n’est pas disponible pour les contrôles basés sur UI Automation.

## <a name="members-of-the-legacyiaccessible-control-pattern"></a>Membres du modèle de contrôle **LegacyIAccessible**

Les propriétés, méthodes et événements suivants sont des membres du modèle de contrôle **LegacyIAccessible** . Les notes sont destinées aux clients UI Automation.



| Membres                                                                        | Type de membre | Notes                                                                                                                                |
|--------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**ChildId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_childid)                   | Propriété    | Retourne **CHILDID \_ Self** (0) pour un objet non enfant.                                                                                |
| [**Nœud**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_defaultaction)       | Propriété    | None                                                                                                                                 |
| [**Description**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_description)           | Propriété    | None                                                                                                                                 |
| [**Aide**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_help)                         | Propriété    | None                                                                                                                                 |
| [**KeyboardShortcut**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_keyboardshortcut) | Propriété    | None                                                                                                                                 |
| [**Nomme**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_name)                         | Propriété    | None                                                                                                                                 |
| [**Rôle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_role)                         | Propriété    | Utilisez la fonction [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) pour récupérer une chaîne localisée.                                                    |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getselection)         | Méthode      | Récupère un pointeur d’interface [**IUIAutomationElementArray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray) .                                |
| [**État**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_state)                       | Propriété    | Utilisez la fonction [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) pour récupérer une chaîne localisée.                                                  |
| [**Valeur**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_value)                       | Propriété    | None                                                                                                                                 |
| [**DoDefaultAction**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-dodefaultaction)   | Méthode      | None                                                                                                                                 |
| [**GetIAccessible**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getiaccessible)     | Méthode      | None                                                                                                                                 |
| [**Sélectionner**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-select)                     | Méthode      | L’indicateur de sélection est une valeur Microsoft Active Accessibility **SELFLAG** . Pour plus d’informations, consultez [constantes SELFLAG](selflag.md). |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-setvalue)                 | Méthode      | None                                                                                                                                 |



 

Ce modèle de contrôle n’est associé aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




