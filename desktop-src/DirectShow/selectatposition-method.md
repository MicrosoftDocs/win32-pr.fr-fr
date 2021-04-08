---
description: La méthode SelectAtPosition sélectionne le bouton de menu aux coordonnées spécifiées du pointeur de la souris.
ms.assetid: 005ec550-e04c-4dae-aa5d-d79afefe48ed
title: Méthode SelectAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97bc9feaa4855baac75fca0e776a26a6975b235a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746252"
---
# <a name="selectatposition-method"></a><span data-ttu-id="81477-103">Méthode SelectAtPosition</span><span class="sxs-lookup"><span data-stu-id="81477-103">SelectAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="81477-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="81477-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="81477-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="81477-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="81477-106">La `SelectAtPosition` méthode sélectionne le bouton de menu aux coordonnées spécifiées du pointeur de la souris.</span><span class="sxs-lookup"><span data-stu-id="81477-106">The `SelectAtPosition` method selects the menu button at the specified mouse pointer coordinates.</span></span>

``` syntax
MSWebDVD.SelectAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="81477-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81477-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81477-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="81477-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="81477-109">Spécifie la coordonnée x sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="81477-109">Specifies the x-coordinate as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="81477-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*PosY*</span><span class="sxs-lookup"><span data-stu-id="81477-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="81477-111">Spécifie la coordonnée y sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="81477-111">Specifies the y-coordinate as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81477-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="81477-112">Return Value</span></span>

<span data-ttu-id="81477-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="81477-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81477-114">Notes</span><span class="sxs-lookup"><span data-stu-id="81477-114">Remarks</span></span>

<span data-ttu-id="81477-115">Utilisez cette méthode lors de l’implémentation de la gestion de souris personnalisée après avoir défini [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) sur **true**.</span><span class="sxs-lookup"><span data-stu-id="81477-115">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="81477-116">Sélectionnez simplement le bouton.</span><span class="sxs-lookup"><span data-stu-id="81477-116">Selecting merely highlights the button.</span></span> <span data-ttu-id="81477-117">Pour envoyer la commande associée à un bouton qui a été sélectionné, appelez [**ActivateButton**](activatebutton-method.md).</span><span class="sxs-lookup"><span data-stu-id="81477-117">To send the command associated with a button that has been selected, call [**ActivateButton**](activatebutton-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="81477-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81477-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81477-119">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="81477-119">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="81477-120">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="81477-120">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="81477-121">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="81477-121">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="81477-122">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="81477-122">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="81477-123">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="81477-123">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> </dl>

 

 



