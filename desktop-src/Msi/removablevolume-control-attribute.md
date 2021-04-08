---
description: Si ce bit est défini, le contrôle affiche tous les volumes impliqués dans l’installation actuelle, ainsi que tous les volumes amovibles. Si ce bit n’est pas défini, le contrôle répertorie les volumes dans l’installation actuelle.
ms.assetid: fc16ca46-54a1-4b24-ba51-8b4d358268f4
title: Attribut de contrôle RemovableVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a91a464eb55ee965f12eae9885849eb2080996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751125"
---
# <a name="removablevolume-control-attribute"></a><span data-ttu-id="a69ad-104">Attribut de contrôle RemovableVolume</span><span class="sxs-lookup"><span data-stu-id="a69ad-104">RemovableVolume Control Attribute</span></span>

<span data-ttu-id="a69ad-105">Si ce bit est défini, le contrôle affiche tous les volumes impliqués dans l’installation actuelle, ainsi que tous les volumes amovibles.</span><span class="sxs-lookup"><span data-stu-id="a69ad-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the removable volumes.</span></span> <span data-ttu-id="a69ad-106">Si ce bit n’est pas défini, le contrôle répertorie les volumes dans l’installation actuelle.</span><span class="sxs-lookup"><span data-stu-id="a69ad-106">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="a69ad-107">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="a69ad-107">Valid Controls</span></span>

[<span data-ttu-id="a69ad-108">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="a69ad-108">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="a69ad-109">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="a69ad-109">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="a69ad-110">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="a69ad-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="a69ad-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="a69ad-111">Value</span></span>



| <span data-ttu-id="a69ad-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="a69ad-112">Decimal</span></span> | <span data-ttu-id="a69ad-113">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="a69ad-113">Hexadecimal</span></span> | <span data-ttu-id="a69ad-114">Constante</span><span class="sxs-lookup"><span data-stu-id="a69ad-114">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="a69ad-115">65536</span><span class="sxs-lookup"><span data-stu-id="a69ad-115">65536</span></span>   | <span data-ttu-id="a69ad-116">0x00010000</span><span class="sxs-lookup"><span data-stu-id="a69ad-116">0x00010000</span></span>  | <span data-ttu-id="a69ad-117">**msidbControlAttributesRemovableVolume**</span><span class="sxs-lookup"><span data-stu-id="a69ad-117">**msidbControlAttributesRemovableVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a69ad-118">Notes</span><span class="sxs-lookup"><span data-stu-id="a69ad-118">Remarks</span></span>

<span data-ttu-id="a69ad-119">Pour définir cet attribut sur un contrôle, incluez le bit RemovableVolume dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="a69ad-119">To set this attribute on a control, include the RemovableVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="a69ad-120">Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="a69ad-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



