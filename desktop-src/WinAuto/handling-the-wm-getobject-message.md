---
title: Gestion du message de WM_GETOBJECT
description: Microsoft Active Accessibility et Microsoft UI Automation envoient le \_ message WM GETOBJECT à une application serveur ou fournisseur pour extraire des informations sur un objet accessible pris en charge par le serveur ou le fournisseur.
ms.assetid: 4b8e551f-aba7-4a89-8874-ba690175f525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 695fad8f050606f0a95a1780551d35499e39d166
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403693"
---
# <a name="handling-the-wm_getobject-message"></a>Gestion du message WM de \_ GETOBJECT

Microsoft Active Accessibility et Microsoft UI Automation envoient le message [**WM \_ GETOBJECT**](wm-getobject.md) à une application serveur ou fournisseur pour extraire des informations sur un objet accessible pris en charge par le serveur ou le fournisseur. Les clients n’envoient jamais de **WM \_ GETOBJECT** directement. Au lieu de cela, Microsoft Active Accessibility envoie ce message lorsqu’un client appelle les fonctions [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)et [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) . UI Automation envoie **WM \_ GETOBJECT** lorsqu’un client appelle [**IUIAutomation :: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)et [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), et lors de la gestion des événements pour lesquels le client s’est inscrit.

Microsoft Active Accessibility ou UI Automation spécifie le type d’objet pour lequel il a besoin d’informations en passant une valeur appelée *identificateur d’objet* avec le message [**WM \_ GETOBJECT**](wm-getobject.md) . Lorsqu’il reçoit le message, le serveur ou le fournisseur examine l’identificateur d’objet pour déterminer comment répondre au message. La réponse varie selon que l’application réceptrice implémente Microsoft Active Accessibility (un serveur), UI Automation (fournisseur), ou aucun des autres, pour l’objet spécifié.

-   Si l’application réceptrice est un serveur Microsoft Active Accessibility et que le message [**WM \_ GETOBJECT**](wm-getobject.md) comprend un identificateur d’objet [**du \_ client objid**](object-identifiers.md), le serveur doit retourner la valeur obtenue en passant l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de l’objet à la fonction [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .
-   Si l’application réceptrice est fournisseur d’Automation aUI et que l’identificateur d’objet est **UiaRootObjectId**, le fournisseur doit retourner l’interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) de l’objet. Le fournisseur obtient l’interface en appelant la fonction [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .
-   Si l’application réceptrice n’implémente ni Microsoft Active Accessibility ni UI Automation, elle doit transmettre le message [**WM \_**](wm-getobject.md) à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Le passage du message permet à l’infrastructure d’accessibilité de déterminer si un proxy est disponible pour l’objet spécifié.
-   Si l’identificateur d’objet n’est ni [**objID \_ client**](object-identifiers.md) ni UiaRootObjectId, l’application de réception doit transmettre le message [**WM \_**](wm-getobject.md) de la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Le passage du message permet à l’infrastructure d’accessibilité d’utiliser les fournisseurs par défaut pour les éléments d’interface utilisateur standard.

Microsoft Active Accessibility et UI Automation peuvent transmettre des identificateurs d’objet personnalisés [**dans \_ un message WM**](wm-getobject.md) pour récupérer des valeurs ou des objets définis par l’application à partir d’un serveur ou d’un fournisseur. L’identificateur d’objet [**objID \_ NATIVEOM**](object-identifiers.md) ou [**objID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) peut être utilisé pour récupérer une interface de modèle objet natif, ou pour demander un objet proxy spécifique qui est pris en charge par Oleacc.dll.

En gérant à la fois les identificateurs d’objet [**\_ client objid**](object-identifiers.md) et **UiaRootObjectId** , une implémentation de serveur Microsoft Active Accessibility peut coexister avec une implémentation de fournisseur UI Automation. étant donné que la plupart des contrôles de Windows standard et des contrôles communs implémentés par la bibliothèque de contrôles communs (ComCtl32.dll) n’implémentent pas Microsoft Active Accessibility ou UI Automation, ces contrôles ne gèrent généralement pas le message [**WM de \_ GETOBJECT**](wm-getobject.md) . Au lieu de cela, l’infrastructure Microsoft Active Accessibility ou UI Automation vérifie si un objet proxy est disponible pour un élément d’interface utilisateur particulier. Dans le cas contraire, il fournit l’objet proxy par défaut pour l’objet de fenêtre hôte.

 

 