---
title: accessibilité des contrôles ActiveX sans fenêtre
description: cette section décrit comment utiliser l’API d’accessibilité Windows pour s’assurer que les contrôles Microsoft ActiveX sans fenêtre sont accessibles.
ms.assetid: 93CBCF20-DADF-4A63-BE60-F2A0D8810C62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb0489cdd5de3ac34df361bfa3e7b3624ee18f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530201"
---
# <a name="windowless-activex-control-accessibility"></a>accessibilité des contrôles ActiveX sans fenêtre

cette section décrit comment utiliser l’API d’accessibilité Windows pour s’assurer que les contrôles Microsoft ActiveX sans fenêtre sont accessibles.

Windows 8 comprend de nouvelles interfaces API d’accessibilité Windows qui simplifient la tâche d’implémentation de l’accessibilité pour les contrôles ActiveX sans fenêtre. L’API comprend des interfaces qui sont implémentées sur un contrôle sans fenêtre et sur le conteneur de contrôle, ce qui permet au contrôle sans fenêtre et à son conteneur de travailler ensemble pour fournir des informations d’accessibilité sur le contrôle sans fenêtre. L’API prend en charge les scénarios suivants :

-   Microsoft Active Accessibility les contrôles sans fenêtre hébergés dans un conteneur de contrôle Microsoft Active Accessibility.
-   Microsoft Active Accessibility les contrôles sans fenêtre hébergés dans un conteneur de contrôle Microsoft UI Automation.
-   Contrôles sans fenêtre UI Automation hébergés dans un conteneur de contrôle Microsoft Active Accessibility.
-   Contrôles sans fenêtre UI Automation hébergés dans un conteneur de contrôle UI Automation.

le tableau suivant répertorie les interfaces qui prennent en charge les contrôles ActiveX sans fenêtre et identifie les objets qui implémentent les interfaces.



| Object              | MSAA                                                                             | UI Automation                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Objet de contrôle      | [**IAccessibleHandler**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| Site de contrôle        | [**IAccessibleWindowlessSite**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| Racine de la fenêtre hôte | [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a>Dans cette section

-   [comment utiliser UI Automation pour rendre un contrôle de ActiveX sans fenêtre Accessible](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [comment utiliser MSAA pour rendre un contrôle de ActiveX sans fenêtre Accessible](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [comment héberger un contrôle ActiveX sans fenêtre UI Automation](host-a-ui-automation-windowless-activex-control.md)
-   [comment héberger un contrôle de ActiveX sans fenêtre MSAA](host-an-msaa-windowless-activex-control.md)

 

 