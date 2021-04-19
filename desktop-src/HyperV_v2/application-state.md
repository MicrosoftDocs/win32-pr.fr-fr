---
description: Spécifie l’état d’intégrité d’une application.
ms.assetid: CA06AA34-A549-4CFC-9B52-D2E0B200C3E9
title: Énumération APPLICATION_STATE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPLICATION_STATE
api_type:
- IDLDef
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 4b7e288f41c863dc3f0365db3c6aae867605e5c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527642"
---
# <a name="application_state-enumeration"></a><span data-ttu-id="b6982-103">Énumération de l’état de l’APPLICATION \_</span><span class="sxs-lookup"><span data-stu-id="b6982-103">APPLICATION\_STATE enumeration</span></span>

<span data-ttu-id="b6982-104">Spécifie l’état d’intégrité d’une application.</span><span class="sxs-lookup"><span data-stu-id="b6982-104">Specifies the health state of an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6982-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6982-105">Syntax</span></span>


```C++
typedef enum _APPLICATION_STATE { 
  ApplicationStateHealthy   = 0,
  ApplicationStateCritical
} APPLICATION_STATE, *PAPPLICATION_STATE;
```



## <a name="constants"></a><span data-ttu-id="b6982-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b6982-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b6982-107"><span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**ApplicationStateHealthy**</span><span class="sxs-lookup"><span data-stu-id="b6982-107"><span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**ApplicationStateHealthy**</span></span>
</dt> <dd>

<span data-ttu-id="b6982-108">L’état de l’application est sain.</span><span class="sxs-lookup"><span data-stu-id="b6982-108">The application state is healthy.</span></span>

</dd> <dt>

<span data-ttu-id="b6982-109"><span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**ApplicationStateCritical**</span><span class="sxs-lookup"><span data-stu-id="b6982-109"><span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**ApplicationStateCritical**</span></span>
</dt> <dd>

<span data-ttu-id="b6982-110">L’état de l’application est critique.</span><span class="sxs-lookup"><span data-stu-id="b6982-110">The application state is critical.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6982-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b6982-111">Remarks</span></span>

<span data-ttu-id="b6982-112">Pour utiliser cet élément de programmation, les composants d’intégration Windows 8 doivent être installés sur l’ordinateur virtuel dans lequel l’application s’exécute.</span><span class="sxs-lookup"><span data-stu-id="b6982-112">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6982-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6982-113">Requirements</span></span>



| <span data-ttu-id="b6982-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6982-114">Requirement</span></span> | <span data-ttu-id="b6982-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6982-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6982-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6982-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b6982-117">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6982-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="b6982-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6982-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b6982-119">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6982-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b6982-120">Version</span><span class="sxs-lookup"><span data-stu-id="b6982-120">Version</span></span><br/>                  | <span data-ttu-id="b6982-121">Composants d’intégration pour Windows 8</span><span class="sxs-lookup"><span data-stu-id="b6982-121">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="b6982-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="b6982-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b6982-123"><dt>VmApplicationHealthMonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b6982-123"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6982-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6982-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6982-125">**SetApplicationState**</span><span class="sxs-lookup"><span data-stu-id="b6982-125">**SetApplicationState**</span></span>](ivmapplicationhealthmonitor-setapplicationstate.md)
</dt> </dl>

 

 




