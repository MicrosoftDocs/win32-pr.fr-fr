---
title: Structures UI Automation
description: Cette section décrit les structures utilisées par les applications clientes UI Automation et le fournisseur UI Automation pour Microsoft Win32.
ms.assetid: 37d6a7c0-6925-443b-aa21-da2a14a9ddad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55ddf9086f0714665c944a5a80e53e63eb3a91a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462102"
---
# <a name="ui-automation-structures"></a><span data-ttu-id="21a99-103">Structures UI Automation</span><span class="sxs-lookup"><span data-stu-id="21a99-103">UI Automation Structures</span></span>

<span data-ttu-id="21a99-104">Cette section décrit les structures utilisées par les applications clientes UI Automation et le fournisseur UI Automation pour Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="21a99-104">This section describes the structures used by UI Automation client applications and UI Automation provider for Microsoft Win32.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="21a99-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="21a99-105">In this section</span></span>



| <span data-ttu-id="21a99-106">Structure</span><span class="sxs-lookup"><span data-stu-id="21a99-106">Structure</span></span>                                                                            | <span data-ttu-id="21a99-107">Description</span><span class="sxs-lookup"><span data-stu-id="21a99-107">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21a99-108">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="21a99-108">**ExtendedProperty**</span></span>](/windows/desktop/api/UIAutomationClient/ns-uiautomationclient-extendedproperty)<br/>                       | <span data-ttu-id="21a99-109">Contient des informations sur une propriété étendue.</span><span class="sxs-lookup"><span data-stu-id="21a99-109">Contains information about an extended property.</span></span> <br/>                                  |
| [<span data-ttu-id="21a99-110">**UIAutomationEventInfo**</span><span class="sxs-lookup"><span data-stu-id="21a99-110">**UIAutomationEventInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo)<br/>       | <span data-ttu-id="21a99-111">Contient des informations sur un événement personnalisé.</span><span class="sxs-lookup"><span data-stu-id="21a99-111">Contains information about a custom event.</span></span><br/>                                         |
| [<span data-ttu-id="21a99-112">**UIAutomationMethodInfo**</span><span class="sxs-lookup"><span data-stu-id="21a99-112">**UIAutomationMethodInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo)<br/>     | <span data-ttu-id="21a99-113">Contient des informations sur une méthode prise en charge par un modèle de contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="21a99-113">Contains information about a method that is supported by a custom control pattern.</span></span><br/> |
| [<span data-ttu-id="21a99-114">**UIAutomationParameter**</span><span class="sxs-lookup"><span data-stu-id="21a99-114">**UIAutomationParameter**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter)<br/>       | <span data-ttu-id="21a99-115">Contient des informations sur un paramètre d’un modèle de contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="21a99-115">Contains information about a parameter of a custom control pattern.</span></span><br/>                |
| [<span data-ttu-id="21a99-116">**UIAutomationPatternInfo**</span><span class="sxs-lookup"><span data-stu-id="21a99-116">**UIAutomationPatternInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo)<br/>   | <span data-ttu-id="21a99-117">Contient des informations sur un modèle de contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="21a99-117">Contains information about a custom control pattern.</span></span><br/>                               |
| [<span data-ttu-id="21a99-118">**UIAutomationPropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="21a99-118">**UIAutomationPropertyInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo)<br/> | <span data-ttu-id="21a99-119">Contient des informations sur une propriété personnalisée.</span><span class="sxs-lookup"><span data-stu-id="21a99-119">Contains information about a custom property.</span></span><br/>                                      |
| [<span data-ttu-id="21a99-120">**UiaChangeInfo**</span><span class="sxs-lookup"><span data-stu-id="21a99-120">**UiaChangeInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiachangeinfo)<br/>                                    | <span data-ttu-id="21a99-121">Contient des données relatives à une modification d’UI Automation qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="21a99-121">Contains data about a UI Automation change that occurred.</span></span><br/>                          |
| [<span data-ttu-id="21a99-122">**UiaPoint**</span><span class="sxs-lookup"><span data-stu-id="21a99-122">**UiaPoint**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiapoint)<br/>                                 | <span data-ttu-id="21a99-123">Contient les coordonnées d’un point.</span><span class="sxs-lookup"><span data-stu-id="21a99-123">Contains the coordinates of a point.</span></span> <br/>                                              |
| [<span data-ttu-id="21a99-124">**UiaRect**</span><span class="sxs-lookup"><span data-stu-id="21a99-124">**UiaRect**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect)<br/>                                   | <span data-ttu-id="21a99-125">Contient la position et la taille d’un rectangle, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="21a99-125">Contains the position and size of a rectangle, in screen coordinates.</span></span><br/>              |



 

 

 





