---
description: Représente le type d’informations dans la structure des informations de l' \_ ensemble d’UC système \_ \_ .
ms.assetid: B42CB8E8-0010-4B11-AB0D-6D196DCCC90A
title: Énumération CPU_SET_INFORMATION_TYPE (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPU_SET_INFORMATION_TYPE
api_type:
- HeaderDef
api_location:
- Processthreadapi.h
ms.openlocfilehash: 0283275856e8e68bf983aaeb9a7660a5a0a6bf59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520558"
---
# <a name="cpu_set_information_type-enumeration"></a><span data-ttu-id="ca508-103">\_ \_ Énumération des types d’informations de jeu d’UC \_</span><span class="sxs-lookup"><span data-stu-id="ca508-103">CPU\_SET\_INFORMATION\_TYPE enumeration</span></span>

<span data-ttu-id="ca508-104">Représente le type d’informations dans la structure des informations de l' [**\_ ensemble d’UC \_ \_ système**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) .</span><span class="sxs-lookup"><span data-stu-id="ca508-104">Represents the type of information in the [**SYSTEM\_CPU\_SET\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca508-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca508-105">Syntax</span></span>


```C++
typedef enum _CPU_SET_INFORMATION_TYPE { 
  CpuSetInformation
} CPU_SET_INFORMATION_TYPE, *PCPU_SET_INFORMATION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="ca508-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ca508-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ca508-107"><span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**CpuSetInformation**</span><span class="sxs-lookup"><span data-stu-id="ca508-107"><span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**CpuSetInformation**</span></span>
</dt> <dd>

<span data-ttu-id="ca508-108">La structure contient des informations sur le jeu d’UC.</span><span class="sxs-lookup"><span data-stu-id="ca508-108">The structure contains CPU Set information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca508-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca508-109">Requirements</span></span>



| <span data-ttu-id="ca508-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca508-110">Requirement</span></span> | <span data-ttu-id="ca508-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca508-111">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca508-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca508-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ca508-113">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca508-113">Windows 10 \[desktop apps only\]</span></span><br/>                                                                       |
| <span data-ttu-id="ca508-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca508-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ca508-115">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca508-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ca508-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca508-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca508-117"><dt>Processthreadsapi. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca508-117"><dt>Processthreadsapi.h (include Windows.h)</dt></span></span> </dl> |



 

 




