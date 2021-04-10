---
description: Si ce bit est défini, le contrôle s’affiche avec une apparence 3D enfoncé.
ms.assetid: 00052b01-f2f0-4749-8826-084e5ebb300a
title: Attribut de contrôle enfoncé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c6852a2f32880a427016e41ce9f68314a4a4ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114158"
---
# <a name="sunken-control-attribute"></a><span data-ttu-id="22744-103">Attribut de contrôle enfoncé</span><span class="sxs-lookup"><span data-stu-id="22744-103">Sunken Control Attribute</span></span>

<span data-ttu-id="22744-104">Si ce bit est défini, le contrôle s’affiche avec une apparence 3D enfoncé.</span><span class="sxs-lookup"><span data-stu-id="22744-104">If this bit is set, the control is displayed with a sunken, three dimensional look.</span></span> <span data-ttu-id="22744-105">L’effet de ce bit de style est différent sur les différents contrôles et versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="22744-105">The effect of this style bit is different on different controls and versions of Windows.</span></span> <span data-ttu-id="22744-106">Sur certains contrôles, il n’a aucun effet visible.</span><span class="sxs-lookup"><span data-stu-id="22744-106">On some controls it has no visible effect.</span></span> <span data-ttu-id="22744-107">Si le système ne prend pas en charge l’attribut de contrôle enfoncé, le contrôle est affiché dans le style visuel par défaut.</span><span class="sxs-lookup"><span data-stu-id="22744-107">If the system does not support the Sunken control attribute, the control is displayed in the default visual style.</span></span> <span data-ttu-id="22744-108">Si ce bit n’est pas défini, le contrôle est affiché avec le style visuel par défaut.</span><span class="sxs-lookup"><span data-stu-id="22744-108">If this bit is not set, the control is displayed with the default visual style.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="22744-109">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="22744-109">Valid Controls</span></span>

<span data-ttu-id="22744-110">Tous les contrôles.</span><span class="sxs-lookup"><span data-stu-id="22744-110">All controls.</span></span>

## <a name="value"></a><span data-ttu-id="22744-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="22744-111">Value</span></span>



| <span data-ttu-id="22744-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="22744-112">Decimal</span></span> | <span data-ttu-id="22744-113">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="22744-113">Hexadecimal</span></span> | <span data-ttu-id="22744-114">Constante</span><span class="sxs-lookup"><span data-stu-id="22744-114">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="22744-115">4</span><span class="sxs-lookup"><span data-stu-id="22744-115">4</span></span>       | <span data-ttu-id="22744-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="22744-116">0x00000004</span></span>  | <span data-ttu-id="22744-117">**msidbControlAttributesSunken**</span><span class="sxs-lookup"><span data-stu-id="22744-117">**msidbControlAttributesSunken**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="22744-118">Notes</span><span class="sxs-lookup"><span data-stu-id="22744-118">Remarks</span></span>

<span data-ttu-id="22744-119">Pour définir cet attribut sur un contrôle, incluez le bit enfoncé dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="22744-119">To set this attribute on a control, include the Sunken bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="22744-120">Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="22744-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



