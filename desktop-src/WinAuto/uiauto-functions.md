---
title: Fonctions pour les fournisseurs
description: Cette section décrit les fonctions du fournisseur UI Automation pour les applications Microsoft Win32.
ms.assetid: 76012ec7-0114-4b6b-a35e-5cfde5b90230
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0542c3d0b313e1bed8ec040924349e37a29fea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010524"
---
# <a name="functions-for-providers"></a>Fonctions pour les fournisseurs

Cette section décrit les fonctions du fournisseur UI Automation pour les applications Microsoft Win32.

## <a name="in-this-section"></a>Dans cette section



| Fonction                                                                                                 | Description                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UiaClientsAreListening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening)<br/>                       | Obtient une valeur qui indique si une application cliente est abonnée à des événements Microsoft UI Automation.<br/>                                             |
| [**UiaDisconnectAllProviders**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectallproviders)<br/>                         | Libère toutes les ressources UI Automation détenues par tous les fournisseurs associés au processus appelant. <br/>                                               |
| [**UiaDisconnectProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectprovider)<br/>                                 | Libère toutes les références qu’un fournisseur particulier contient aux objets UI Automation.<br/>                                                                      |
| [**UiaGetReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue)<br/> | Récupère une valeur réservée indiquant que la valeur d’un attribut de texte UI Automation varie dans une plage de texte.<br/>                                      |
| [**UiaGetReservedNotSupportedValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue)<br/>     | Récupère une valeur réservée indiquant qu’une propriété UI Automation ou un attribut de texte n’est pas pris en charge.<br/>                                               |
| [**UiaHostProviderFromHwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd)<br/>                     | Obtient le fournisseur hôte pour une fenêtre.<br/>                                                                                                                    |
| [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider)<br/>                   | Récupère une implémentation [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) qui fournit des données Microsoft Active Accessibility pour le compte d’un fournisseur UI Automation.<br/> |
| [**UiaProviderForNonClient**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfornonclient)<br/>                     | Obtient le fournisseur pour l’ensemble de la zone non cliente d’une fenêtre ou pour un contrôle dans la zone non cliente d’une fenêtre.<br/>                                      |
| [**UiaProviderFromIAccessible**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible)<br/>               | Crée un fournisseur UI Automation basé sur l’objet Microsoft Active Accessibility spécifié.<br/>                                                          |
| [**UiaRaiseAsyncContentLoadedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseasynccontentloadedevent)<br/>     | Appelé par un fournisseur pour notifier au noyau UI Automation le chargement asynchrone du contenu.<br/>                                                      |
| [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent)<br/>                     | Notifie les écouteurs d’un événement.<br/>                                                                                                                         |
| [**UiaRaiseAutomationPropertyChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationpropertychangedevent)<br/>    | Appelé par les fournisseurs pour notifier au noyau UI Automation qu’une propriété d’élément a changé.<br/>                                                              |
| [**UiaRaiseChangesEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisechangesevent)<br/>                           | Appelé par les fournisseurs pour notifier au noyau UI Automation qu’une modification s’est produite.<br/>                                                                        |
| [**UiaRaiseNotificationEvent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**)<br/>             | Appelé par les fournisseurs pour initier un événement de notification.<br/>                                                                                                   |
| [**UiaRaiseStructureChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisestructurechangedevent)<br/>         | Appelé par un fournisseur pour notifier au noyau UI Automation que l’arborescence a changé.<br/>                                                              |
| [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent)<br/>   | Appelé par un fournisseur pour notifier au noyau UI Automation qu’un contrôle de texte a changé de texte par programmation.<br/>                                            |
| [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider)<br/>             | Obtient une interface au fournisseur UI Automation pour une fenêtre.<br/>                                                                                           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fournisseurs UI Automation](uiauto-entry-uiautoprovidersforwin32apps.md)
</dt> </dl>

 

