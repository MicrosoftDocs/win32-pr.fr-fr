---
description: Sert de classe parente pour les classes qui contrôlent la génération d’événements, tels que les événements de minuterie.
ms.assetid: 381b06e7-2857-4932-9f52-f1d62efa8b79
ms.tgt_platform: multiple
title: Classe __EventGenerator
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventGenerator
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b40524405c3b284e7ec61414e36448cb37afeab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210905"
---
# <a name="__eventgenerator-class"></a><span data-ttu-id="4f6fb-103">\_\_EventGenerator, classe</span><span class="sxs-lookup"><span data-stu-id="4f6fb-103">\_\_EventGenerator class</span></span>

<span data-ttu-id="4f6fb-104">La classe système **\_ \_ EventGenerator** est une classe de base abstraite qui sert de classe parente pour les classes qui contrôlent la génération d’événements, tels que les [événements de minuterie](receiving-a-timed-or-repeating-event.md).</span><span class="sxs-lookup"><span data-stu-id="4f6fb-104">The **\_\_EventGenerator** system class is an abstract base class that serves as a parent class for classes that control the generation of events, such as [timer events](receiving-a-timed-or-repeating-event.md).</span></span>

<span data-ttu-id="4f6fb-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4f6fb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4f6fb-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="4f6fb-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f6fb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f6fb-107">Syntax</span></span>

``` syntax
[abstract]
class __EventGenerator : __IndicationRelated
{
};
```

## <a name="members"></a><span data-ttu-id="4f6fb-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4f6fb-108">Members</span></span>

<span data-ttu-id="4f6fb-109">La classe **\_ \_ EventGenerator** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="4f6fb-109">The **\_\_EventGenerator** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f6fb-110">Notes</span><span class="sxs-lookup"><span data-stu-id="4f6fb-110">Remarks</span></span>

<span data-ttu-id="4f6fb-111">La classe **\_ \_ EventGenerator** est dérivée de [**\_ \_ IndicationRelated**](--indicationrelated.md), qui n’a pas de propriétés.</span><span class="sxs-lookup"><span data-stu-id="4f6fb-111">The **\_\_EventGenerator** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f6fb-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f6fb-112">Requirements</span></span>



| <span data-ttu-id="4f6fb-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f6fb-113">Requirement</span></span> | <span data-ttu-id="4f6fb-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f6fb-114">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4f6fb-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f6fb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4f6fb-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f6fb-116">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4f6fb-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f6fb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4f6fb-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f6fb-118">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="4f6fb-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4f6fb-119">Namespace</span></span><br/>                | <span data-ttu-id="4f6fb-120">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="4f6fb-120">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="4f6fb-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f6fb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f6fb-122">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="4f6fb-122">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="4f6fb-123">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="4f6fb-123">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

