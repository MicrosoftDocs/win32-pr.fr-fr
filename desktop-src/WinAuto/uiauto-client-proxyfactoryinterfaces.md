---
title: Interfaces de fabrique proxy pour les clients
description: Cette section décrit les interfaces de fabrique proxy pour les applications clientes UI Automation non managées.
ms.assetid: 46c6720a-19c2-4ddd-893c-1a46af0642fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc1827ab36a221dcd7f27e5b2a05de91931b0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029706"
---
# <a name="proxy-factory-interfaces-for-clients"></a>Interfaces de fabrique proxy pour les clients

Cette section décrit les interfaces de fabrique proxy pour les applications clientes UI Automation non managées.

## <a name="in-this-section"></a>Dans cette section



| Interface                                                                                      | Description                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>               | Expose les propriétés et les méthodes d’un objet qui crée un fournisseur Microsoft UI Automation pour les éléments d’interface utilisateur qui n’ont pas de prise en charge native pour UI Automation. Cette interface est implémentée par les proxys.<br/>                                                                          |
| [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry)<br/>     | Représente une fabrique de proxy dans la table gérée par UI Automation et expose des propriétés et des méthodes qui peuvent être utilisées par les applications clientes pour interagir avec les objets [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) .<br/>                                   |
| [**IUIAutomationProxyFactoryMapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping)<br/> | Expose les propriétés et les méthodes pour une table de fabriques de proxy. Chaque entrée de table est représentée par une interface [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) . Les entrées s’affichent dans l’ordre dans lequel le système tentera d’utiliser les proxys.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Clients UI Automation](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





