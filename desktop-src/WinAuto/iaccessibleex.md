---
title: Interface IAccessibleEx
description: Les contrôles qui n’ont pas de fournisseur UI Automation Microsoft, mais qui implémentent IAccessible, peuvent facilement être mis à niveau pour fournir une fonctionnalité d’automatisation d’interface utilisateur en implémentant l’interface IAccessibleEx.
ms.assetid: 5523156e-c9b8-4aad-b568-f3b3c402d33e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a74e7d464acf18244d91bc69199a56004b20beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100769"
---
# <a name="the-iaccessibleex-interface"></a><span data-ttu-id="2c616-103">Interface IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="2c616-103">The IAccessibleEx Interface</span></span>

<span data-ttu-id="2c616-104">Les contrôles qui n’ont pas de fournisseur UI Automation Microsoft, mais qui implémentent [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), peuvent facilement être mis à niveau pour fournir une fonctionnalité d’automatisation d’interface utilisateur en implémentant l’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="2c616-104">Controls that do not have a Microsoft UI Automation provider, but that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), can easily be upgraded to provide some UI Automation functionality by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span> <span data-ttu-id="2c616-105">Cette interface permet au contrôle d’exposer des propriétés UI Automation et des modèles de contrôle, sans avoir besoin d’une implémentation complète des interfaces du fournisseur UI Automation telles que [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span><span class="sxs-lookup"><span data-stu-id="2c616-105">This interface enables the control to expose UI Automation properties and control patterns, without the need for a full implementation of UI Automation provider interfaces such as [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span></span> <span data-ttu-id="2c616-106">Pour utiliser **IAccessibleEx**, **IRawElementProviderFragment** et toutes les autres interfaces UI Automation, incluez le fichier d’en-tête uiautomation. h dans votre code source.</span><span class="sxs-lookup"><span data-stu-id="2c616-106">To use **IAccessibleEx**, **IRawElementProviderFragment**, and all other UI Automation interfaces, include the UIAutomation.h header file in your source code.</span></span>

<span data-ttu-id="2c616-107">Par exemple, considérez un contrôle personnalisé qui a une valeur de plage.</span><span class="sxs-lookup"><span data-stu-id="2c616-107">For example, consider a custom control that has a range value.</span></span> <span data-ttu-id="2c616-108">Le serveur Microsoft Active Accessibility pour le contrôle définit le rôle du contrôle et est en mesure de retourner sa valeur actuelle.</span><span class="sxs-lookup"><span data-stu-id="2c616-108">The Microsoft Active Accessibility server for the control defines the control's role and is able to return its current value.</span></span> <span data-ttu-id="2c616-109">Toutefois, étant donné que Microsoft Active Accessibility ne définit pas de propriétés minimales et maximales, le serveur n’a pas la possibilité de retourner les valeurs minimale et maximale du contrôle.</span><span class="sxs-lookup"><span data-stu-id="2c616-109">However, because Microsoft Active Accessibility does not define minimum and maximum properties, the server lacks the means to return the minimum and maximum values of the control.</span></span> <span data-ttu-id="2c616-110">Un client UI Automation est en mesure de récupérer le rôle du contrôle, la valeur actuelle et d’autres propriétés de Active Accessibility Microsoft, car le noyau UI Automation peut les obtenir via [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="2c616-110">A UI Automation client is able to retrieve the control's role, current value, and other Microsoft Active Accessibility properties, because the UI Automation core can obtain these through [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="2c616-111">Toutefois, sans accès à une interface [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) sur l’objet, UI Automation ne peut pas non plus récupérer les valeurs maximale et minimale.</span><span class="sxs-lookup"><span data-stu-id="2c616-111">However, without access to an [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface on the object, UI Automation is also unable to retrieve the maximum and minimum values.</span></span>

<span data-ttu-id="2c616-112">Le développeur de contrôle peut fournir un fournisseur UI Automation complet pour le contrôle, mais cela signifierait la duplication d’une grande partie des fonctionnalités existantes de l’implémentation de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : par exemple, la navigation et les propriétés communes.</span><span class="sxs-lookup"><span data-stu-id="2c616-112">The control developer could supply a complete UI Automation provider for the control, but this would mean duplicating much of the existing functionality of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation: for example, navigation and common properties.</span></span> <span data-ttu-id="2c616-113">Au lieu de cela, le développeur peut continuer à s’appuyer sur **IAccessible** pour fournir cette fonctionnalité, tout en ajoutant la prise en charge des propriétés spécifiques au contrôle par le biais de [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span><span class="sxs-lookup"><span data-stu-id="2c616-113">Instead, the developer can continue to rely on **IAccessible** to supply this functionality, while adding support for control-specific properties through [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2c616-114">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="2c616-114">In this section</span></span>

-   [<span data-ttu-id="2c616-115">Instructions d’implémentation de IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="2c616-115">IAccessibleEx Implementation Guidelines</span></span>](iaccessibleex-implementation-guidelines.md)
-   [<span data-ttu-id="2c616-116">Implémentation de IAccessibleEx pour les fournisseurs</span><span class="sxs-lookup"><span data-stu-id="2c616-116">Implementing IAccessibleEx for Providers</span></span>](implementing-iaccessibleex-for-providers.md)
-   [<span data-ttu-id="2c616-117">Utilisation de IAccessibleEx à partir d’un client</span><span class="sxs-lookup"><span data-stu-id="2c616-117">Using IAccessibleEx from a Client</span></span>](using-iaccessibleex-from-a-client.md)

## <a name="related-topics"></a><span data-ttu-id="2c616-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c616-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c616-119">Infrastructure commune</span><span class="sxs-lookup"><span data-stu-id="2c616-119">Common Infrastructure</span></span>](common-infrastructure.md)
</dt> </dl>

 

 




