---
description: Si le bit de contrôle CDROMVolume est défini, le contrôle affiche tous les volumes de l’installation actuelle, ainsi que tous les volumes CD-ROM.
ms.assetid: 233df659-413d-416e-a3d7-d05a67e9bd73
title: Attribut de contrôle CDROMVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a687cfd52f347d9bfd24e74fb10b15f865e13b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106541204"
---
# <a name="cdromvolume-control-attribute"></a><span data-ttu-id="8cf5a-103">Attribut de contrôle CDROMVolume</span><span class="sxs-lookup"><span data-stu-id="8cf5a-103">CDROMVolume Control Attribute</span></span>

<span data-ttu-id="8cf5a-104">Si le bit de contrôle CDROMVolume est défini, le contrôle affiche tous les volumes de l’installation actuelle, ainsi que tous les volumes CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-104">If the CDROMVolume Control bit is set, the control shows all the volumes in the current installation plus all the CD-ROM volumes.</span></span>

<span data-ttu-id="8cf5a-105">Si ce bit n’est pas défini, le contrôle affiche tous les volumes de l’installation actuelle.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-105">If this bit is not set, the control shows all the volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="8cf5a-106">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="8cf5a-106">Valid Controls</span></span>

[<span data-ttu-id="8cf5a-107">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="8cf5a-107">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="8cf5a-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="8cf5a-108">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="8cf5a-109">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="8cf5a-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="8cf5a-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="8cf5a-110">Value</span></span>



| <span data-ttu-id="8cf5a-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="8cf5a-111">Decimal</span></span> | <span data-ttu-id="8cf5a-112">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="8cf5a-112">Hexadecimal</span></span> | <span data-ttu-id="8cf5a-113">Constante</span><span class="sxs-lookup"><span data-stu-id="8cf5a-113">Constant</span></span>                              |
|---------|-------------|---------------------------------------|
| <span data-ttu-id="8cf5a-114">524 288</span><span class="sxs-lookup"><span data-stu-id="8cf5a-114">524288</span></span>  | <span data-ttu-id="8cf5a-115">0x00080000</span><span class="sxs-lookup"><span data-stu-id="8cf5a-115">0x00080000</span></span>  | <span data-ttu-id="8cf5a-116">**msidbControlAttributesCDROMVolume**</span><span class="sxs-lookup"><span data-stu-id="8cf5a-116">**msidbControlAttributesCDROMVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8cf5a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8cf5a-117">Remarks</span></span>

<span data-ttu-id="8cf5a-118">Pour définir cet attribut sur un contrôle, incluez le bit CDROMVolume dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="8cf5a-118">To set this attribute on a control, include the CDROMVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="8cf5a-119">Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="8cf5a-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



