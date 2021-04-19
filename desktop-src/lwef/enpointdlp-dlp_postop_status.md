---
description: Spécifie les informations d’État relatives à une opération DLP de point de terminaison.
title: Structure DLP_POSTOP_STATUS (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_POSTOP_STATUS
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: c0221926700fc8960de5ef4d25c36136c3fc9737
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495440"
---
# <a name="dlp_postop_status-structure"></a><span data-ttu-id="1eeac-103">Structure DLP_POSTOP_STATUS</span><span class="sxs-lookup"><span data-stu-id="1eeac-103">DLP_POSTOP_STATUS structure</span></span>

<span data-ttu-id="1eeac-104">Spécifie les informations d’État relatives à une opération DLP de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1eeac-104">Specifies status information about an endpoint DLP operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eeac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1eeac-105">Syntax</span></span>


```C++
typedef struct _DLP_POSTOP_STATUS {
    
    DWORD Version;    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS; 
```


## <a name="members"></a><span data-ttu-id="1eeac-106">Membres</span><span class="sxs-lookup"><span data-stu-id="1eeac-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1eeac-107">*Version* \[ de dans\]</span><span class="sxs-lookup"><span data-stu-id="1eeac-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eeac-108">Valeur DWORD spécifiant la version de l’API.</span><span class="sxs-lookup"><span data-stu-id="1eeac-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="1eeac-109">Cette valeur doit toujours être **DLP_POSTOP_STATUS_V_LATEST**.</span><span class="sxs-lookup"><span data-stu-id="1eeac-109">This value should always be **DLP_POSTOP_STATUS_V_LATEST**.</span></span> <span data-ttu-id="1eeac-110">Cette constante est définie dans la liste des fichiers d’en-tête de l’exemple endpointdlp. h dans l’article [protection contre la perte de données](endpointdlp-endpoint-data-loss-prevention.md)</span><span class="sxs-lookup"><span data-stu-id="1eeac-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md)</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="1eeac-111">*OperationSuccess* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eeac-111">*OperationSuccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eeac-112">Valeur BOOLÉENNE indiquant si l’opération d’ouverture a réussi.</span><span class="sxs-lookup"><span data-stu-id="1eeac-112">A BOOL indicating whether the open operation was successful.</span></span>

</dd> </dl>





## <a name="remarks"></a><span data-ttu-id="1eeac-113">Notes</span><span class="sxs-lookup"><span data-stu-id="1eeac-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="1eeac-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1eeac-114">Requirements</span></span>



| <span data-ttu-id="1eeac-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1eeac-115">Requirement</span></span>          |    <span data-ttu-id="1eeac-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1eeac-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1eeac-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1eeac-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1eeac-118">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="1eeac-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
