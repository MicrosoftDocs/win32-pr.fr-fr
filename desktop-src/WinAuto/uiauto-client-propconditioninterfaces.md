---
title: Interfaces de condition de propriété pour les clients
description: Cette section décrit les interfaces de condition de propriété pour les clients UI Automation pour les applications Microsoft Win32.
ms.assetid: cea34e47-03a9-4ff9-9019-427a2a3e13d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f840706d4f9e340cae86813a4992400791dccd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031329"
---
# <a name="property-condition-interfaces-for-clients"></a><span data-ttu-id="38ea4-103">Interfaces de condition de propriété pour les clients</span><span class="sxs-lookup"><span data-stu-id="38ea4-103">Property Condition Interfaces for Clients</span></span>

<span data-ttu-id="38ea4-104">Cette section décrit les interfaces de condition de propriété pour les clients UI Automation pour les applications Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="38ea4-104">This section describes property condition interfaces for UI Automation clients for Microsoft Win32 applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="38ea4-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="38ea4-105">In this section</span></span>



| <span data-ttu-id="38ea4-106">Interface</span><span class="sxs-lookup"><span data-stu-id="38ea4-106">Interface</span></span>                                                                                  | <span data-ttu-id="38ea4-107">Description</span><span class="sxs-lookup"><span data-stu-id="38ea4-107">Description</span></span>                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38ea4-108">**IUIAutomationAndCondition**</span><span class="sxs-lookup"><span data-stu-id="38ea4-108">**IUIAutomationAndCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationandcondition)<br/>           | <span data-ttu-id="38ea4-109">Expose les propriétés et les méthodes que les applications clientes UI Automation de Microsoft peuvent utiliser pour récupérer des informations sur une condition de propriété basée sur et.</span><span class="sxs-lookup"><span data-stu-id="38ea4-109">Exposes properties and methods that Microsoft UI Automation client applications can use to retrieve information about an AND-based property condition.</span></span> <br/> |
| [<span data-ttu-id="38ea4-110">**IUIAutomationBoolCondition**</span><span class="sxs-lookup"><span data-stu-id="38ea4-110">**IUIAutomationBoolCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationboolcondition)<br/>         | <span data-ttu-id="38ea4-111">Représente une condition qui peut avoir la **valeur true** (sélectionne tous les éléments) ou **false** (ne sélectionne aucun élément).</span><span class="sxs-lookup"><span data-stu-id="38ea4-111">Represents a condition that can be either **TRUE** (selects all elements) or **FALSE** (selects no elements).</span></span><br/>                                           |
| [<span data-ttu-id="38ea4-112">**IUIAutomationCondition**</span><span class="sxs-lookup"><span data-stu-id="38ea4-112">**IUIAutomationCondition**</span></span>](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)<br/>                 | <span data-ttu-id="38ea4-113">Il s’agit de l’interface principale pour les conditions utilisées dans le filtrage lors de la recherche d’éléments dans l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="38ea4-113">This is the primary interface for conditions used in filtering when searching for elements in the UI Automation tree.</span></span><br/>                                   |
| [<span data-ttu-id="38ea4-114">**IUIAutomationNotCondition**</span><span class="sxs-lookup"><span data-stu-id="38ea4-114">**IUIAutomationNotCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotcondition)<br/>           | <span data-ttu-id="38ea4-115">Représente une condition qui est la valeur négative d’une autre condition.</span><span class="sxs-lookup"><span data-stu-id="38ea4-115">Represents a condition that is the negative of another condition.</span></span><br/>                                                                                       |
| [<span data-ttu-id="38ea4-116">**IUIAutomationOrCondition**</span><span class="sxs-lookup"><span data-stu-id="38ea4-116">**IUIAutomationOrCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationorcondition)<br/>             | <span data-ttu-id="38ea4-117">Représente une condition composée de plusieurs conditions, au moins l’une d’entre elles devant avoir la valeur true.</span><span class="sxs-lookup"><span data-stu-id="38ea4-117">Represents a condition made up of multiple conditions, at least one of which must be true.</span></span><br/>                                                              |
| [<span data-ttu-id="38ea4-118">**IUIAutomationPropertyCondition**</span><span class="sxs-lookup"><span data-stu-id="38ea4-118">**IUIAutomationPropertyCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition)<br/> | <span data-ttu-id="38ea4-119">Représente une condition basée sur une valeur de propriété utilisée pour rechercher des éléments UI Automation.</span><span class="sxs-lookup"><span data-stu-id="38ea4-119">Represents a condition based on a property value that is used to find UI Automation elements.</span></span><br/>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="38ea4-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="38ea4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38ea4-121">Clients UI Automation</span><span class="sxs-lookup"><span data-stu-id="38ea4-121">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

