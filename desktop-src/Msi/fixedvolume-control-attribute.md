---
description: Si le bit de contrôle FixedVolume est défini, le contrôle affiche tous les volumes impliqués dans l’installation actuelle, ainsi que tous les disques durs internes fixes.
ms.assetid: e0917a8c-f43a-412d-9b91-9d5f80779f41
title: Attribut de contrôle FixedVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c524bd228d19dbef823df00eff83e34df503a438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863550"
---
# <a name="fixedvolume-control-attribute"></a><span data-ttu-id="714e3-103">Attribut de contrôle FixedVolume</span><span class="sxs-lookup"><span data-stu-id="714e3-103">FixedVolume Control Attribute</span></span>

<span data-ttu-id="714e3-104">Si le bit de contrôle FixedVolume est défini, le contrôle affiche tous les volumes impliqués dans l’installation actuelle, ainsi que tous les disques durs internes fixes.</span><span class="sxs-lookup"><span data-stu-id="714e3-104">If the FixedVolume Control bit is set, the control shows all the volumes involved in the current installation plus all the fixed internal hard drives.</span></span>

<span data-ttu-id="714e3-105">Si ce bit n’est pas défini, le contrôle répertorie les volumes dans l’installation actuelle.</span><span class="sxs-lookup"><span data-stu-id="714e3-105">If this bit is not set, the control lists the volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="714e3-106">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="714e3-106">Valid Controls</span></span>

[<span data-ttu-id="714e3-107">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="714e3-107">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="714e3-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="714e3-108">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="714e3-109">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="714e3-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)



| <span data-ttu-id="714e3-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="714e3-110">Decimal</span></span> | <span data-ttu-id="714e3-111">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="714e3-111">Hexadecimal</span></span> | <span data-ttu-id="714e3-112">Constante</span><span class="sxs-lookup"><span data-stu-id="714e3-112">Constant</span></span>                              |
|---------|-------------|---------------------------------------|
| <span data-ttu-id="714e3-113">131 072</span><span class="sxs-lookup"><span data-stu-id="714e3-113">131072</span></span>  | <span data-ttu-id="714e3-114">0x00020000</span><span class="sxs-lookup"><span data-stu-id="714e3-114">0x00020000</span></span>  | <span data-ttu-id="714e3-115">**msidbControlAttributesFixedVolume**</span><span class="sxs-lookup"><span data-stu-id="714e3-115">**msidbControlAttributesFixedVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="714e3-116">Notes</span><span class="sxs-lookup"><span data-stu-id="714e3-116">Remarks</span></span>

<span data-ttu-id="714e3-117">Pour définir cet attribut sur un contrôle, incluez le bit FixedVolume dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="714e3-117">To set this attribute on a control, include the FixedVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="714e3-118">Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="714e3-118">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



