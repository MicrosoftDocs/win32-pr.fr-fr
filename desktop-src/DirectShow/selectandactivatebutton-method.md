---
description: La méthode SelectAndActivateButton sélectionne et active le bouton spécifié.
ms.assetid: fa6239ea-0478-41f1-9515-d67a7fad11db
title: Méthode SelectAndActivateButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717af00becd5f00f55b166353246f92ea7dfd1bd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517151"
---
# <a name="selectandactivatebutton-method"></a><span data-ttu-id="69d76-103">Méthode SelectAndActivateButton</span><span class="sxs-lookup"><span data-stu-id="69d76-103">SelectAndActivateButton Method</span></span>

> [!Note]  
> <span data-ttu-id="69d76-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="69d76-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="69d76-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="69d76-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="69d76-106">La `SelectAndActivateButton` méthode sélectionne et active le bouton spécifié.</span><span class="sxs-lookup"><span data-stu-id="69d76-106">The `SelectAndActivateButton` method selects and activates the specified button.</span></span>

``` syntax
MSWebDVD.SelectAndActivateButton(iButton)
```

## <a name="parameters"></a><span data-ttu-id="69d76-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69d76-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69d76-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span><span class="sxs-lookup"><span data-stu-id="69d76-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span></span>
</dt> <dd>

<span data-ttu-id="69d76-109">Spécifie le bouton sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="69d76-109">Specifies the button as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69d76-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="69d76-110">Return Value</span></span>

<span data-ttu-id="69d76-111">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="69d76-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="69d76-112">Notes</span><span class="sxs-lookup"><span data-stu-id="69d76-112">Remarks</span></span>

<span data-ttu-id="69d76-113">Utilisez cette méthode lors de l’implémentation de la gestion de souris personnalisée après avoir défini [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) sur **true**.</span><span class="sxs-lookup"><span data-stu-id="69d76-113">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="69d76-114">Cette méthode met en surbrillance le bouton spécifié et l’active automatiquement.</span><span class="sxs-lookup"><span data-stu-id="69d76-114">This method highlights the specified button and activate it automatically.</span></span>

## <a name="see-also"></a><span data-ttu-id="69d76-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69d76-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69d76-116">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="69d76-116">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="69d76-117">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="69d76-117">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="69d76-118">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="69d76-118">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="69d76-119">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="69d76-119">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="69d76-120">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="69d76-120">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="69d76-121">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="69d76-121">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



