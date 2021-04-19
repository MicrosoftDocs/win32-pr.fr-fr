---
description: L’événement ValidateProductID affecte l’ID de produit complet à la propriété ProductID. Si la validation échoue, cet événement affiche un message d’erreur et une boîte de dialogue modale pour une entrée utilisateur de l’ID de produit.
ms.assetid: 44002cae-154a-4938-a15c-456c293e94fb
title: ValidateProductID ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b86cacfc4561fe9e4d94436724b42a78d3d8792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524486"
---
# <a name="validateproductid-controlevent"></a><span data-ttu-id="89f71-104">ValidateProductID ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="89f71-104">ValidateProductID ControlEvent</span></span>

<span data-ttu-id="89f71-105">L’événement ValidateProductID affecte l’ID de produit complet à la propriété [**ProductID**](productid.md) .</span><span class="sxs-lookup"><span data-stu-id="89f71-105">The ValidateProductID event sets the [**ProductID**](productid.md) property to the full Product ID.</span></span> <span data-ttu-id="89f71-106">Si la validation échoue, cet événement affiche un message d’erreur et une boîte de dialogue modale pour une entrée utilisateur de l’ID de produit.</span><span class="sxs-lookup"><span data-stu-id="89f71-106">If the validation is unsuccessful, then this event puts up an error message and modal dialog box for a user entry of the Product ID.</span></span>

<span data-ttu-id="89f71-107">Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md)ou un [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="89f71-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="89f71-108">Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="89f71-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="89f71-109">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="89f71-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="89f71-110">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="89f71-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="89f71-111">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="89f71-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="89f71-112">Publié par</span><span class="sxs-lookup"><span data-stu-id="89f71-112">Published By</span></span>

<span data-ttu-id="89f71-113">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="89f71-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="89f71-114">Argument</span><span class="sxs-lookup"><span data-stu-id="89f71-114">Argument</span></span>

<span data-ttu-id="89f71-115">Aucun</span><span class="sxs-lookup"><span data-stu-id="89f71-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="89f71-116">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="89f71-116">Action on Subscribers</span></span>

<span data-ttu-id="89f71-117">Aucun</span><span class="sxs-lookup"><span data-stu-id="89f71-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="89f71-118">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="89f71-118">Typical Use</span></span>

<span data-ttu-id="89f71-119">Un contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue modale est lié à cet événement et est utilisé pour vérifier l’entrée de l’ID de produit de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="89f71-119">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event and is used to check the user's entry of the Product ID.</span></span> <span data-ttu-id="89f71-120">Si l’entrée de l’utilisateur est valide, la boîte de dialogue suivante s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="89f71-120">If the user's entry is valid, then the next dialog box will open.</span></span>

 

 



