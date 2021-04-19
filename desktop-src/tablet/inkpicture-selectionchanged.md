---
description: Se produit lorsque la sélection d’encre dans le contrôle InkPicture a changé, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de sélection.
ms.assetid: e300ec91-e8f3-473f-b526-efeafafaa32a
title: InkPicture. SelectionChanged, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14594efe4e5ecda64167ec9a0e075fc60d8e9a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530746"
---
# <a name="inkpictureselectionchanged-event"></a><span data-ttu-id="9e6c5-103">InkPicture. SelectionChanged, événement</span><span class="sxs-lookup"><span data-stu-id="9e6c5-103">InkPicture.SelectionChanged event</span></span>

<span data-ttu-id="9e6c5-104">Se produit lorsque la sélection d’encre dans le contrôle [InkPicture](inkpicture-control-reference.md) a changé, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="9e6c5-104">Occurs when the selection of ink within the [InkPicture](inkpicture-control-reference.md) control has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e6c5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e6c5-105">Syntax</span></span>


```C++
void SelectionChanged();
```



## <a name="parameters"></a><span data-ttu-id="9e6c5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e6c5-106">Parameters</span></span>

<span data-ttu-id="9e6c5-107">Cet événement n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="9e6c5-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9e6c5-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e6c5-108">Return value</span></span>

<span data-ttu-id="9e6c5-109">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9e6c5-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e6c5-110">Notes</span><span class="sxs-lookup"><span data-stu-id="9e6c5-110">Remarks</span></span>

<span data-ttu-id="9e6c5-111">Pour plus d’informations sur cet événement, reportez-vous à l’événement [**SelectionChanged**](inkoverlay-selectionchanged.md) de l’objet [**InkOverlay**](inkoverlay-class.md) , qui a la même fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="9e6c5-111">For further details about this event, refer to the [**InkOverlay**](inkoverlay-class.md) object's [**SelectionChanged**](inkoverlay-selectionchanged.md) event, which has the same functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e6c5-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e6c5-112">Requirements</span></span>



| <span data-ttu-id="9e6c5-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e6c5-113">Requirement</span></span> | <span data-ttu-id="9e6c5-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e6c5-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e6c5-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e6c5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9e6c5-116">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9e6c5-116">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9e6c5-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e6c5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9e6c5-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e6c5-118">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9e6c5-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e6c5-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e6c5-120"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9e6c5-120"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9e6c5-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9e6c5-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="9e6c5-122"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e6c5-122"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9e6c5-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e6c5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e6c5-124">InkPicture</span><span class="sxs-lookup"><span data-stu-id="9e6c5-124">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="9e6c5-125">[**Propriété de sélection, \[ contrôle InkPicture\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="9e6c5-125">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> </dl>

 

 




