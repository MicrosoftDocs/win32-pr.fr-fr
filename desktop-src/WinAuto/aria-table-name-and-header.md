---
title: Erreur de table de données ARIA
description: Erreur de table de données ARIA
ms.assetid: 3D0448BB-50DC-4C85-93BD-D8E626475AB0
keywords:
- AriaDataTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286f88a0b3a0d962fd6ac45581f94bc351cb507
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383103"
---
# <a name="aria-data-table-error"></a><span data-ttu-id="5269c-104">Erreur de table de données ARIA</span><span class="sxs-lookup"><span data-stu-id="5269c-104">ARIA Data Table Error</span></span>

## <a name="text"></a><span data-ttu-id="5269c-105">Texte</span><span class="sxs-lookup"><span data-stu-id="5269c-105">Text</span></span>

<span data-ttu-id="5269c-106">La table contient des données, mais n’a pas de balise accessible définie via **les éléments Aria-label**, **aria-labelledby**, **title**, **Caption** ou **th** .</span><span class="sxs-lookup"><span data-stu-id="5269c-106">Table contains data but doesn't have accessible markup defined though **aria-label**, **aria-labelledby**, **title**, **caption** or **th** elements.</span></span>

## <a name="type"></a><span data-ttu-id="5269c-107">Type</span><span class="sxs-lookup"><span data-stu-id="5269c-107">Type</span></span>

<span data-ttu-id="5269c-108">Error</span><span class="sxs-lookup"><span data-stu-id="5269c-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="5269c-109">Description</span><span class="sxs-lookup"><span data-stu-id="5269c-109">Description</span></span>

<span data-ttu-id="5269c-110">Cette erreur s’applique aux tableaux HTML comportant plusieurs cellules.</span><span class="sxs-lookup"><span data-stu-id="5269c-110">This error applies to HTML tables with more than one cell.</span></span> <span data-ttu-id="5269c-111">Cette erreur ne s’applique pas aux tables avec `role="presentation"` , car celles-ci sont considérées comme des tables de disposition.</span><span class="sxs-lookup"><span data-stu-id="5269c-111">This error does not apply to tables with `role="presentation"` because these are considered to be layout tables.</span></span>

<span data-ttu-id="5269c-112">Cette erreur indique qu’une table de données n’a pas de nom accessible ou d’informations d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="5269c-112">This error indicates that a data table doesn’t have an accessible name or header information.</span></span>

<span data-ttu-id="5269c-113">Pour corriger cette erreur, définissez un nom accessible à l’aide de la balise [**Caption**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) , ou des attributs [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)ou [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) .</span><span class="sxs-lookup"><span data-stu-id="5269c-113">To fix this error, define an accessible name by using the [**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) tag, or the [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), or [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attributes.</span></span> <span data-ttu-id="5269c-114">S’il manque des informations d’en-tête dans la table, utilisez des balises [**thead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) pour marquer les cellules d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="5269c-114">If the table is missing header information, use [**THead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) tags to mark header cells.</span></span>

## <a name="example"></a><span data-ttu-id="5269c-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="5269c-115">Example</span></span>


```HTML
<!-- Data tables must contain an accessibile name and header information. -->
<table>
  <caption>ARIA Examples</caption>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      ...
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Accessible tables</td>
      <td>This example illustrates how to make data tables accessible using ARIA</td>
      ...
    </tr>
  </tbody>
</table>
```



 

 




