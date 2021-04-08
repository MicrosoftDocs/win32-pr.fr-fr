---
title: Erreur de table de présentation ARIA
description: Erreur de table de présentation ARIA
ms.assetid: 3D5AE911-78E5-4C40-B77B-604E65839F63
keywords:
- AriaLayoutTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae1ef7cae971e6dc365bd3f8ebe6135561f3ff3
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734588"
---
# <a name="aria-presentation-table-error"></a><span data-ttu-id="93537-104">Erreur de table de présentation ARIA</span><span class="sxs-lookup"><span data-stu-id="93537-104">ARIA Presentation Table Error</span></span>

## <a name="text"></a><span data-ttu-id="93537-105">Texte</span><span class="sxs-lookup"><span data-stu-id="93537-105">Text</span></span>

<span data-ttu-id="93537-106">La table utilisée pour la disposition ne doit pas avoir d’en-tête, de nom accessible ou d’informations de résumé définis (**th**, **Summary**, **Aria-DescribedBy**, **aria-labelledby**, **Aria-label**, **titre**, attributs de **légende** ).</span><span class="sxs-lookup"><span data-stu-id="93537-106">Table used for layout must not have header, accessible name or summary information defined (**th**, **summary**, **aria-describedby**, **aria-labelledby**, **aria-label**, **title**, **caption** attributes).</span></span>

## <a name="type"></a><span data-ttu-id="93537-107">Type</span><span class="sxs-lookup"><span data-stu-id="93537-107">Type</span></span>

<span data-ttu-id="93537-108">Error</span><span class="sxs-lookup"><span data-stu-id="93537-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="93537-109">Description</span><span class="sxs-lookup"><span data-stu-id="93537-109">Description</span></span>

<span data-ttu-id="93537-110">Cette erreur s’applique aux balises de table HTML dont l’attribut [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) a la valeur « Presentation », ou à une table comportant une seule cellule (table 1 × 1).</span><span class="sxs-lookup"><span data-stu-id="93537-110">This error applies to HTML table tags that have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute set to "presentation", or with a table that has a single cell (1×1 table).</span></span>

<span data-ttu-id="93537-111">Cette erreur indique qu’une table est marquée en tant que disposition uniquement (has `role="presentation"` ), mais elle contient également des informations d’accessibilité comme s’il s’agissait d’une table de données, ce qui peut prêter à confusion pour les utilisateurs de lecteur d’écran.</span><span class="sxs-lookup"><span data-stu-id="93537-111">This error indicates that a table is marked as layout only (has `role="presentation"`), but it also contains accessibility information as if it was a data table, which can be confusing for screen reader users.</span></span>

<span data-ttu-id="93537-112">Pour résoudre cette erreur, déterminez si la table est simplement une table de disposition et, le cas échéant, supprimez le balisage accessible :</span><span class="sxs-lookup"><span data-stu-id="93537-112">To address this error, determine whether the table actually is just a layout table and, if so, remove the accessible markup:</span></span>

-   <span data-ttu-id="93537-113">Attribut [**Caption**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) , [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)ou [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) .</span><span class="sxs-lookup"><span data-stu-id="93537-113">[**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) element, [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), or [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attributes.</span></span>
-   <span data-ttu-id="93537-114">attributs [**Summary**](https://www.bing.com/search?q=**summary**) ou [**Aria-DescribedBy**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .</span><span class="sxs-lookup"><span data-stu-id="93537-114">[**summary**](https://www.bing.com/search?q=**summary**) or [**aria-describedby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>
-   <span data-ttu-id="93537-115">Balises [**thead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) .</span><span class="sxs-lookup"><span data-stu-id="93537-115">[**THEAD**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) tags.</span></span>

## <a name="example"></a><span data-ttu-id="93537-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="93537-116">Example</span></span>

![<span data-ttu-id="93537-117">html pour un élément table, avec des attributs tels que le résumé qui déclenche l’erreur de table de présentation Aria affichée comme balise HTML barrée</span><span class="sxs-lookup"><span data-stu-id="93537-117">html for a table element, with attributes such as summary that trigger the aria presentation table error shown as struck-out html markup</span></span> ](images/aria-layout-table.png)

## <a name="remarks"></a><span data-ttu-id="93537-118">Notes</span><span class="sxs-lookup"><span data-stu-id="93537-118">Remarks</span></span>

<span data-ttu-id="93537-119">Si vous déterminez qu’une table a besoin d’informations d’accessibilité, supprimez l’attribut de [**rôle**](https://developer.mozilla.org/docs/Web/HTML/Reference) ou affectez-lui une valeur autre que « Presentation ».</span><span class="sxs-lookup"><span data-stu-id="93537-119">If you determine that a table does need accessibility information, remove the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute or set it to a value other than "presentation".</span></span>

 

 




