---
description: Cet attribut spécifie si les fichiers de sauvegarde de restauration sont inclus dans les coûts affichés par le contrôle VolumeCostList.
ms.assetid: a3ed4d8a-170b-4708-afc2-03d2a5b665a3
title: Attribut de contrôle ControlShowRollbackCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7947777a356933ab74051163b6b9b023736dbb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867297"
---
# <a name="controlshowrollbackcost-control-attribute"></a><span data-ttu-id="134ea-103">Attribut de contrôle ControlShowRollbackCost</span><span class="sxs-lookup"><span data-stu-id="134ea-103">ControlShowRollbackCost Control Attribute</span></span>

<span data-ttu-id="134ea-104">Cet attribut spécifie si les fichiers de sauvegarde de restauration sont inclus dans les coûts affichés par le [contrôle VolumeCostList](volumecostlist-control.md).</span><span class="sxs-lookup"><span data-stu-id="134ea-104">This attribute specifies whether or not the rollback backup files are included in the costs displayed by the [VolumeCostList control](volumecostlist-control.md).</span></span>

<span data-ttu-id="134ea-105">Si ce bit est défini et que la propriété [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = P, les fichiers de sauvegarde de restauration sont inclus dans le coût affiché par le [contrôle VolumeCostList](volumecostlist-control.md).</span><span class="sxs-lookup"><span data-stu-id="134ea-105">If this bit is set and [**PROMPTROLLBACKCOST**](promptrollbackcost.md) property = P, the rollback backup files are included in the cost displayed by the [VolumeCostList Control](volumecostlist-control.md).</span></span>

<span data-ttu-id="134ea-106">Si ce bit n’est pas défini et que la propriété [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = P, les fichiers de restauration de sauvegarde ne sont pas inclus dans le coût affiché par le [contrôle VolumeCostList](volumecostlist-control.md).</span><span class="sxs-lookup"><span data-stu-id="134ea-106">If this bit is not set and [**PROMPTROLLBACKCOST**](promptrollbackcost.md) property = P, the rollback backup files are not included in the cost displayed by the [VolumeCostList Control](volumecostlist-control.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="134ea-107">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="134ea-107">Valid Controls</span></span>

[<span data-ttu-id="134ea-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="134ea-108">VolumeCostList</span></span>](volumecostlist-control.md)

## <a name="value"></a><span data-ttu-id="134ea-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="134ea-109">Value</span></span>



| <span data-ttu-id="134ea-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="134ea-110">Decimal</span></span> | <span data-ttu-id="134ea-111">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="134ea-111">Hexadecimal</span></span> | <span data-ttu-id="134ea-112">Constante</span><span class="sxs-lookup"><span data-stu-id="134ea-112">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="134ea-113">4 194 304</span><span class="sxs-lookup"><span data-stu-id="134ea-113">4194304</span></span> | <span data-ttu-id="134ea-114">0x00400000</span><span class="sxs-lookup"><span data-stu-id="134ea-114">0x00400000</span></span>  | <span data-ttu-id="134ea-115">**msidbControlShowRollbackCost**</span><span class="sxs-lookup"><span data-stu-id="134ea-115">**msidbControlShowRollbackCost**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="134ea-116">Notes</span><span class="sxs-lookup"><span data-stu-id="134ea-116">Remarks</span></span>

<span data-ttu-id="134ea-117">Cet attribut de contrôle est ignoré si [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D ou F.</span><span class="sxs-lookup"><span data-stu-id="134ea-117">This control attribute is ignored if [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D or F.</span></span>

<span data-ttu-id="134ea-118">Si [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F, le coût de la restauration, les fichiers de sauvegarde sont inclus.</span><span class="sxs-lookup"><span data-stu-id="134ea-118">If [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F, the cost of the rollback, backup files is included.</span></span>

<span data-ttu-id="134ea-119">Si [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D ou la propriété [**disablerollback**](-disablerollback.md) = 1, le coût de la restauration, les fichiers de sauvegarde ne sont pas inclus.</span><span class="sxs-lookup"><span data-stu-id="134ea-119">If [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D, or [**DISABLEROLLBACK**](-disablerollback.md) property = 1, the cost of the rollback, backup files is not included.</span></span>

 

 



