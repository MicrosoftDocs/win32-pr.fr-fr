---
title: Propriété Value
description: La propriété valeur fournit une représentation textuelle des informations visuelles contenues dans un objet. Tous les objets ne prennent pas en charge la propriété Value.
ms.assetid: 89b99645-31f5-458a-ae61-a72bf1338195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6cd3ad86b9ce3a4fcc917fc4f49792adf432bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310153"
---
# <a name="value-property"></a><span data-ttu-id="50abe-104">Propriété Value</span><span class="sxs-lookup"><span data-stu-id="50abe-104">Value Property</span></span>

<span data-ttu-id="50abe-105">La propriété **valeur** fournit une représentation textuelle des informations visuelles contenues dans un objet.</span><span class="sxs-lookup"><span data-stu-id="50abe-105">The **Value** property provides a textual representation of the visual information contained in an object.</span></span> <span data-ttu-id="50abe-106">Tous les objets ne prennent pas en charge la propriété **value** .</span><span class="sxs-lookup"><span data-stu-id="50abe-106">Not all objects support the **Value** property.</span></span>

<span data-ttu-id="50abe-107">La propriété **value** est récupérée en appelant [**IAccessible :: \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span><span class="sxs-lookup"><span data-stu-id="50abe-107">The **Value** property is retrieved by calling [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span></span>

<span data-ttu-id="50abe-108">La propriété **valeur** indique au client les informations visuelles contenues dans un objet.</span><span class="sxs-lookup"><span data-stu-id="50abe-108">The **Value** property tells the client about the visual information contained in an object.</span></span> <span data-ttu-id="50abe-109">Par exemple, la valeur d’un contrôle d’édition est le texte qu’il contient, alors qu’un élément de menu n’a pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="50abe-109">For example, an edit control's value is the text it contains, whereas a menu item has no value.</span></span>

## <a name="providing-hierarchical-information"></a><span data-ttu-id="50abe-110">Fournir des informations hiérarchiques</span><span class="sxs-lookup"><span data-stu-id="50abe-110">Providing Hierarchical Information</span></span>

<span data-ttu-id="50abe-111">La propriété **value** fournit des informations hiérarchiques dans les cas tels qu’un contrôle Tree View.</span><span class="sxs-lookup"><span data-stu-id="50abe-111">The **Value** property provides hierarchical information in cases such as a tree view control.</span></span> <span data-ttu-id="50abe-112">Bien que l’objet parent dans le contrôle TreeView ne fournisse pas d’informations dans la propriété **value** , chaque élément du contrôle a une valeur de base zéro qui représente son niveau dans la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="50abe-112">Although the parent object in the tree view control does not provide information in the **Value** property, each item within the control has a zero-based value that represents its level within the hierarchy.</span></span> <span data-ttu-id="50abe-113">Les éléments de niveau supérieur ont une valeur de zéro, les éléments de second niveau ont la valeur un, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="50abe-113">Top-level items have a value of zero, second-level items have a value of one, and so on.</span></span>

 

 




