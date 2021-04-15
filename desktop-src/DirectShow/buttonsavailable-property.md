---
description: La propriété ButtonsAvailable récupère le nombre total de boutons dans le menu actuel.
ms.assetid: 4df3a7e7-1be4-4cc7-ad61-567f7f45811e
title: Propriété ButtonsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cab4afdd9f6e23a376bb72885810b8464f180d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392751"
---
# <a name="buttonsavailable-property"></a><span data-ttu-id="553dd-103">Propriété ButtonsAvailable</span><span class="sxs-lookup"><span data-stu-id="553dd-103">ButtonsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="553dd-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="553dd-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="553dd-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="553dd-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="553dd-106">La `ButtonsAvailable` propriété récupère le nombre total de boutons dans le menu actuel.</span><span class="sxs-lookup"><span data-stu-id="553dd-106">The `ButtonsAvailable` property retrieves the total number of buttons on the current menu.</span></span>

``` syntax
[ iButtons = ] MSWebDVD.ButtonsAvailable
```

## <a name="return-value"></a><span data-ttu-id="553dd-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="553dd-107">Return Value</span></span>

<span data-ttu-id="553dd-108">Retourne une valeur entière représentant le nombre de boutons.</span><span class="sxs-lookup"><span data-stu-id="553dd-108">Returns an integer value representing the number of buttons.</span></span>

## <a name="remarks"></a><span data-ttu-id="553dd-109">Notes</span><span class="sxs-lookup"><span data-stu-id="553dd-109">Remarks</span></span>

<span data-ttu-id="553dd-110">Cette propriété est en lecture seule sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="553dd-110">This property is read-only with no default value.</span></span> <span data-ttu-id="553dd-111">Utilisez cette méthode lors de l’implémentation de la gestion de souris personnalisée après avoir défini [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) sur **true**.</span><span class="sxs-lookup"><span data-stu-id="553dd-111">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="553dd-112">Appelez cette méthode pour récupérer la limite supérieure de la plage de numéros de boutons valides.</span><span class="sxs-lookup"><span data-stu-id="553dd-112">Call this method to retrieve the upper limit for the range of valid button numbers.</span></span>

## <a name="see-also"></a><span data-ttu-id="553dd-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="553dd-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="553dd-114">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="553dd-114">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="553dd-115">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="553dd-115">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="553dd-116">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="553dd-116">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="553dd-117">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="553dd-117">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="553dd-118">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="553dd-118">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



