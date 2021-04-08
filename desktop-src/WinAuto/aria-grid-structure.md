---
title: Erreur de structure de grille ARIA
description: Erreur de structure de grille ARIA
ms.assetid: 8B2AEC98-1056-4560-AD6E-C6ECA0B94692
keywords:
- AriaGridStructureErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd692c5fb82675b8fdcc6bf88fe35695113c9ef0
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734596"
---
# <a name="aria-grid-structure-error"></a><span data-ttu-id="d16be-104">Erreur de structure de grille ARIA</span><span class="sxs-lookup"><span data-stu-id="d16be-104">ARIA Grid Structure Error</span></span>

## <a name="text"></a><span data-ttu-id="d16be-105">Texte</span><span class="sxs-lookup"><span data-stu-id="d16be-105">Text</span></span>

<span data-ttu-id="d16be-106">L’élément avec le rôle de **grille** n’est pas associé à une structure de grille ou à un balisage accessible.</span><span class="sxs-lookup"><span data-stu-id="d16be-106">Element with the **grid** role doesn't have a corresponding grid structure or accessible markup.</span></span>

## <a name="type"></a><span data-ttu-id="d16be-107">Type</span><span class="sxs-lookup"><span data-stu-id="d16be-107">Type</span></span>

<span data-ttu-id="d16be-108">Error</span><span class="sxs-lookup"><span data-stu-id="d16be-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="d16be-109">Description</span><span class="sxs-lookup"><span data-stu-id="d16be-109">Description</span></span>

<span data-ttu-id="d16be-110">Cette erreur s’applique aux éléments personnalisés dont l’attribut **role** a la valeur « Grid ».</span><span class="sxs-lookup"><span data-stu-id="d16be-110">This error applies to custom elements that have the **role** attribute set to "grid".</span></span> <span data-ttu-id="d16be-111">Elle ne s’applique pas aux balises de table HTML qui ont un **rôle** implicite « Grid ».</span><span class="sxs-lookup"><span data-stu-id="d16be-111">It does not apply to HTML table tags that have an implicit **role** of "grid".</span></span>

<span data-ttu-id="d16be-112">Un élément dont l’attribut de **rôle** est défini sur « Grid » doit avoir la structure définie par le rôle de grille WAI-ARIA (initiative d’accessibilité Web-accessible riches Internet applications), y compris le nom accessible pour la grille et ses sous-éléments d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="d16be-112">An element that has its **role** attribute set to "grid" must have the structure defined by the Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) grid role, including the accessible name for the grid and its header subelements.</span></span>

<span data-ttu-id="d16be-113">Pour corriger cette erreur, examinez votre implémentation pour vous assurer qu’elle est conforme à la spécification WAI-ARIA.</span><span class="sxs-lookup"><span data-stu-id="d16be-113">To fix this error, review your implementation to ensure that it complies with the WAI-ARIA specification.</span></span> <span data-ttu-id="d16be-114">En particulier, vérifiez que la structure respecte les règles suivantes.</span><span class="sxs-lookup"><span data-stu-id="d16be-114">Specifically, ensure that the structure meets the following rules.</span></span>

-   <span data-ttu-id="d16be-115">**Grid** contient des éléments **Row** ou **rowgroup** .</span><span class="sxs-lookup"><span data-stu-id="d16be-115">**grid** contains **row** or **rowgroup** elements.</span></span>
-   <span data-ttu-id="d16be-116">**rowgroup** contient des éléments de **ligne** .</span><span class="sxs-lookup"><span data-stu-id="d16be-116">**rowgroup** contains **row** elements.</span></span>
-   <span data-ttu-id="d16be-117">les éléments **Row** contiennent les éléments **ColumnHeader** , **GridCell** ou **RowHeader** .</span><span class="sxs-lookup"><span data-stu-id="d16be-117">**row** elements contain **columnheader** or **gridcell** or **rowheader** elements.</span></span>

<span data-ttu-id="d16be-118">Un nom accessible doit être défini pour les éléments **Grid**, **ColumnHeader**, **GridCell** et **RowHeader** à l’aide de l’un des attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="d16be-118">An accessible name should be defined for **grid**, **columnheader**, **gridcell** and **rowheader** elements by using one of the following attributes.</span></span>

-   <span data-ttu-id="d16be-119">attribut [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) permettant de référencer l’élément contenant du texte.</span><span class="sxs-lookup"><span data-stu-id="d16be-119">[**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute for referencing the element containing text.</span></span>
-   <span data-ttu-id="d16be-120">attribut [**Aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) pour définir directement le nom accessible.</span><span class="sxs-lookup"><span data-stu-id="d16be-120">[**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute to set the accessible name directly.</span></span>
-   <span data-ttu-id="d16be-121">[**titre**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) pour la création d’une info-bulle qui est utilisée en même temps que le nom.</span><span class="sxs-lookup"><span data-stu-id="d16be-121">[**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) for creating a tooltip which is at the same time used as a name.</span></span>

 

 




