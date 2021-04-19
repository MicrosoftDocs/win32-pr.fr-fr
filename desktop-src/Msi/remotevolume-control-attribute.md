---
description: Si ce bit est défini, le contrôle affiche tous les volumes impliqués dans l’installation actuelle, ainsi que tous les volumes distants. Si ce bit n’est pas défini, le contrôle répertorie les volumes dans l’installation actuelle.
ms.assetid: be70cd86-6aaf-4307-a553-715d6185accd
title: Attribut de contrôle RemoteVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eeabf4ea1f0174700301c23e780d0933f62743f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106530833"
---
# <a name="remotevolume-control-attribute"></a><span data-ttu-id="18530-104">Attribut de contrôle RemoteVolume</span><span class="sxs-lookup"><span data-stu-id="18530-104">RemoteVolume Control Attribute</span></span>

<span data-ttu-id="18530-105">Si ce bit est défini, le contrôle affiche tous les volumes impliqués dans l’installation actuelle, ainsi que tous les volumes distants.</span><span class="sxs-lookup"><span data-stu-id="18530-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the remote volumes.</span></span> <span data-ttu-id="18530-106">Si ce bit n’est pas défini, le contrôle répertorie les volumes dans l’installation actuelle.</span><span class="sxs-lookup"><span data-stu-id="18530-106">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="18530-107">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="18530-107">Valid Controls</span></span>

[<span data-ttu-id="18530-108">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="18530-108">DirectoryCombo</span></span>](directorycombo-control.md)

[<span data-ttu-id="18530-109">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="18530-109">VolumeCostList</span></span>](volumecostlist-control.md)

[<span data-ttu-id="18530-110">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="18530-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="18530-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="18530-111">Value</span></span>



| <span data-ttu-id="18530-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="18530-112">Decimal</span></span> | <span data-ttu-id="18530-113">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="18530-113">Hexadecimal</span></span> | <span data-ttu-id="18530-114">Constante</span><span class="sxs-lookup"><span data-stu-id="18530-114">Constant</span></span>                               |
|---------|-------------|----------------------------------------|
| <span data-ttu-id="18530-115">262 144</span><span class="sxs-lookup"><span data-stu-id="18530-115">262144</span></span>  | <span data-ttu-id="18530-116">0x00040000</span><span class="sxs-lookup"><span data-stu-id="18530-116">0x00040000</span></span>  | <span data-ttu-id="18530-117">**msidbControlAttributesRemoteVolume**</span><span class="sxs-lookup"><span data-stu-id="18530-117">**msidbControlAttributesRemoteVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="18530-118">Notes</span><span class="sxs-lookup"><span data-stu-id="18530-118">Remarks</span></span>

<span data-ttu-id="18530-119">Pour définir cet attribut sur un contrôle, incluez le bit RemoteVolume dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="18530-119">To set this attribute on a control, include the RemoteVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="18530-120">Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="18530-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



