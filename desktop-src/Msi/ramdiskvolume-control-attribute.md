---
description: Si ce bit est défini, le contrôle affiche tous les volumes impliqués dans l’installation actuelle, ainsi que tous les volumes de disque RAM. Si ce bit n’est pas défini, le contrôle répertorie les volumes dans l’installation actuelle.
ms.assetid: 52526f39-26fb-4a67-a95f-77f7eb761372
title: Attribut de contrôle RAMDiskVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4324af143bab619c6f881925586186be45b44a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518465"
---
# <a name="ramdiskvolume-control-attribute"></a><span data-ttu-id="35564-104">Attribut de contrôle RAMDiskVolume</span><span class="sxs-lookup"><span data-stu-id="35564-104">RAMDiskVolume Control Attribute</span></span>

<span data-ttu-id="35564-105">Si ce bit est défini, le contrôle affiche tous les volumes impliqués dans l’installation actuelle, ainsi que tous les volumes de disque RAM.</span><span class="sxs-lookup"><span data-stu-id="35564-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the RAM disk volumes.</span></span> <span data-ttu-id="35564-106">Si ce bit n’est pas défini, le contrôle répertorie les volumes dans l’installation actuelle.</span><span class="sxs-lookup"><span data-stu-id="35564-106">If this bit is not set the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="35564-107">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="35564-107">Valid Controls</span></span>

[<span data-ttu-id="35564-108">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="35564-108">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="35564-109">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="35564-109">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="35564-110">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="35564-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="35564-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="35564-111">Value</span></span>



| <span data-ttu-id="35564-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="35564-112">Decimal</span></span> | <span data-ttu-id="35564-113">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="35564-113">Hexadecimal</span></span> | <span data-ttu-id="35564-114">Constante</span><span class="sxs-lookup"><span data-stu-id="35564-114">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="35564-115">1048567</span><span class="sxs-lookup"><span data-stu-id="35564-115">1048567</span></span> | <span data-ttu-id="35564-116">0x00100000</span><span class="sxs-lookup"><span data-stu-id="35564-116">0x00100000</span></span>  | <span data-ttu-id="35564-117">**msidbControlAttributesRAMDiskVolume**</span><span class="sxs-lookup"><span data-stu-id="35564-117">**msidbControlAttributesRAMDiskVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="35564-118">Notes</span><span class="sxs-lookup"><span data-stu-id="35564-118">Remarks</span></span>

<span data-ttu-id="35564-119">Pour définir cet attribut sur un contrôle, incluez le bit RAMDiskVolume dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="35564-119">To set this attribute on a control, include the RAMDiskVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="35564-120">Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="35564-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



