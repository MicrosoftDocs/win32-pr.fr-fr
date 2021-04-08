---
description: Le contrôle Line est une ligne horizontale.
ms.assetid: 8b180b71-1e80-47c0-bb44-d5fcecabaed2
title: Contrôle Line
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba3b7374574e2a0087e7dae8d0ffa9f097be9f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755620"
---
# <a name="line-control"></a><span data-ttu-id="cc424-103">Contrôle Line</span><span class="sxs-lookup"><span data-stu-id="cc424-103">Line Control</span></span>

<span data-ttu-id="cc424-104">Le contrôle Line est une ligne horizontale.</span><span class="sxs-lookup"><span data-stu-id="cc424-104">The Line control is a horizontal line.</span></span>

## <a name="control-attributes"></a><span data-ttu-id="cc424-105">Attributs du contrôle</span><span class="sxs-lookup"><span data-stu-id="cc424-105">Control Attributes</span></span>

<span data-ttu-id="cc424-106">Vous pouvez utiliser les attributs suivants avec ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="cc424-106">You can use the following attributes with this control.</span></span> <span data-ttu-id="cc424-107">Pour modifier la valeur d’un attribut à l’aide d’un événement, abonnez le contrôle à un ControlEvent, dans la [table EventMapping](eventmapping-table.md) et répertoriez l’identificateur de l’attribut dans la colonne d’attribut.</span><span class="sxs-lookup"><span data-stu-id="cc424-107">To change the value of an attribute using an event, subscribe the control to a ControlEvent in the [EventMapping table](eventmapping-table.md) and list the attribute's identifier in the Attribute column.</span></span> <span data-ttu-id="cc424-108">Entrez l’identificateur du ControlEvent, dans la colonne d’événement.</span><span class="sxs-lookup"><span data-stu-id="cc424-108">Enter the identifier of the ControlEvent in the Event column.</span></span>



| <span data-ttu-id="cc424-109">Identificateur d’attribut</span><span class="sxs-lookup"><span data-stu-id="cc424-109">Attribute identifier</span></span>                       | <span data-ttu-id="cc424-110">Bit hexadécimal</span><span class="sxs-lookup"><span data-stu-id="cc424-110">Hexadecimal bit</span></span>                  | <span data-ttu-id="cc424-111">Description</span><span class="sxs-lookup"><span data-stu-id="cc424-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc424-112">Position</span><span class="sxs-lookup"><span data-stu-id="cc424-112">Position</span></span>](position-control-attribute.md) |                                  | <span data-ttu-id="cc424-113">Position du contrôle dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="cc424-113">Position of the control in the dialog box.</span></span> <span data-ttu-id="cc424-114">Entrez la largeur, la hauteur et les coordonnées du contrôle dans la largeur, la hauteur, le X et les colonnes Y de la table de [contrôle](control-table.md) ou de la [table BBControl](bbcontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="cc424-114">Enter the control's width, height, and coordinates of the control's left corner into the Width, Height, X, and Y columns of the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md).</span></span> <span data-ttu-id="cc424-115">Utilisez les [unités d’installation](installer-units.md) pour la longueur et la distance.</span><span class="sxs-lookup"><span data-stu-id="cc424-115">Use [installer units](installer-units.md) for length and distance.</span></span><br/>                                         |
| [<span data-ttu-id="cc424-116">Visible</span><span class="sxs-lookup"><span data-stu-id="cc424-116">Visible</span></span>](visible-control-attribute.md)   | <span data-ttu-id="cc424-117">0x00000000 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cc424-117">0x00000000 0x00000001</span></span><br/> | <span data-ttu-id="cc424-118">Contrôle masqué.</span><span class="sxs-lookup"><span data-stu-id="cc424-118">Hidden control.</span></span> <span data-ttu-id="cc424-119">Contrôle visible.</span><span class="sxs-lookup"><span data-stu-id="cc424-119">Visible control.</span></span><br/> <span data-ttu-id="cc424-120">Incluez ce bit dans le mot de bits de la colonne d’attributs dans la table de [contrôle](control-table.md) ou la [table BBControl](bbcontrol-table.md) pour rendre le contrôle visible ou masqué lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="cc424-120">Include this bit in the bit word of the Attributes column in the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md) to make the control visible or hidden upon its creation.</span></span><br/> <span data-ttu-id="cc424-121">Vous pouvez également masquer ou afficher un contrôle à l’aide de la [table ControlCondition](controlcondition-table.md).</span><span class="sxs-lookup"><span data-stu-id="cc424-121">You can also hide or show a control by using the [ControlCondition table](controlcondition-table.md).</span></span><br/> |
| [<span data-ttu-id="cc424-122">Sunken</span><span class="sxs-lookup"><span data-stu-id="cc424-122">Sunken</span></span>](sunken-control-attribute.md)     | <span data-ttu-id="cc424-123">0x00000000 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cc424-123">0x00000000 0x00000004</span></span><br/> | <span data-ttu-id="cc424-124">Affiche le style visuel par défaut.</span><span class="sxs-lookup"><span data-stu-id="cc424-124">Displays the default visual style.</span></span> <span data-ttu-id="cc424-125">Affiche le contrôle avec une apparence 3D enfoncée.</span><span class="sxs-lookup"><span data-stu-id="cc424-125">Displays the control with a sunken, 3-D look.</span></span><br/> <span data-ttu-id="cc424-126">Incluez ces bits dans le mot de bits dans la colonne attributs de la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="cc424-126">Include these bits in the bit word in the Attributes column of the [Control table](control-table.md).</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="cc424-127">Notes</span><span class="sxs-lookup"><span data-stu-id="cc424-127">Remarks</span></span>

<span data-ttu-id="cc424-128">Ce contrôle peut être créé à partir de la classe statique à l’aide de la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="cc424-128">This control can be created from the STATIC class by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="cc424-129">Il a les styles **SS \_ ETCHEDHORZ** et **SS \_ 3D enfoncé** .</span><span class="sxs-lookup"><span data-stu-id="cc424-129">It has the **SS\_ETCHEDHORZ** and **SS\_SUNKEN** styles.</span></span>

 

 
