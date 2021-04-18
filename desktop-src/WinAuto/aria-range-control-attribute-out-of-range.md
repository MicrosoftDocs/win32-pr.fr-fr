---
title: Attributs de contrôle de plage ARIA incompatibles
description: Attributs de contrôle de plage ARIA incompatibles
ms.assetid: 265AE578-D841-4931-9F4A-97BB86ECEC88
keywords:
- AriaRangeControlAttributesIncompatibleId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef55ee57c4966896e666dd5a7ac1d20eb5257c6
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104508182"
---
# <a name="aria-range-control-attributes-incompatible"></a><span data-ttu-id="49c24-104">Attributs de contrôle de plage ARIA incompatibles</span><span class="sxs-lookup"><span data-stu-id="49c24-104">ARIA Range Control Attributes Incompatible</span></span>

## <a name="text"></a><span data-ttu-id="49c24-105">Texte</span><span class="sxs-lookup"><span data-stu-id="49c24-105">Text</span></span>

<span data-ttu-id="49c24-106">L’élément a le rôle **ProgressBar** ou **Slider** , mais la valeur **Aria-valuenow** exposée est en dehors de la plage Aria **-valuemin** **Aria-ValueMax** .</span><span class="sxs-lookup"><span data-stu-id="49c24-106">Element has **progressbar** or **slider** role but exposed **aria-valuenow** value is outside of **aria-valuemin** **aria-valuemax** range.</span></span>

## <a name="type"></a><span data-ttu-id="49c24-107">Type</span><span class="sxs-lookup"><span data-stu-id="49c24-107">Type</span></span>

<span data-ttu-id="49c24-108">Error</span><span class="sxs-lookup"><span data-stu-id="49c24-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="49c24-109">Description</span><span class="sxs-lookup"><span data-stu-id="49c24-109">Description</span></span>

<span data-ttu-id="49c24-110">Cette erreur s’applique aux éléments qui ont un [**rôle**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicite ou explicite) égal à **ProgressBar**, **Slider** ou **SpinButton**.</span><span class="sxs-lookup"><span data-stu-id="49c24-110">This error applies to elements that have a [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicit or explicit) equal to **progressbar**, **slider**, or **spinbutton**.</span></span>

<span data-ttu-id="49c24-111">Cette erreur indique que la valeur [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) exposée n’est pas dans la plage définie par les attributs [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) et [**Aria-ValueMax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .</span><span class="sxs-lookup"><span data-stu-id="49c24-111">This error indicates that the exposed [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) value is not in the range defined by the [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) and [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>

<span data-ttu-id="49c24-112">Pour corriger cette erreur, vérifiez votre implémentation pour vous assurer que les attributs [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) et [**Aria-ValueMax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) sont correctement définis et que la valeur de l’attribut [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) est correctement gérée.</span><span class="sxs-lookup"><span data-stu-id="49c24-112">To fix this error, check your implementation to ensure that the [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) and [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes are correctly set, and that the [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute value is properly maintained.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49c24-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="49c24-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49c24-114">Attributs de contrôle de plage ARIA manquants</span><span class="sxs-lookup"><span data-stu-id="49c24-114">ARIA Range Control Attributes Missing</span></span>](aria-range-control-attributes-missing.md)
</dt> </dl>

 

 




