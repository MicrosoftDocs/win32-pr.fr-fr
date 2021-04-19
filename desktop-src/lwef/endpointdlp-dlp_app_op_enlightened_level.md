---
description: Associe une action de protection contre la perte de données (DLP) au niveau de l’application.
title: Structure DLP_APP_OP_ENLIGHTENED_LEVEL (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_APP_OP_ENLIGHTENED_LEVEL
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 2d9c1aa8335078cad71832c6090cada1669641cb
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495786"
---
# <a name="dlp_app_op_enlightened_level-structure"></a><span data-ttu-id="58e97-103">Structure DLP_APP_OP_ENLIGHTENED_LEVEL</span><span class="sxs-lookup"><span data-stu-id="58e97-103">DLP_APP_OP_ENLIGHTENED_LEVEL structure</span></span>

<span data-ttu-id="58e97-104">Associe une action de protection contre la perte de données (DLP) au niveau de l’application.</span><span class="sxs-lookup"><span data-stu-id="58e97-104">Associates an endpoint Data Loss Prevention (DLP) action with an enforcement level.</span></span>

## <a name="syntax"></a><span data-ttu-id="58e97-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58e97-105">Syntax</span></span>


```C++
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;
```


## <a name="members"></a><span data-ttu-id="58e97-106">Membres</span><span class="sxs-lookup"><span data-stu-id="58e97-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="58e97-107">*Opération* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58e97-107">*Operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58e97-108">Valeur de l’énumération [DlpActionType](endpointdlp-dlpactiontype.md) qui spécifie le type d’action DLP de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="58e97-108">A value from the [DlpActionType](endpointdlp-dlpactiontype.md) enumeration specifying the endpoint DLP action type.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="58e97-109">*AppEnforcementLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58e97-109">*AppEnforcementLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58e97-110">Valeur de [DlpAppEnforceLevel](endpointdlp-dlpappenforcelevel.md) qui spécifie le niveau de mise en application pour le type d’action DLP de point de terminaison associé.</span><span class="sxs-lookup"><span data-stu-id="58e97-110">A value from the [DlpAppEnforceLevel](endpointdlp-dlpappenforcelevel.md) specifying the level of enforcement for the associated endpoint DLP action type.</span></span>

</dd> </dl>





## <a name="remarks"></a><span data-ttu-id="58e97-111">Notes</span><span class="sxs-lookup"><span data-stu-id="58e97-111">Remarks</span></span>

<span data-ttu-id="58e97-112">Transmettez un tableau de ces structures dans [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md) pour définir le mode de mise en application pour un ensemble d’opérations DLP de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="58e97-112">Pass an array of these structures into [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md) to set the enforcement mode for a set of endpoint DLP operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="58e97-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="58e97-113">Requirements</span></span>



| <span data-ttu-id="58e97-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58e97-114">Requirement</span></span>          |    <span data-ttu-id="58e97-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="58e97-115">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58e97-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58e97-116">Minimum supported client</span></span><br/> | <span data-ttu-id="58e97-117">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="58e97-117">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

