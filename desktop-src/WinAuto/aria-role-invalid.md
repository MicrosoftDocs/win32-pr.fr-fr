---
title: Erreur de rôle ARIA
description: Erreur de rôle ARIA
ms.assetid: FEEB4F28-4A71-4417-A2F9-ABCB86B44F0F
keywords:
- AriaRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df04ad94d68ae1e8e2e8d3352aa349834a2389fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "106511521"
---
# <a name="aria-role-error"></a><span data-ttu-id="f118c-104">Erreur de rôle ARIA</span><span class="sxs-lookup"><span data-stu-id="f118c-104">ARIA Role Error</span></span>

## <a name="text"></a><span data-ttu-id="f118c-105">Texte</span><span class="sxs-lookup"><span data-stu-id="f118c-105">Text</span></span>

<span data-ttu-id="f118c-106">L’élément a un rôle WAI-ARIA non valide.</span><span class="sxs-lookup"><span data-stu-id="f118c-106">Element has invalid WAI-ARIA role.</span></span>

## <a name="type"></a><span data-ttu-id="f118c-107">Type</span><span class="sxs-lookup"><span data-stu-id="f118c-107">Type</span></span>

<span data-ttu-id="f118c-108">Error</span><span class="sxs-lookup"><span data-stu-id="f118c-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="f118c-109">Description</span><span class="sxs-lookup"><span data-stu-id="f118c-109">Description</span></span>

<span data-ttu-id="f118c-110">Cette erreur s’applique à tous les éléments qui ont l’attribut [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) .</span><span class="sxs-lookup"><span data-stu-id="f118c-110">This error applies to all elements that have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute.</span></span> <span data-ttu-id="f118c-111">Elle indique que l’attribut de **rôle** n’est pas une initiative d’accessibilité Web valide-valeur de rôle WAI-ARIA (Rich Internet applications) accessible comme défini par la spécification WAI-ARIA.</span><span class="sxs-lookup"><span data-stu-id="f118c-111">It indicates that the **role** attribute is not a valid Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role value as defined by the WAI-ARIA specification.</span></span> <span data-ttu-id="f118c-112">La définition d’un rôle valide permet de s’assurer que l’élément est correctement interprété par les lecteurs d’écran et d’autres outils de technologie d’assistance.</span><span class="sxs-lookup"><span data-stu-id="f118c-112">Setting a valid role helps ensure that the element is correctly interpreted by screen readers and other assistive technology tools.</span></span>

<span data-ttu-id="f118c-113">Pour corriger cette erreur, affectez à l’attribut [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) une valeur de rôle WAI-ARIA valide.</span><span class="sxs-lookup"><span data-stu-id="f118c-113">To fix this error, set the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute to a valid WAI-ARIA role value.</span></span> <span data-ttu-id="f118c-114">Notez que les rôles en WAI-ARIA abstraits ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="f118c-114">Note that abstract WAI-ARIA roles are not valid.</span></span>

## <a name="example"></a><span data-ttu-id="f118c-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="f118c-115">Example</span></span>


```HTML
<!—The invalid role will not expose this element as a button. -->
<div role="backbutton" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >

<!—Setting the correct role will expose this as a button that can be clicked. -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



## <a name="related-topics"></a><span data-ttu-id="f118c-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f118c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f118c-117">Erreur de rôle de conteneur ARIA</span><span class="sxs-lookup"><span data-stu-id="f118c-117">ARIA Container Role Error</span></span>](aria-container-role.md)
</dt> </dl>

 

 




