---
description: Spécifie si un travail d’impression XPS est dans la phase de mise en file d’attente ou de rendu.
ms.assetid: 14871d29-59e4-45a2-9697-12550c58396c
title: EPrintXPSJobOperation, énumération (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobOperation
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 917993be2af6e7a78afaec1ad4749dadcaebecba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756393"
---
# <a name="eprintxpsjoboperation-enumeration"></a><span data-ttu-id="bb91f-103">Énumération EPrintXPSJobOperation</span><span class="sxs-lookup"><span data-stu-id="bb91f-103">EPrintXPSJobOperation enumeration</span></span>

<span data-ttu-id="bb91f-104">Spécifie si un travail d’impression XPS est dans la phase de mise en file d’attente ou de rendu.</span><span class="sxs-lookup"><span data-stu-id="bb91f-104">Specifies whether an XPS print job is in the spooling or the rendering phase.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb91f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb91f-105">Syntax</span></span>


```C++
typedef enum tagEPrintXPSJobOperation { 
  kJobProduction,
  kJobConsumption
} EPrintXPSJobOperation;
```



## <a name="constants"></a><span data-ttu-id="bb91f-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="bb91f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bb91f-107"><span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kJobProduction**</span><span class="sxs-lookup"><span data-stu-id="bb91f-107"><span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kJobProduction**</span></span>
</dt> <dd>

<span data-ttu-id="bb91f-108">La tâche XPS est en attente.</span><span class="sxs-lookup"><span data-stu-id="bb91f-108">The XPS job is spooling.</span></span>

</dd> <dt>

<span data-ttu-id="bb91f-109"><span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kJobConsumption**</span><span class="sxs-lookup"><span data-stu-id="bb91f-109"><span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kJobConsumption**</span></span>
</dt> <dd>

<span data-ttu-id="bb91f-110">Le travail XPS est en rendu.</span><span class="sxs-lookup"><span data-stu-id="bb91f-110">The XPS job is rendering.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb91f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="bb91f-111">Remarks</span></span>

<span data-ttu-id="bb91f-112">Cette énumération est principalement utilisée comme paramètre pour la fonction [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) .</span><span class="sxs-lookup"><span data-stu-id="bb91f-112">This enumeration is primarily used as a parameter for the [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb91f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb91f-113">Requirements</span></span>



| <span data-ttu-id="bb91f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb91f-114">Requirement</span></span> | <span data-ttu-id="bb91f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb91f-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb91f-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb91f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bb91f-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb91f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="bb91f-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb91f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bb91f-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb91f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bb91f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb91f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb91f-121"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb91f-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




