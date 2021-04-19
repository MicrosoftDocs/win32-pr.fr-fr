---
title: booléen (WMI)
description: Est un \_ paramètre VT bool qui prend la valeur de la variante \_ TRUE (&\# 8211 ; 1) ou la variante \_ false (0).
ms.assetid: 3928ff39-ed17-4a61-bb72-a3c9be16ae45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569f7ce633bfb70fdba5e7055a80ad73ebd0fb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522159"
---
# <a name="boolean-wmi"></a><span data-ttu-id="a6205-103">booléen (WMI)</span><span class="sxs-lookup"><span data-stu-id="a6205-103">boolean (WMI)</span></span>

<span data-ttu-id="a6205-104">Le type de données Boolean est un \_ paramètre VT bool qui prend la valeur de la variante \_ true (– 1) ou de la variante \_ false (0).</span><span class="sxs-lookup"><span data-stu-id="a6205-104">The boolean data type is a VT\_BOOL parameter that takes on the value of VARIANT\_TRUE (–1) or VARIANT\_FALSE (0).</span></span> <span data-ttu-id="a6205-105">Le tableau suivant répertorie la différence entre les représentations de programmation de la **valeur logique true** en C/C++ et le type Automation.</span><span class="sxs-lookup"><span data-stu-id="a6205-105">The following table lists the difference between the programmatic representations of logical **TRUE** in C/C++ and the Automation type.</span></span>

| <span data-ttu-id="a6205-106">Language</span><span class="sxs-lookup"><span data-stu-id="a6205-106">Language</span></span>   | <span data-ttu-id="a6205-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6205-107">Value</span></span>         | <span data-ttu-id="a6205-108">Valeur numérique</span><span class="sxs-lookup"><span data-stu-id="a6205-108">Numerical value</span></span> |
|------------|---------------|-----------------|
| <span data-ttu-id="a6205-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="a6205-109">C/C++</span></span>      | <span data-ttu-id="a6205-110">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a6205-110">**TRUE**</span></span>      | <span data-ttu-id="a6205-111">1</span><span class="sxs-lookup"><span data-stu-id="a6205-111">1</span></span>               |
| <span data-ttu-id="a6205-112">Automatisation</span><span class="sxs-lookup"><span data-stu-id="a6205-112">Automation</span></span> | <span data-ttu-id="a6205-113">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="a6205-113">VARIANT\_TRUE</span></span> | <span data-ttu-id="a6205-114">–1</span><span class="sxs-lookup"><span data-stu-id="a6205-114">–1</span></span>              |

<span data-ttu-id="a6205-115">Les deux types sont différents de zéro et, par conséquent, n’ont pas la valeur **false**, mais ont des représentations différentes pour **true**.</span><span class="sxs-lookup"><span data-stu-id="a6205-115">Both types are nonzero and therefore not **FALSE**, but have different representations for **TRUE**.</span></span>
