---
title: Attributs de contrôle de plage ARIA manquants
description: Attributs de contrôle de plage ARIA manquants
ms.assetid: B79F6277-5339-406A-B5FC-A3657BFC5034
keywords:
- AriaRangeControlAttributesAbsentId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8cd32a7a4807f06c26bd013ee3fd294d33cc57
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104032025"
---
# <a name="aria-range-control-attributes-missing"></a><span data-ttu-id="eb702-104">Attributs de contrôle de plage ARIA manquants</span><span class="sxs-lookup"><span data-stu-id="eb702-104">ARIA Range Control Attributes Missing</span></span>

## <a name="text"></a><span data-ttu-id="eb702-105">Texte</span><span class="sxs-lookup"><span data-stu-id="eb702-105">Text</span></span>

<span data-ttu-id="eb702-106">L’élément a un rôle **ProgressBar** ou **Slider** , mais il n’expose pas les attributs **Aria-valuemin** , **Aria-ValueMax** et **Aria-valuenow** correspondants.</span><span class="sxs-lookup"><span data-stu-id="eb702-106">Element has **progressbar** or **slider** role but is not exposing corresponding **aria-valuemin** , **aria-valuemax** , and **aria-valuenow** attributes.</span></span>

## <a name="type"></a><span data-ttu-id="eb702-107">Type</span><span class="sxs-lookup"><span data-stu-id="eb702-107">Type</span></span>

<span data-ttu-id="eb702-108">Error</span><span class="sxs-lookup"><span data-stu-id="eb702-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="eb702-109">Description</span><span class="sxs-lookup"><span data-stu-id="eb702-109">Description</span></span>

<span data-ttu-id="eb702-110">Cette erreur s’applique aux éléments qui ont un [**rôle**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicite ou explicite) qui est égal à **ProgressBar**, **Slider** ou **SpinButton**.</span><span class="sxs-lookup"><span data-stu-id="eb702-110">This error applies to elements that have a [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicit or explicit) that is equal to **progressbar**, **slider**, or **spinbutton**.</span></span>

<span data-ttu-id="eb702-111">Conformément à la spécification de l’initiative de l’accessibilité du Web (WAI-ARIA) accessible par le Web, les éléments qui ont le rôle **ProgressBar**, **Slider** ou **SpinButton** doivent exposer les attributs [**Aria-ValueMax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)et [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .</span><span class="sxs-lookup"><span data-stu-id="eb702-111">According to the Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) specification, elements that have the **progressbar**, **slider**, or **spinbutton** role must expose the [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), and [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>

<span data-ttu-id="eb702-112">Pour corriger cette erreur, définissez les attributs [**Aria-ValueMax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)et [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) , et conservez dynamiquement la valeur **Aria-valuenow** pour vous assurer que la valeur actuelle est exposée.</span><span class="sxs-lookup"><span data-stu-id="eb702-112">To fix this error, set the [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), and [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes, and dynamically maintain the **aria-valuenow** value to ensure that the current value is exposed.</span></span> <span data-ttu-id="eb702-113">Vous devez également définir l’attribut [**Aria-ValueText**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) pour ajouter une plus grande signification à la valeur **Aria-valuenow** exposée.</span><span class="sxs-lookup"><span data-stu-id="eb702-113">You should also set the [**aria-valuetext**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute to add more meaning to the exposed **aria-valuenow** value.</span></span>

## <a name="example"></a><span data-ttu-id="eb702-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="eb702-114">Example</span></span>


```HTML
<div role="slider" id="sl" aria-valuemin="1" aria-valuemax="5" aria-valuenow="3" aria-valuetext="good"…>
</div>

<script>
  // This function should be triggered when the slider value changes.
  function manageValue()
  {
    ...
    sl.setAttribute("aria-valuenow", currentValue);
    sl.setAttribute("aria-valuetext", currentValueText);
    ...
  }
</script>
```



## <a name="related-topics"></a><span data-ttu-id="eb702-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb702-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb702-116">Attributs de contrôle de plage ARIA incompatibles</span><span class="sxs-lookup"><span data-stu-id="eb702-116">ARIA Range Control Attributes Incompatible</span></span>](aria-range-control-attribute-out-of-range.md)
</dt> </dl>

 

 




