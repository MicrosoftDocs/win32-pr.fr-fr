---
description: Un fichier d’icône peut contenir plusieurs tailles différentes de la même image d’icône.
ms.assetid: 2d4d3689-a45a-4088-b466-e2b3bf4c8fb5
title: Icon, attribut de contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb615a53c589ebc2ad2cafb8a2ff7dec902865e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034397"
---
# <a name="iconsize-control-attribute"></a><span data-ttu-id="6c04a-103">Icon, attribut de contrôle</span><span class="sxs-lookup"><span data-stu-id="6c04a-103">IconSize Control Attribute</span></span>

<span data-ttu-id="6c04a-104">Un fichier d’icône peut contenir plusieurs tailles différentes de la même image d’icône.</span><span class="sxs-lookup"><span data-stu-id="6c04a-104">An icon file can hold several different sizes of the same icon image.</span></span> <span data-ttu-id="6c04a-105">Ces bits spécifient la taille de l’image d’icône à charger.</span><span class="sxs-lookup"><span data-stu-id="6c04a-105">These bits specify which size of the icon image to load.</span></span> <span data-ttu-id="6c04a-106">Si aucun des bits n’est défini, la première image est chargée.</span><span class="sxs-lookup"><span data-stu-id="6c04a-106">If none of the bits are set, the first image is loaded.</span></span> <span data-ttu-id="6c04a-107">Si seul **msidbControlAttributesIconSize16** est défini, la première image de 16x16 est chargée.</span><span class="sxs-lookup"><span data-stu-id="6c04a-107">If only **msidbControlAttributesIconSize16** is set, the first 16x16 image is loaded.</span></span> <span data-ttu-id="6c04a-108">Si seul le **msidbControlAttributesIconSize32** est défini, la première image 32x32 est chargée.</span><span class="sxs-lookup"><span data-stu-id="6c04a-108">If only the **msidbControlAttributesIconSize32** is set, the first 32x32 image is loaded.</span></span> <span data-ttu-id="6c04a-109">Si **msidbControlAttributesIconSize48** est défini, la première image 48 est chargée.</span><span class="sxs-lookup"><span data-stu-id="6c04a-109">If **msidbControlAttributesIconSize48** is set, the first 48x48 image is loaded.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="6c04a-110">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="6c04a-110">Valid Controls</span></span>

[<span data-ttu-id="6c04a-111">CheckBox</span><span class="sxs-lookup"><span data-stu-id="6c04a-111">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="6c04a-112">Icône</span><span class="sxs-lookup"><span data-stu-id="6c04a-112">Icon</span></span>](icon-control.md)

[<span data-ttu-id="6c04a-113">Boutons</span><span class="sxs-lookup"><span data-stu-id="6c04a-113">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="6c04a-114">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="6c04a-114">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="6c04a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c04a-115">Value</span></span>



| <span data-ttu-id="6c04a-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="6c04a-116">Decimal</span></span> | <span data-ttu-id="6c04a-117">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="6c04a-117">Hexadecimal</span></span> | <span data-ttu-id="6c04a-118">Description</span><span class="sxs-lookup"><span data-stu-id="6c04a-118">Description</span></span>                          |
|---------|-------------|--------------------------------------|
| <span data-ttu-id="6c04a-119">2 097 152</span><span class="sxs-lookup"><span data-stu-id="6c04a-119">2097152</span></span> | <span data-ttu-id="6c04a-120">0x00200000</span><span class="sxs-lookup"><span data-stu-id="6c04a-120">0x00200000</span></span>  | <span data-ttu-id="6c04a-121">**msidbControlAttributesIconSize16**</span><span class="sxs-lookup"><span data-stu-id="6c04a-121">**msidbControlAttributesIconSize16**</span></span> |
| <span data-ttu-id="6c04a-122">4 194 304</span><span class="sxs-lookup"><span data-stu-id="6c04a-122">4194304</span></span> | <span data-ttu-id="6c04a-123">0x00400000</span><span class="sxs-lookup"><span data-stu-id="6c04a-123">0x00400000</span></span>  | <span data-ttu-id="6c04a-124">**msidbControlAttributesIconSize32**</span><span class="sxs-lookup"><span data-stu-id="6c04a-124">**msidbControlAttributesIconSize32**</span></span> |
| <span data-ttu-id="6c04a-125">6291456</span><span class="sxs-lookup"><span data-stu-id="6c04a-125">6291456</span></span> | <span data-ttu-id="6c04a-126">0x00600000</span><span class="sxs-lookup"><span data-stu-id="6c04a-126">0x00600000</span></span>  | <span data-ttu-id="6c04a-127">**msidbControlAttributesIconSize48**</span><span class="sxs-lookup"><span data-stu-id="6c04a-127">**msidbControlAttributesIconSize48**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6c04a-128">Notes</span><span class="sxs-lookup"><span data-stu-id="6c04a-128">Remarks</span></span>

<span data-ttu-id="6c04a-129">Pour définir cet attribut sur un contrôle, incluez les bits d’icône dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="6c04a-129">To set this attribute on a control, include the IconSize bits in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="6c04a-130">Si le bit [FixedSize](fixedsize-control-attribute.md) n’est pas défini, l’image chargée est réduite ou étirée pour s’ajuster au contrôle d’icône.</span><span class="sxs-lookup"><span data-stu-id="6c04a-130">If the [FixedSize](fixedsize-control-attribute.md) bit is not set, the loaded image is shrunk or stretched to fit the icon control.</span></span> <span data-ttu-id="6c04a-131">Si le bit [FixedSize](fixedsize-control-attribute.md) est défini et que l’image chargée est plus petite que le contrôle Icon, l’image est centrée à l’intérieur du contrôle.</span><span class="sxs-lookup"><span data-stu-id="6c04a-131">If the [FixedSize](fixedsize-control-attribute.md) bit is set, and the loaded image is smaller than the icon control, the picture is displayed centered inside the control.</span></span> <span data-ttu-id="6c04a-132">Si le bit [FixedSize](fixedsize-control-attribute.md) est défini et que l’image chargée est plus grande que le contrôle Icon, l’image est réduite pour s’ajuster au contrôle.</span><span class="sxs-lookup"><span data-stu-id="6c04a-132">If the [FixedSize](fixedsize-control-attribute.md) bit is set, and the loaded image is larger than the icon control, the picture is reduced to fit the control.</span></span>

<span data-ttu-id="6c04a-133">Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="6c04a-133">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



