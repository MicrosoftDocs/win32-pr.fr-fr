---
title: Description, propriété (fonctionnalités d’accessibilité Windows)
description: La propriété Description d’un objet fournit une description textuelle de l’apparence visuelle d’un objet.
ms.assetid: 1fe3221f-e1dd-44b2-b749-d00bee1b6b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34320b2959899d049d959037c0f24299780b54b0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464150"
---
# <a name="description-property-windows-accessibility-features"></a><span data-ttu-id="664ef-103">Description, propriété (fonctionnalités d’accessibilité Windows)</span><span class="sxs-lookup"><span data-stu-id="664ef-103">Description Property (Windows Accessibility features)</span></span>

> [!Note]  
> <span data-ttu-id="664ef-104">La propriété **Description** est souvent utilisée de manière incorrecte et n’est pas prise en charge par Microsoft UI Automation.</span><span class="sxs-lookup"><span data-stu-id="664ef-104">The **Description** property is often used incorrectly and is not supported by Microsoft UI Automation.</span></span> <span data-ttu-id="664ef-105">Les développeurs Microsoft Active Accessibility Server ne doivent pas utiliser cette propriété.</span><span class="sxs-lookup"><span data-stu-id="664ef-105">Microsoft Active Accessibility server developers should not use this property.</span></span> <span data-ttu-id="664ef-106">Si des informations supplémentaires sont nécessaires pour l’accessibilité et les scénarios d’automatisation, utilisez les propriétés prises en charge par les éléments UI Automation et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="664ef-106">If more information is needed for accessibility and automation scenarios, use the properties supported by UI Automation elements and control patterns.</span></span>

 

<span data-ttu-id="664ef-107">La propriété **Description** d’un objet fournit une description textuelle de l’apparence visuelle d’un objet.</span><span class="sxs-lookup"><span data-stu-id="664ef-107">An object's **Description** property provides a textual description about an object's visual appearance.</span></span> <span data-ttu-id="664ef-108">La description est principalement utilisée pour fournir un contexte plus grand pour les utilisateurs malvoyants ou aveugles, mais elle est également utilisée pour la recherche de contexte ou d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="664ef-108">The description is primarily used to provide greater context for low-vision or blind users, but is also used for context searching or other applications.</span></span> <span data-ttu-id="664ef-109">Cette propriété peut aider les utilisateurs à comprendre une icône ou l’apparence visuelle globale.</span><span class="sxs-lookup"><span data-stu-id="664ef-109">This property can help users understand an icon or the overall visual appearance.</span></span>

<span data-ttu-id="664ef-110">La propriété **Description** est récupérée en appelant [**IAccessible :: \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).</span><span class="sxs-lookup"><span data-stu-id="664ef-110">The **Description** property is retrieved by calling [**IAccessible::get\_accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).</span></span>

## <a name="when-to-support-the-description-property"></a><span data-ttu-id="664ef-111">Quand prendre en charge la propriété Description</span><span class="sxs-lookup"><span data-stu-id="664ef-111">When to Support the Description Property</span></span>

<span data-ttu-id="664ef-112">Les serveurs prennent en charge la propriété **Description** si la description n’est pas évidente ou lorsqu’elle n’est pas redondante en fonction des propriétés [**Name**](name-property.md), [**role**](role-property.md), [**State**](state-property.md)et [**value**](value-property.md) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="664ef-112">Servers support the **Description** property if the description is not obvious, or when it is not redundant based on the object's [**Name**](name-property.md), [**Role**](role-property.md), [**State**](state-property.md), and [**Value**](value-property.md) properties.</span></span> <span data-ttu-id="664ef-113">Par exemple, un bouton intitulé « OK » n’a pas besoin d’informations supplémentaires, alors qu’un bouton qui affiche une image d’un cactus.</span><span class="sxs-lookup"><span data-stu-id="664ef-113">For example, a button labeled "OK" would not need additional information, whereas a button that shows a picture of a cactus would.</span></span> <span data-ttu-id="664ef-114">Le **nom**, le **rôle** et les propriétés d' [**aide**](help-property.md) d’un tel bouton décrivent son rôle, mais la propriété **Description** transmet des informations moins tangibles. par exemple, « ce bouton affiche une image d’un cactus ».</span><span class="sxs-lookup"><span data-stu-id="664ef-114">The **Name**, **Role**, and [**Help**](help-property.md) properties for such a button describe its purpose, but the **Description** property conveys information that is less tangible; for example, "This button shows a picture of a cactus."</span></span>

<span data-ttu-id="664ef-115">Un serveur Microsoft Active Accessibility peut ajouter la prise en charge d’UI Automation en utilisant l' [annotation directe](direct-annotation.md), à l’aide de l’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) , ou en implémentant Microsoft Active Accessibility et UI Automation côte à côte avec les deux implémentations qui gèrent le message [**WM \_ GETOBJECT**](wm-getobject.md) .</span><span class="sxs-lookup"><span data-stu-id="664ef-115">A Microsoft Active Accessibility server can add support for UI Automation by using [Direct Annotation](direct-annotation.md), using the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface, or by implementing Microsoft Active Accessibility and UI Automation side-by-side with both implementations handling the [**WM\_GETOBJECT**](wm-getobject.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="664ef-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="664ef-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="664ef-117">Utilisation de l’annotation directe</span><span class="sxs-lookup"><span data-stu-id="664ef-117">Using Direct Annotation</span></span>](using-direct-annotation.md)
</dt> <dt>

[<span data-ttu-id="664ef-118">Interface IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="664ef-118">The IAccessibleEx Interface</span></span>](iaccessibleex.md)
</dt> </dl>

 

 




