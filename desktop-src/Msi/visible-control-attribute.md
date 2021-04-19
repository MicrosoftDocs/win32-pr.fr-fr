---
description: Si le bit de contrôle visible est défini, le contrôle est visible dans la boîte de dialogue. Si ce bit n’est pas défini, le contrôle est masqué dans la boîte de dialogue. L’état visible ou masqué de l’attribut de contrôle visible peut être modifié ultérieurement par un événement de contrôle.
ms.assetid: 77d3164c-ea8a-4dcf-afd5-02bb2c2568c6
title: Attribut de contrôle visible
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550513f6bd0e40e58694c2c15a9986b5b02f289c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512955"
---
# <a name="visible-control-attribute"></a><span data-ttu-id="ecd64-105">Attribut de contrôle visible</span><span class="sxs-lookup"><span data-stu-id="ecd64-105">Visible Control Attribute</span></span>

<span data-ttu-id="ecd64-106">Si le bit de contrôle visible est défini, le contrôle est visible dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ecd64-106">If the Visible Control bit is set, the control is visible on the dialog box.</span></span> <span data-ttu-id="ecd64-107">Si ce bit n’est pas défini, le contrôle est masqué dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ecd64-107">If this bit is not set, the control is hidden on the dialog box.</span></span> <span data-ttu-id="ecd64-108">L’état visible ou masqué de l’attribut de contrôle visible peut être modifié ultérieurement par un [événement de contrôle](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="ecd64-108">The visible or hidden state of the Visible control attribute can be later changed by a [Control Event](control-events.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="ecd64-109">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="ecd64-109">Valid Controls</span></span>

<span data-ttu-id="ecd64-110">Tous les contrôles.</span><span class="sxs-lookup"><span data-stu-id="ecd64-110">All controls.</span></span>

## <a name="value"></a><span data-ttu-id="ecd64-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecd64-111">Value</span></span>



| <span data-ttu-id="ecd64-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="ecd64-112">Decimal</span></span> | <span data-ttu-id="ecd64-113">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="ecd64-113">Hexadecimal</span></span> | <span data-ttu-id="ecd64-114">Constante</span><span class="sxs-lookup"><span data-stu-id="ecd64-114">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="ecd64-115">1</span><span class="sxs-lookup"><span data-stu-id="ecd64-115">1</span></span>       | <span data-ttu-id="ecd64-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ecd64-116">0x00000001</span></span>  | <span data-ttu-id="ecd64-117">**msidbControlAttributesVisible**</span><span class="sxs-lookup"><span data-stu-id="ecd64-117">**msidbControlAttributesVisible**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ecd64-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ecd64-118">Remarks</span></span>

<span data-ttu-id="ecd64-119">Vous pouvez utiliser la [table ControlCondition](controlcondition-table.md) pour afficher ou masquer un contrôle en fonction de la valeur d’une propriété ou d’une instruction conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="ecd64-119">You can use the [ControlCondition table](controlcondition-table.md) to show or hide a control according to the value of a property or conditional statement.</span></span> <span data-ttu-id="ecd64-120">Vous pouvez également afficher ou masquer un contrôle en abonnant le contrôle à un [ControlEvent,](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="ecd64-120">You can also show or hide a control by subscribing the control to a [ControlEvent](control-events.md).</span></span> <span data-ttu-id="ecd64-121">Entrez l’identificateur de l’attribut dans la colonne d’attribut et l’identificateur de l’événement dans la colonne d’événement de la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="ecd64-121">Enter the attribute's identifier in the Attribute column and the event's identifier in the Event column of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="ecd64-122">Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="ecd64-122">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



