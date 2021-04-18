---
description: Cet attribut spécifie si le contrôle donné est activé ou désactivé. La plupart des contrôles apparaissent gris lorsqu’ils sont désactivés.
ms.assetid: d84b1b55-34e1-4173-b945-39a809014d55
title: Attribut de contrôle activé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb7c5cbbbc12353fc07cf50404a1feae1d98f1b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520457"
---
# <a name="enabled-control-attribute"></a><span data-ttu-id="90a1a-104">Attribut de contrôle activé</span><span class="sxs-lookup"><span data-stu-id="90a1a-104">Enabled Control Attribute</span></span>

<span data-ttu-id="90a1a-105">Cet attribut spécifie si le contrôle donné est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="90a1a-105">This attribute specifies if the given control is enabled or disabled.</span></span> <span data-ttu-id="90a1a-106">La plupart des contrôles apparaissent gris lorsqu’ils sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="90a1a-106">Most controls appear gray when disabled.</span></span>

<span data-ttu-id="90a1a-107">Si ce bit est défini, le contrôle est créé comme activé.</span><span class="sxs-lookup"><span data-stu-id="90a1a-107">If this bit is set, the control is created as enabled.</span></span>

<span data-ttu-id="90a1a-108">Si ce bit n’est pas défini, le contrôle est créé comme étant désactivé.</span><span class="sxs-lookup"><span data-stu-id="90a1a-108">If this bit is not set, the control is created as disabled.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="90a1a-109">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="90a1a-109">Valid Controls</span></span>

<span data-ttu-id="90a1a-110">Tous les contrôles.</span><span class="sxs-lookup"><span data-stu-id="90a1a-110">All controls.</span></span> <span data-ttu-id="90a1a-111">L’apparence de certains contrôles qui ne sont pas associés à une propriété, tels que des bitmaps et des icônes, n’est pas affectée par la définition de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="90a1a-111">The appearance of some controls that are not associated with a property, such as Bitmaps and Icons, are unaffected by setting this attribute.</span></span>

## <a name="value"></a><span data-ttu-id="90a1a-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="90a1a-112">Value</span></span>



| <span data-ttu-id="90a1a-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="90a1a-113">Decimal</span></span> | <span data-ttu-id="90a1a-114">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="90a1a-114">Hexadecimal</span></span> | <span data-ttu-id="90a1a-115">Constante</span><span class="sxs-lookup"><span data-stu-id="90a1a-115">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="90a1a-116">2</span><span class="sxs-lookup"><span data-stu-id="90a1a-116">2</span></span>       | <span data-ttu-id="90a1a-117">0x00000002</span><span class="sxs-lookup"><span data-stu-id="90a1a-117">0x00000002</span></span>  | <span data-ttu-id="90a1a-118">**msidbControlAttributesEnabled**</span><span class="sxs-lookup"><span data-stu-id="90a1a-118">**msidbControlAttributesEnabled**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="90a1a-119">Notes</span><span class="sxs-lookup"><span data-stu-id="90a1a-119">Remarks</span></span>

<span data-ttu-id="90a1a-120">Vous pouvez également utiliser la [table ControlCondition](controlcondition-table.md) pour désactiver ou activer un contrôle en fonction de la valeur d’une propriété ou d’une instruction conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="90a1a-120">You can also use the [ControlCondition table](controlcondition-table.md) to disable or enable a control according to the value of a property or conditional statement.</span></span>

<span data-ttu-id="90a1a-121">Vous pouvez également activer ou désactiver un contrôle en abonnant le contrôle à un [ControlEvent,](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="90a1a-121">You can also enable or disable a control by subscribing the control to a [ControlEvent](control-events.md).</span></span> <span data-ttu-id="90a1a-122">Entrez l’identificateur de l’attribut dans la colonne d’attribut et l’identificateur de l’événement dans la colonne d’événement de la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="90a1a-122">Enter the attribute's identifier in the Attribute column and the event's identifier in the Event column of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="90a1a-123">Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="90a1a-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



