---
description: Cette section contient des méthodes pour le contrôle InkPicture.
ms.assetid: 5691e595-f264-4547-9db6-f984483005e8
title: Méthodes InkPicture
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b28d15c61105e9cb5aa690860a0362aac826f019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320934"
---
# <a name="inkpicture-methods"></a><span data-ttu-id="1efc1-103">Méthodes InkPicture</span><span class="sxs-lookup"><span data-stu-id="1efc1-103">InkPicture Methods</span></span>

<span data-ttu-id="1efc1-104">Cette section contient des méthodes pour le contrôle InkPicture.</span><span class="sxs-lookup"><span data-stu-id="1efc1-104">This section contains Methods for the InkPicture Control.</span></span>



| <span data-ttu-id="1efc1-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="1efc1-105">Method</span></span>                                                                                   | <span data-ttu-id="1efc1-106">Description</span><span class="sxs-lookup"><span data-stu-id="1efc1-106">Description</span></span>                                                                                                                                                                      |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1efc1-107">**Méthode GetEventInterest**</span><span class="sxs-lookup"><span data-stu-id="1efc1-107">**GetEventInterest Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-geteventinterest)                           | <span data-ttu-id="1efc1-108">Récupère une valeur qui indique si le contrôle [InkPicture](inkpicture-control-reference.md) s’intéresse à un événement particulier.</span><span class="sxs-lookup"><span data-stu-id="1efc1-108">Retrieves a value that indicates whether the [InkPicture](inkpicture-control-reference.md) control has interest in a particular event.</span></span><br/>                               |
| [<span data-ttu-id="1efc1-109">**GetGestureStatus**</span><span class="sxs-lookup"><span data-stu-id="1efc1-109">**GetGestureStatus**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getgesturestatus)                                  | <span data-ttu-id="1efc1-110">Récupère une valeur qui indique si le contrôle [InkPicture](inkpicture-control-reference.md) présente un intérêt pour un mouvement d’application particulier.</span><span class="sxs-lookup"><span data-stu-id="1efc1-110">Retrieves a value that indicates whether the [InkPicture](inkpicture-control-reference.md) control has interest in a particular application gesture.</span></span><br/>                 |
| [<span data-ttu-id="1efc1-111">**Méthode GetWindowInputRectangle**</span><span class="sxs-lookup"><span data-stu-id="1efc1-111">**GetWindowInputRectangle Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getwindowinputrectangle)             | <span data-ttu-id="1efc1-112">Retourne le rectangle de la fenêtre, en pixels, au sein duquel l’encre est dessinée.</span><span class="sxs-lookup"><span data-stu-id="1efc1-112">Returns the window rectangle, in pixels, within which ink is drawn.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="1efc1-113">**HitTestSelection**</span><span class="sxs-lookup"><span data-stu-id="1efc1-113">**HitTestSelection**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-hittestselection)                                  | <span data-ttu-id="1efc1-114">Récupère un membre de l’énumération [**SelectionHitResult**](/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult) , qui spécifie la partie d’une sélection qui, le cas échéant, a été atteinte pendant un test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="1efc1-114">Retrieves a member of the [**SelectionHitResult**](/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult) enumeration, which specifies which part of a selection, if any, was hit during a hit test.</span></span><br/> |
| [<span data-ttu-id="1efc1-115">**Méthode SetAllTabletsMode**</span><span class="sxs-lookup"><span data-stu-id="1efc1-115">**SetAllTabletsMode Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode)                         | <span data-ttu-id="1efc1-116">Permet au contrôle [InkPicture](inkpicture-control-reference.md) de collecter de l’encre à partir de n’importe quelle tablette attachée au Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="1efc1-116">Enables the [InkPicture](inkpicture-control-reference.md) control to collect ink from any tablet attached to the Tablet PC.</span></span><br/>                                          |
| [<span data-ttu-id="1efc1-117">**Méthode SetEventInterest**</span><span class="sxs-lookup"><span data-stu-id="1efc1-117">**SetEventInterest Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-seteventinterest)                           | <span data-ttu-id="1efc1-118">Modifie une valeur qui indique si un contrôle [InkPicture](inkpicture-control-reference.md) présente un intérêt dans un événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="1efc1-118">Modifies a value that indicates whether an [InkPicture](inkpicture-control-reference.md) control has interest in a specified event.</span></span><br/>                                  |
| [<span data-ttu-id="1efc1-119">**Méthode SetGestureStatus**</span><span class="sxs-lookup"><span data-stu-id="1efc1-119">**SetGestureStatus Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)                           | <span data-ttu-id="1efc1-120">Modifie l’intérêt de l’objet [InkPicture](inkpicture-control-reference.md) dans un mouvement d’application spécifié.</span><span class="sxs-lookup"><span data-stu-id="1efc1-120">Modifies the interest of the [InkPicture](inkpicture-control-reference.md) object in a specified application gesture.</span></span><br/>                                                |
| [<span data-ttu-id="1efc1-121">**Méthode SetSingleTabletIntegratedMode**</span><span class="sxs-lookup"><span data-stu-id="1efc1-121">**SetSingleTabletIntegratedMode Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setsingletabletintegratedmode) | <span data-ttu-id="1efc1-122">Modifie le contrôle [InkPicture](inkpicture-control-reference.md) pour collecter l’encre à partir d’une seule tablette attachée au Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="1efc1-122">Modifies the [InkPicture](inkpicture-control-reference.md) control to collect ink from only one tablet attached to the Tablet PC.</span></span> <span data-ttu-id="1efc1-123">L’encre d’autres tablettes est ignorée.</span><span class="sxs-lookup"><span data-stu-id="1efc1-123">Ink from other tablets is ignored.</span></span><br/> |
| [<span data-ttu-id="1efc1-124">**Méthode SetWindowInputRectangle**</span><span class="sxs-lookup"><span data-stu-id="1efc1-124">**SetWindowInputRectangle Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setwindowinputrectangle)             | <span data-ttu-id="1efc1-125">Spécifie le rectangle de la fenêtre à définir, en coordonnées de la fenêtre, dans laquelle l’encre est dessinée.</span><span class="sxs-lookup"><span data-stu-id="1efc1-125">Specifies the window rectangle to set, in window coordinates, within which ink is drawn.</span></span><br/>                                                                              |



 

 

 




