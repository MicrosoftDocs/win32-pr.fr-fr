---
description: La méthode ActivateAtPosition active le bouton de menu à la position spécifiée.
ms.assetid: eddc4880-dd78-4d96-8bff-c5c883a19927
title: Méthode ActivateAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64a83e7fcbc00990c7be7d1a99638a1b4a3de14b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109719"
---
# <a name="activateatposition-method"></a><span data-ttu-id="4e087-103">Méthode ActivateAtPosition</span><span class="sxs-lookup"><span data-stu-id="4e087-103">ActivateAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="4e087-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4e087-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4e087-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4e087-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4e087-106">La méthode ActivateAtPosition active le bouton de menu à la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4e087-106">The ActivateAtPosition method activates the menu button at the specified position.</span></span>

``` syntax
        MSWebDVD.ActivateAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="4e087-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e087-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e087-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="4e087-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="4e087-109">Spécifie la coordonnée x comme un entier.</span><span class="sxs-lookup"><span data-stu-id="4e087-109">Specifies x-coordinate as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="4e087-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*PosY*</span><span class="sxs-lookup"><span data-stu-id="4e087-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="4e087-111">Spécifie la coordonnée y sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="4e087-111">Specifies the y-coordinate as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e087-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4e087-112">Return Value</span></span>

<span data-ttu-id="4e087-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="4e087-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e087-114">Notes</span><span class="sxs-lookup"><span data-stu-id="4e087-114">Remarks</span></span>

<span data-ttu-id="4e087-115">Utilisez cette méthode lors de l’implémentation de la gestion de souris personnalisée après avoir défini [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) sur **true**.</span><span class="sxs-lookup"><span data-stu-id="4e087-115">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e087-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e087-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e087-117">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="4e087-117">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="4e087-118">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="4e087-118">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="4e087-119">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="4e087-119">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="4e087-120">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="4e087-120">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="4e087-121">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="4e087-121">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="4e087-122">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="4e087-122">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



