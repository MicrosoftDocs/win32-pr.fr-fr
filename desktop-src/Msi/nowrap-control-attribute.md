---
description: Si ce bit est défini, le texte du contrôle est affiché sur une seule ligne. Si le texte s’étend au-delà des marges du contrôle, il est tronqué et des points de suspension (&\# 0034 ;... &\# 0034 ;) est inséré à la fin pour indiquer la troncation. Si ce bit n’est pas défini, le texte est renvoyé à la ligne.
ms.assetid: 0dec3d25-0da7-4054-8d5c-55e81be16489
title: Attribut de contrôle nowrap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ee40b52fbec1c8add841f7055a7f42667eca94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531991"
---
# <a name="nowrap-control-attribute"></a><span data-ttu-id="9faf8-105">Attribut de contrôle nowrap</span><span class="sxs-lookup"><span data-stu-id="9faf8-105">NoWrap Control Attribute</span></span>

<span data-ttu-id="9faf8-106">Si ce bit est défini, le texte du contrôle est affiché sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="9faf8-106">If this bit is set the text in the control is displayed on a single line.</span></span> <span data-ttu-id="9faf8-107">Si le texte s’étend au-delà des marges du contrôle, il est tronqué et des points de suspension (« ... ») sont insérés à la fin pour indiquer la troncation.</span><span class="sxs-lookup"><span data-stu-id="9faf8-107">If the text extends beyond the control's margins it is truncated and an ellipsis ("...") is inserted at the end to indicate the truncation.</span></span> <span data-ttu-id="9faf8-108">Si ce bit n’est pas défini, le texte est renvoyé à la ligne.</span><span class="sxs-lookup"><span data-stu-id="9faf8-108">If this bit is not set, text wraps.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="9faf8-109">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="9faf8-109">Valid Controls</span></span>

[<span data-ttu-id="9faf8-110">Text</span><span class="sxs-lookup"><span data-stu-id="9faf8-110">Text</span></span>](text-control.md)

## <a name="value"></a><span data-ttu-id="9faf8-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="9faf8-111">Value</span></span>



| <span data-ttu-id="9faf8-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="9faf8-112">Decimal</span></span> | <span data-ttu-id="9faf8-113">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="9faf8-113">Hexadecimal</span></span> | <span data-ttu-id="9faf8-114">Constante</span><span class="sxs-lookup"><span data-stu-id="9faf8-114">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="9faf8-115">262 144</span><span class="sxs-lookup"><span data-stu-id="9faf8-115">262144</span></span>  | <span data-ttu-id="9faf8-116">0x00040000</span><span class="sxs-lookup"><span data-stu-id="9faf8-116">0x00040000</span></span>  | <span data-ttu-id="9faf8-117">**msidbControlAttributesNoWrap**</span><span class="sxs-lookup"><span data-stu-id="9faf8-117">**msidbControlAttributesNoWrap**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9faf8-118">Notes</span><span class="sxs-lookup"><span data-stu-id="9faf8-118">Remarks</span></span>

<span data-ttu-id="9faf8-119">Pour définir cet attribut sur un contrôle, incluez le bit nowrap dans la colonne Attributes de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="9faf8-119">To set this attribute on a control, include the NoWrap bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="9faf8-120">Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="9faf8-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



