---
description: La propriété CurrentButton récupère le numéro du bouton de menu sélectionné.
ms.assetid: bd9720bc-068a-4f29-aa2d-1c6b550f789c
title: Propriété CurrentButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c12def9f9a73c9538781bde6940b03bfb376fcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317721"
---
# <a name="currentbutton-property"></a><span data-ttu-id="22bb2-103">Propriété CurrentButton</span><span class="sxs-lookup"><span data-stu-id="22bb2-103">CurrentButton Property</span></span>

> [!Note]  
> <span data-ttu-id="22bb2-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="22bb2-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="22bb2-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="22bb2-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="22bb2-106">La `CurrentButton` propriété récupère le numéro du bouton de menu sélectionné.</span><span class="sxs-lookup"><span data-stu-id="22bb2-106">The `CurrentButton` property retrieves the number of the selected menu button.</span></span>

``` syntax
[ iButton = ] MSWebDVD.CurrentButton
```

## <a name="return-value"></a><span data-ttu-id="22bb2-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="22bb2-107">Return Value</span></span>

<span data-ttu-id="22bb2-108">Retourne une valeur entière représentant le bouton.</span><span class="sxs-lookup"><span data-stu-id="22bb2-108">Returns an integer value representing the button.</span></span>

## <a name="remarks"></a><span data-ttu-id="22bb2-109">Notes</span><span class="sxs-lookup"><span data-stu-id="22bb2-109">Remarks</span></span>

<span data-ttu-id="22bb2-110">Cette propriété est en lecture seule sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="22bb2-110">This property is read-only with no default value.</span></span> <span data-ttu-id="22bb2-111">Utilisez cette méthode lors de l’implémentation de la gestion de souris personnalisée après avoir défini [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) sur **true**.</span><span class="sxs-lookup"><span data-stu-id="22bb2-111">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="22bb2-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22bb2-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22bb2-113">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="22bb2-113">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="22bb2-114">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="22bb2-114">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="22bb2-115">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="22bb2-115">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="22bb2-116">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="22bb2-116">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="22bb2-117">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="22bb2-117">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="22bb2-118">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="22bb2-118">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



