---
description: Le qualificateur dynamique indique une classe dont les instances sont créées dynamiquement. La valeur de ce qualificateur doit être définie sur TRUE.
ms.assetid: 63286687-abbf-49f0-8061-3b47fba75806
ms.tgt_platform: multiple
title: Qualificateur dynamique
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dynamic
api_type:
- NA
api_location: ''
ms.openlocfilehash: f6530942859c8c3de571ba9ddb94e9b1ce78cc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864022"
---
# <a name="dynamic-qualifier"></a><span data-ttu-id="cc1a4-104">Qualificateur dynamique</span><span class="sxs-lookup"><span data-stu-id="cc1a4-104">Dynamic Qualifier</span></span>

<span data-ttu-id="cc1a4-105">Le qualificateur **dynamique** indique une classe dont les instances sont créées dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="cc1a4-105">The **Dynamic** qualifier indicates a class whose instances are created dynamically.</span></span> <span data-ttu-id="cc1a4-106">La valeur de ce qualificateur doit être définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="cc1a4-106">The value of this qualifier must be set to **TRUE**.</span></span>

<span data-ttu-id="cc1a4-107">Le qualificateur **dynamique** doit être spécifié sur toutes les classes qui contiennent des données et pour lesquelles les instances sont créées dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="cc1a4-107">The **Dynamic** qualifier must be specified on all classes that contain data and for which instances are created dynamically.</span></span> <span data-ttu-id="cc1a4-108">Le qualificateur du [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) est généralement spécifié pour identifier le fournisseur chargé de fournir les données.</span><span class="sxs-lookup"><span data-stu-id="cc1a4-108">The [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is typically also specified to identify the provider responsible for supplying the data.</span></span>

<span data-ttu-id="cc1a4-109">Les classes qui contiennent uniquement des méthodes nécessitant une implémentation ne requièrent pas le qualificateur **dynamique** .</span><span class="sxs-lookup"><span data-stu-id="cc1a4-109">Classes that contain only methods that need implementation do not require the **Dynamic** qualifier.</span></span> <span data-ttu-id="cc1a4-110">Seul le qualificateur du [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) est requis pour spécifier le nom du fournisseur pour fournir l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="cc1a4-110">Only the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is required to specify the name of the provider to supply the implementation.</span></span>

<span data-ttu-id="cc1a4-111">Toutes les classes dérivées d’une classe dynamique doivent être dynamiques.</span><span class="sxs-lookup"><span data-stu-id="cc1a4-111">All classes derived from a dynamic class must be dynamic.</span></span> <span data-ttu-id="cc1a4-112">Vous ne pouvez pas dériver une classe statique à partir d’une classe dynamique.</span><span class="sxs-lookup"><span data-stu-id="cc1a4-112">You cannot derive a static class from a dynamic class.</span></span>

<span data-ttu-id="cc1a4-113">Quand **Dynamic** est spécifié sur une propriété d’une instance, le qualificateur **PropertyContext** doit également être spécifié.</span><span class="sxs-lookup"><span data-stu-id="cc1a4-113">When **Dynamic** is specified on a property of an instance, the **PropertyContext** qualifier must also be specified.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc1a4-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc1a4-114">Requirements</span></span>



| <span data-ttu-id="cc1a4-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc1a4-115">Requirement</span></span> | <span data-ttu-id="cc1a4-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc1a4-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="cc1a4-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc1a4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cc1a4-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc1a4-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="cc1a4-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc1a4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cc1a4-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc1a4-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc1a4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc1a4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc1a4-122">**Qualificateurs WMI standard**</span><span class="sxs-lookup"><span data-stu-id="cc1a4-122">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="cc1a4-123">Qualificateurs WMI</span><span class="sxs-lookup"><span data-stu-id="cc1a4-123">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="cc1a4-124">Ajout d’un qualificateur</span><span class="sxs-lookup"><span data-stu-id="cc1a4-124">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




