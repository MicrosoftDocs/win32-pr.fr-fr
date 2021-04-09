---
description: La méthode GetButtonAtPosition récupère le numéro du bouton aux coordonnées spécifiées sans le sélectionner ou l’activer.
ms.assetid: ac933d0d-db2e-488f-b661-2fdc9f5acb39
title: Méthode GetButtonAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9347929946a6f26cac4652a5357bd6454c80446c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108526"
---
# <a name="getbuttonatposition-method"></a><span data-ttu-id="737e7-103">Méthode GetButtonAtPosition</span><span class="sxs-lookup"><span data-stu-id="737e7-103">GetButtonAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="737e7-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="737e7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="737e7-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="737e7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="737e7-106">La `GetButtonAtPosition` méthode récupère le numéro du bouton aux coordonnées spécifiées sans le sélectionner ou l’activer.</span><span class="sxs-lookup"><span data-stu-id="737e7-106">The `GetButtonAtPosition` method retrieves the number of the button at the specified coordinates without selecting or activating it.</span></span>

``` syntax
[ iButton = ] MSWebDVD.GetButtonAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="737e7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="737e7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="737e7-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="737e7-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="737e7-109">Spécifie la coordonnée x du pointeur de la souris sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="737e7-109">Specifies the x-coordinate of the mouse pointer as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="737e7-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*PosY*</span><span class="sxs-lookup"><span data-stu-id="737e7-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="737e7-111">Spécifie la coordonnée y du pointeur de la souris sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="737e7-111">Specifies the y-coordinate of the mouse pointer as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="737e7-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="737e7-112">Return Value</span></span>

<span data-ttu-id="737e7-113">Retourne une valeur entière qui spécifie le bouton, le cas échéant, à la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="737e7-113">Returns an integer value specifying the button, if any, at the specified position.</span></span>

## <a name="remarks"></a><span data-ttu-id="737e7-114">Notes</span><span class="sxs-lookup"><span data-stu-id="737e7-114">Remarks</span></span>

<span data-ttu-id="737e7-115">Cette méthode retourne zéro si aucun bouton n’est présent aux coordonnées spécifiées.</span><span class="sxs-lookup"><span data-stu-id="737e7-115">This method returns zero if no button is present at the given coordinates.</span></span> <span data-ttu-id="737e7-116">Utilisez cette méthode lors de l’implémentation de la gestion de souris personnalisée après avoir défini [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) sur **true**.</span><span class="sxs-lookup"><span data-stu-id="737e7-116">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="737e7-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="737e7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="737e7-118">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="737e7-118">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="737e7-119">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="737e7-119">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="737e7-120">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="737e7-120">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="737e7-121">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="737e7-121">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="737e7-122">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="737e7-122">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="737e7-123">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="737e7-123">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



