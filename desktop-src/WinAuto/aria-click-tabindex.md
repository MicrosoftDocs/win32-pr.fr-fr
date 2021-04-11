---
title: Erreur de la TabIndex ARIA
description: Erreur de la TabIndex ARIA
ms.assetid: CCBC56E8-8899-4962-8315-762538CA666C
keywords:
- AriaTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acfec56fe1f9f6074579a8b84bccc9dfdef2e1da
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104032029"
---
# <a name="aria-tabindex-error"></a><span data-ttu-id="e8510-104">Erreur de la TabIndex ARIA</span><span class="sxs-lookup"><span data-stu-id="e8510-104">ARIA Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="e8510-105">Texte</span><span class="sxs-lookup"><span data-stu-id="e8510-105">Text</span></span>

<span data-ttu-id="e8510-106">L’élément n’est pas désactivé et possède un gestionnaire d’événements **Click** , mais il a **TabIndex** < 0 et n’est pas dans l’ordre de tabulation par défaut.</span><span class="sxs-lookup"><span data-stu-id="e8510-106">Element is not disabled and has a **click** event handler but it has **tabIndex** < 0 and is not in the tab order by default.</span></span>

## <a name="type"></a><span data-ttu-id="e8510-107">Type</span><span class="sxs-lookup"><span data-stu-id="e8510-107">Type</span></span>

<span data-ttu-id="e8510-108">Error</span><span class="sxs-lookup"><span data-stu-id="e8510-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="e8510-109">Description</span><span class="sxs-lookup"><span data-stu-id="e8510-109">Description</span></span>

<span data-ttu-id="e8510-110">Cette erreur s’applique aux éléments qui ont un gestionnaire d’événements Click et qui ne sont pas désactivés.</span><span class="sxs-lookup"><span data-stu-id="e8510-110">This error applies to elements that have a click event handler and are not disabled.</span></span> <span data-ttu-id="e8510-111">Ces éléments doivent être dans l’ordre de tabulation.</span><span class="sxs-lookup"><span data-stu-id="e8510-111">These elements must be in the tab order.</span></span> <span data-ttu-id="e8510-112">Cela garantit qu’un élément peut être atteint à l’aide de la touche Tab, ce qui indique comment les utilisateurs de lecteurs d’écran parcourent généralement l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e8510-112">This ensures that an element can be reached using the Tab key, which is how screen reader users typically navigate the UI.</span></span>

<span data-ttu-id="e8510-113">Pour corriger cette erreur, affectez à l’attribut [**TabIndex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) une valeur supérieure ou égale à 0.</span><span class="sxs-lookup"><span data-stu-id="e8510-113">To fix this error, set the [**tabindex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) attribute to a value that is equal to or greater than 0.</span></span> <span data-ttu-id="e8510-114">Vous n’avez pas besoin de définir explicitement l’attribut **TabIndex** pour les balises qui sont dans l’ordre de tabulation par défaut, par exemple un (avec attribut [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) ), un [**bouton**](https://developer.mozilla.org/docs/Web/HTML/Element/button), une [**entrée**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (à l’exclusion de « masqué »), une [**sélection**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**un**](https://developer.mozilla.org/docs/Web/HTML/Element/a) élément [**textarea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea)et une [**zone**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (dans le cadre de l’image interactive).</span><span class="sxs-lookup"><span data-stu-id="e8510-114">You do not need to explicitly set the **tabindex** attribute for tags that are in the tab order by default, such as [**a**](https://developer.mozilla.org/docs/Web/HTML/Element/a) (with [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) attribute), [**button**](https://developer.mozilla.org/docs/Web/HTML/Element/button), [**input**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (excluding "hidden"), [**select**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**textarea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea), and [**area**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (as part of the image map).</span></span>

## <a name="example"></a><span data-ttu-id="e8510-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="e8510-115">Example</span></span>


```HTML
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




