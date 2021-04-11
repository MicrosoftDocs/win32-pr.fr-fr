---
description: La méthode GetButtonRect récupère le rectangle pour le bouton spécifié, dans les coordonnées de la fenêtre.
ms.assetid: 359e9483-d7ba-45b0-882b-5a4c56dc0350
title: Méthode GetButtonRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 752c90637ee58aaa862245b29536dc71ad8e9a1c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108523"
---
# <a name="getbuttonrect-method"></a><span data-ttu-id="15ffc-103">Méthode GetButtonRect</span><span class="sxs-lookup"><span data-stu-id="15ffc-103">GetButtonRect Method</span></span>

> [!Note]  
> <span data-ttu-id="15ffc-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="15ffc-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="15ffc-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="15ffc-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="15ffc-106">La `GetButtonRect` méthode récupère le rectangle pour le bouton spécifié, en coordonnées de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="15ffc-106">The `GetButtonRect` method retrieves the rectangle for the specified button, in window coordinates.</span></span>

``` syntax
[ oButton = ] MSWebDVD.GetButtonRect(iButton)
```

## <a name="parameters"></a><span data-ttu-id="15ffc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15ffc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15ffc-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span><span class="sxs-lookup"><span data-stu-id="15ffc-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span></span>
</dt> <dd>

<span data-ttu-id="15ffc-109">Spécifie le numéro de bouton sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="15ffc-109">Specifies the button number as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15ffc-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="15ffc-110">Return Value</span></span>

<span data-ttu-id="15ffc-111">Retourne un objet [DVDRect](dvdrect-object.md) qui définit le rectangle.</span><span class="sxs-lookup"><span data-stu-id="15ffc-111">Returns a [DVDRect](dvdrect-object.md) object that defines the rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="15ffc-112">Notes</span><span class="sxs-lookup"><span data-stu-id="15ffc-112">Remarks</span></span>

<span data-ttu-id="15ffc-113">Utilisez cette méthode lors de l’implémentation de la gestion de souris personnalisée après avoir défini [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) sur **true**.</span><span class="sxs-lookup"><span data-stu-id="15ffc-113">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="15ffc-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15ffc-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15ffc-115">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="15ffc-115">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="15ffc-116">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="15ffc-116">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="15ffc-117">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="15ffc-117">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="15ffc-118">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="15ffc-118">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="15ffc-119">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="15ffc-119">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



