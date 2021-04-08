---
description: Si le bit de contrôle FixedSize est défini, l’image est rognée ou centrée dans le contrôle sans modifier sa forme ou sa taille.
ms.assetid: fb1ef0ba-5183-4708-a47d-26c83584df6c
title: Attribut de contrôle FixedSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ee044860b79e56998da68dc6ddf4926e9115ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751141"
---
# <a name="fixedsize-control-attribute"></a><span data-ttu-id="5ed5c-103">Attribut de contrôle FixedSize</span><span class="sxs-lookup"><span data-stu-id="5ed5c-103">FixedSize Control Attribute</span></span>

<span data-ttu-id="5ed5c-104">Si le bit de contrôle FixedSize est défini, l’image est rognée ou centrée dans le contrôle sans modifier sa forme ou sa taille.</span><span class="sxs-lookup"><span data-stu-id="5ed5c-104">If the FixedSize Control bit is set, the picture is cropped or centered in the control without changing its shape or size.</span></span>

<span data-ttu-id="5ed5c-105">Si ce bit n’est pas défini, l’image est étirée pour s’ajuster au contrôle.</span><span class="sxs-lookup"><span data-stu-id="5ed5c-105">If this bit is not set the picture is stretched to fit the control.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="5ed5c-106">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="5ed5c-106">Valid Controls</span></span>

[<span data-ttu-id="5ed5c-107">Bitmap</span><span class="sxs-lookup"><span data-stu-id="5ed5c-107">Bitmap</span></span>](bitmap-control.md)

[<span data-ttu-id="5ed5c-108">CheckBox</span><span class="sxs-lookup"><span data-stu-id="5ed5c-108">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="5ed5c-109">Icône</span><span class="sxs-lookup"><span data-stu-id="5ed5c-109">Icon</span></span>](icon-control.md)

[<span data-ttu-id="5ed5c-110">Boutons</span><span class="sxs-lookup"><span data-stu-id="5ed5c-110">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="5ed5c-111">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="5ed5c-111">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="5ed5c-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ed5c-112">Value</span></span>



| <span data-ttu-id="5ed5c-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="5ed5c-113">Decimal</span></span> | <span data-ttu-id="5ed5c-114">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="5ed5c-114">Hexadecimal</span></span> | <span data-ttu-id="5ed5c-115">Constante</span><span class="sxs-lookup"><span data-stu-id="5ed5c-115">Constant</span></span>                            |
|---------|-------------|-------------------------------------|
| <span data-ttu-id="5ed5c-116">1 048 576</span><span class="sxs-lookup"><span data-stu-id="5ed5c-116">1048576</span></span> | <span data-ttu-id="5ed5c-117">0x00100000</span><span class="sxs-lookup"><span data-stu-id="5ed5c-117">0x00100000</span></span>  | <span data-ttu-id="5ed5c-118">**msidbControlAttributesFixedSize**</span><span class="sxs-lookup"><span data-stu-id="5ed5c-118">**msidbControlAttributesFixedSize**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5ed5c-119">Notes</span><span class="sxs-lookup"><span data-stu-id="5ed5c-119">Remarks</span></span>

<span data-ttu-id="5ed5c-120">Pour définir cet attribut sur un contrôle, incluez le bit FixedSize dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="5ed5c-120">To set this attribute on a control, include the FixedSize bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="5ed5c-121">La définition du bit FixedSize n’a aucun effet sur une [case à cocher](checkbox-control.md), un [PUSHBUTTON](pushbutton-control.md)ou un [RadioButtonGroup](radiobuttongroup-control.md) si ni la [bitmap](bitmap-control-attribute.md) ni l' [icône](icon-control-attribute.md) n’a été définie.</span><span class="sxs-lookup"><span data-stu-id="5ed5c-121">Setting the FixedSize bit has no effect on a [CheckBox](checkbox-control.md), [PushButton](pushbutton-control.md), or [RadioButtonGroup](radiobuttongroup-control.md) if neither the [Bitmap](bitmap-control-attribute.md) or the [Icon](icon-control-attribute.md) have been set.</span></span>

<span data-ttu-id="5ed5c-122">La définition du bit FixedSize n’a aucun effet sur un contrôle Icon, ou un bouton de commande associé à une icône, [si les bits](iconsize-control-attribute.md) d’icône ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="5ed5c-122">Setting the FixedSize bit has no effect on an Icon control, or a PushButton associated with an icon, if the [IconSize](iconsize-control-attribute.md) bits is not set.</span></span>

<span data-ttu-id="5ed5c-123">Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="5ed5c-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



