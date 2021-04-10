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
# <a name="proxy-factory-interfaces-for-clients"></a><span data-ttu-id="9ccd3-103">Interfaces de fabrique proxy pour les clients</span><span class="sxs-lookup"><span data-stu-id="9ccd3-103">Proxy Factory Interfaces for Clients</span></span>

<span data-ttu-id="9ccd3-104">Cette section décrit les interfaces de fabrique proxy pour les applications clientes UI Automation non managées.</span><span class="sxs-lookup"><span data-stu-id="9ccd3-104">This section describes the proxy factory interfaces for unmanaged UI Automation client applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9ccd3-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="9ccd3-105">In this section</span></span>



| <span data-ttu-id="9ccd3-106">Interface</span><span class="sxs-lookup"><span data-stu-id="9ccd3-106">Interface</span></span>                                                                                      | <span data-ttu-id="9ccd3-107">Description</span><span class="sxs-lookup"><span data-stu-id="9ccd3-107">Description</span></span>                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ccd3-108">**IUIAutomationProxyFactory**</span><span class="sxs-lookup"><span data-stu-id="9ccd3-108">**IUIAutomationProxyFactory**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>               | <span data-ttu-id="9ccd3-109">Expose les propriétés et les méthodes d’un objet qui crée un fournisseur Microsoft UI Automation pour les éléments d’interface utilisateur qui n’ont pas de prise en charge native pour UI Automation.</span><span class="sxs-lookup"><span data-stu-id="9ccd3-109">Exposes properties and methods of an object that creates a Microsoft UI Automation provider for UI elements that do not have native support for UI Automation.</span></span> <span data-ttu-id="9ccd3-110">Cette interface est implémentée par les proxys.</span><span class="sxs-lookup"><span data-stu-id="9ccd3-110">This interface is implemented by proxies.</span></span><br/>                                                                          |
| [<span data-ttu-id="9ccd3-111">**IUIAutomationProxyFactoryEntry**</span><span class="sxs-lookup"><span data-stu-id="9ccd3-111">**IUIAutomationProxyFactoryEntry**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry)<br/>     | <span data-ttu-id="9ccd3-112">Représente une fabrique de proxy dans la table gérée par UI Automation et expose des propriétés et des méthodes qui peuvent être utilisées par les applications clientes pour interagir avec les objets [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) .</span><span class="sxs-lookup"><span data-stu-id="9ccd3-112">Represents a proxy factory in the table maintained by UI Automation, and exposes properties and methods that can be used by client applications to interact with [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) objects.</span></span><br/>                                   |
| [<span data-ttu-id="9ccd3-113">**IUIAutomationProxyFactoryMapping**</span><span class="sxs-lookup"><span data-stu-id="9ccd3-113">**IUIAutomationProxyFactoryMapping**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping)<br/> | <span data-ttu-id="9ccd3-114">Expose les propriétés et les méthodes pour une table de fabriques de proxy.</span><span class="sxs-lookup"><span data-stu-id="9ccd3-114">Exposes properties and methods for a table of proxy factories.</span></span> <span data-ttu-id="9ccd3-115">Chaque entrée de table est représentée par une interface [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) .</span><span class="sxs-lookup"><span data-stu-id="9ccd3-115">Each table entry is represented by an [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) interface.</span></span> <span data-ttu-id="9ccd3-116">Les entrées s’affichent dans l’ordre dans lequel le système tentera d’utiliser les proxys.</span><span class="sxs-lookup"><span data-stu-id="9ccd3-116">The entries are in the order in which the system will attempt to use the proxies.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="9ccd3-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9ccd3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ccd3-118">Clients UI Automation</span><span class="sxs-lookup"><span data-stu-id="9ccd3-118">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





