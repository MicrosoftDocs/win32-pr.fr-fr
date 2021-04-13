---
description: Si le bit de contrôle FloppyVolume est défini, le contrôle affiche tous les volumes impliqués dans l’installation actuelle, ainsi que tous les volumes de disquette.
ms.assetid: 65e17920-bb2c-4b98-a2dd-ebaee752ed0a
title: Attribut de contrôle FloppyVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70045ee5d6e16fbe1f679eafd83e6d657c9bf6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528185"
---
# <a name="floppyvolume-control-attribute"></a><span data-ttu-id="42a0b-103">Attribut de contrôle FloppyVolume</span><span class="sxs-lookup"><span data-stu-id="42a0b-103">FloppyVolume Control Attribute</span></span>

<span data-ttu-id="42a0b-104">Si le bit de contrôle FloppyVolume est défini, le contrôle affiche tous les volumes impliqués dans l’installation actuelle, ainsi que tous les volumes de disquette.</span><span class="sxs-lookup"><span data-stu-id="42a0b-104">If the FloppyVolume Control bit is set, the control shows all the volumes involved in the current installation plus all the floppy volumes.</span></span>

<span data-ttu-id="42a0b-105">Si ce bit n’est pas défini, le contrôle répertorie les volumes dans l’installation actuelle.</span><span class="sxs-lookup"><span data-stu-id="42a0b-105">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="42a0b-106">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="42a0b-106">Valid Controls</span></span>

[<span data-ttu-id="42a0b-107">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="42a0b-107">DirectoryCombo</span></span>](directorycombo-control.md)

[<span data-ttu-id="42a0b-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="42a0b-108">VolumeCostList</span></span>](volumecostlist-control.md)

[<span data-ttu-id="42a0b-109">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="42a0b-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="42a0b-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="42a0b-110">Value</span></span>



| <span data-ttu-id="42a0b-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="42a0b-111">Decimal</span></span> | <span data-ttu-id="42a0b-112">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="42a0b-112">Hexadecimal</span></span> | <span data-ttu-id="42a0b-113">Constante</span><span class="sxs-lookup"><span data-stu-id="42a0b-113">Constant</span></span>                               |
|---------|-------------|----------------------------------------|
| <span data-ttu-id="42a0b-114">2 097 152</span><span class="sxs-lookup"><span data-stu-id="42a0b-114">2097152</span></span> | <span data-ttu-id="42a0b-115">0x00200000</span><span class="sxs-lookup"><span data-stu-id="42a0b-115">0x00200000</span></span>  | <span data-ttu-id="42a0b-116">**msidbControlAttributesFloppyVolume**</span><span class="sxs-lookup"><span data-stu-id="42a0b-116">**msidbControlAttributesFloppyVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="42a0b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="42a0b-117">Remarks</span></span>

<span data-ttu-id="42a0b-118">Pour définir cet attribut sur un contrôle, incluez le bit FloppyVolume dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="42a0b-118">To set this attribute on a control, include the FloppyVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="42a0b-119">Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="42a0b-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



