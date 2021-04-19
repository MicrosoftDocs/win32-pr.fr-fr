---
description: Spécifie le niveau d’application d’une opération de protection contre la perte de données (DLP) de point de terminaison.
title: Énumération DlpAppEnforceLevel (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpAppEnforceLevel
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d0ccc8d0d39bc4022899deaeb9e8a81eae1f720f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495770"
---
# <a name="dlpappenforcelevel-enumeration"></a><span data-ttu-id="a3e8d-103">Énumération DlpAppEnforceLevel</span><span class="sxs-lookup"><span data-stu-id="a3e8d-103">DlpAppEnforceLevel enumeration</span></span>

<span data-ttu-id="a3e8d-104">Spécifie le niveau d’application d’une opération de protection contre la perte de données (DLP) de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="a3e8d-104">Specifies the enforcement level of an endpoint Data Loss Prevention (DLP) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e8d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3e8d-105">Syntax</span></span>


```C++
typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, 
    DlpAppEnforceLevelNotify,   
    DlpAppEnforceLevelPrevent,   
    DlpAppEnforceLevelFull, 
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;
```


## <a name="constants"></a><span data-ttu-id="a3e8d-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="a3e8d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a3e8d-107">*DlpAppEnforceLevelNone* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a3e8d-107">*DlpAppEnforceLevelNone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e8d-108">Aucune mise en application par l’application.</span><span class="sxs-lookup"><span data-stu-id="a3e8d-108">No enforcement by the app.</span></span> <span data-ttu-id="a3e8d-109">Le système DLP applique l’opération.</span><span class="sxs-lookup"><span data-stu-id="a3e8d-109">The DLP system will enforce the operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="a3e8d-110">*DlpAppEnforceLevelNotify* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a3e8d-110">*DlpAppEnforceLevelNotify* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e8d-111">L’application un utilise les API DLP pour informer le système DLP de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a3e8d-111">Tne app will use the DLP APIs to notify the DLP system about the operation.</span></span> <span data-ttu-id="a3e8d-112">Le système DLP applique l’opération.</span><span class="sxs-lookup"><span data-stu-id="a3e8d-112">The DLP system will enforce the operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="a3e8d-113">*DlpAppEnforceLevelPrevent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a3e8d-113">*DlpAppEnforceLevelPrevent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e8d-114">Non pris en charge dans la version actuelle.</span><span class="sxs-lookup"><span data-stu-id="a3e8d-114">Not supported in the current version.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="a3e8d-115">*DlpAppEnforceLevelFull* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a3e8d-115">*DlpAppEnforceLevelFull* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e8d-116">Non pris en charge dans la version actuelle.</span><span class="sxs-lookup"><span data-stu-id="a3e8d-116">Not supported in the current version.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="a3e8d-117">*DlpAppEnforceLevelCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a3e8d-117">*DlpAppEnforceLevelCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e8d-118">Valeur maximale de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="a3e8d-118">The maximum value of the enumeration.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="a3e8d-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a3e8d-119">Remarks</span></span>

<span data-ttu-id="a3e8d-120">Les valeurs de cette énumération sont utilisées par la structure [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) .</span><span class="sxs-lookup"><span data-stu-id="a3e8d-120">Values from this enumeration are used by the [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structure.</span></span>


## <a name="requirements"></a><span data-ttu-id="a3e8d-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a3e8d-121">Requirements</span></span>



| <span data-ttu-id="a3e8d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3e8d-122">Requirement</span></span>          |    <span data-ttu-id="a3e8d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3e8d-123">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e8d-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3e8d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a3e8d-125">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="a3e8d-125">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

