---
description: Si ce bit est défini sur un contrôle de texte, l’occurrence du caractère &\# 0034 ; &&\# 0034 ; dans une chaîne de texte s’affiche comme lui-même. Si ce bit n’est pas défini, le caractère suivant &\# 0034 ; &&\# 0034 ; dans la chaîne de texte est affiché sous la forme d’un caractère de soulignement.
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: NoPrefix (attribut de contrôle)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1e1a0c6da65605efca1aacc4582b34a8f673d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201956"
---
# <a name="noprefix-control-attribute"></a><span data-ttu-id="0242b-104">NoPrefix (attribut de contrôle)</span><span class="sxs-lookup"><span data-stu-id="0242b-104">NoPrefix Control Attribute</span></span>

<span data-ttu-id="0242b-105">Si ce bit est défini sur un contrôle de texte, l’occurrence du caractère « & » dans une chaîne de texte s’affiche comme lui-même.</span><span class="sxs-lookup"><span data-stu-id="0242b-105">If this bit is set on a text control, the occurrence of the character "&" in a text string is displayed as itself.</span></span> <span data-ttu-id="0242b-106">Si ce bit n’est pas défini, le caractère qui suit « & » dans la chaîne de texte est affiché sous la forme d’un caractère de soulignement.</span><span class="sxs-lookup"><span data-stu-id="0242b-106">If this bit is not set, then the character following "&" in the text string is displayed as an underscored character.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="0242b-107">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="0242b-107">Valid Controls</span></span>

[<span data-ttu-id="0242b-108">Text</span><span class="sxs-lookup"><span data-stu-id="0242b-108">Text</span></span>](text-control.md)

## <a name="value"></a><span data-ttu-id="0242b-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="0242b-109">Value</span></span>



| <span data-ttu-id="0242b-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="0242b-110">Decimal</span></span> | <span data-ttu-id="0242b-111">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="0242b-111">Hexadecimal</span></span> | <span data-ttu-id="0242b-112">Constante</span><span class="sxs-lookup"><span data-stu-id="0242b-112">Constant</span></span>                           |
|---------|-------------|------------------------------------|
| <span data-ttu-id="0242b-113">131 072</span><span class="sxs-lookup"><span data-stu-id="0242b-113">131072</span></span>  | <span data-ttu-id="0242b-114">0x20000</span><span class="sxs-lookup"><span data-stu-id="0242b-114">0x20000</span></span>     | <span data-ttu-id="0242b-115">**msidbControlAttributesNoPrefix**</span><span class="sxs-lookup"><span data-stu-id="0242b-115">**msidbControlAttributesNoPrefix**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0242b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0242b-116">Remarks</span></span>

<span data-ttu-id="0242b-117">Pour définir cet attribut sur un contrôle, incluez le bit de préfixe dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="0242b-117">To set this attribute on a control, include the NoPrefix bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="0242b-118">Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="0242b-118">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



