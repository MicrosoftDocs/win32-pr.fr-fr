---
description: Représente la classe parente à partir de laquelle toutes les classes de trace d’événements du gestionnaire d’objets sont dérivées.
ms.assetid: 07cfc4a2-c665-4080-bc4b-fe9ec7191fdc
title: ObTrace, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTrace
api_type:
- NA
api_location: ''
ms.openlocfilehash: ca89f58df9f5dd741da5b1fb8572b153c956cd43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757660"
---
# <a name="obtrace-class"></a><span data-ttu-id="f2f86-103">ObTrace, classe</span><span class="sxs-lookup"><span data-stu-id="f2f86-103">ObTrace class</span></span>

<span data-ttu-id="f2f86-104">Représente la classe parente à partir de laquelle toutes les classes de trace d’événements du gestionnaire d’objets sont dérivées.</span><span class="sxs-lookup"><span data-stu-id="f2f86-104">Represents the parent class from which all object manager event trace classes are derived.</span></span>

<span data-ttu-id="f2f86-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f2f86-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2f86-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2f86-106">Syntax</span></span>

``` syntax
[DisplayName("Object"), Dynamic, EventVersion(2), Guid("{89497f50-effe-4440-8cf2-ce6b1cdcaca7}")]
class ObTrace : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="f2f86-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f2f86-107">Members</span></span>

<span data-ttu-id="f2f86-108">La classe **ObTrace** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="f2f86-108">The **ObTrace** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2f86-109">Notes</span><span class="sxs-lookup"><span data-stu-id="f2f86-109">Remarks</span></span>

<span data-ttu-id="f2f86-110">Pour activer le suivi d’événements du gestionnaire d’objets, appelez la fonction [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) avec le paramètre *InformationClass* égal à la valeur d’énumération de la [**\_ \_ classe informations de trace**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) **TraceSystemTraceEnableFlagsInfo** et le membre **EnableFlags** de la structure des [**\_ \_ Propriétés de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) égal au **\_ \_ handle de perf ob** (0x80000040).</span><span class="sxs-lookup"><span data-stu-id="f2f86-110">To enable object manager event tracing, call the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function with the *InformationClass* parameter equal to the [**TRACE\_INFO\_CLASS**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) enumeration value **TraceSystemTraceEnableFlagsInfo** and the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure's **EnableFlags** member equal to **PERF\_OB\_HANDLE** (0x80000040).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2f86-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f2f86-111">Requirements</span></span>



| <span data-ttu-id="f2f86-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2f86-112">Requirement</span></span> | <span data-ttu-id="f2f86-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2f86-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2f86-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2f86-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f2f86-115">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2f86-115">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f2f86-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2f86-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f2f86-117">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2f86-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f2f86-118">MOF</span><span class="sxs-lookup"><span data-stu-id="f2f86-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2f86-119"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2f86-119"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 
