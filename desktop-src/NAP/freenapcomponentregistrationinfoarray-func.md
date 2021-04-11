---
title: FreeNapComponentRegistrationInfoArray, fonction (NapUtil. h)
description: Libère un nombre spécifié de structures de données NapComponentRegistrationInfo à partir d’un tableau.
ms.assetid: 6fcb1394-04dd-4d8a-87f7-6b69b6ef29ff
keywords:
- FreeNapComponentRegistrationInfoArray fonction NAP
topic_type:
- apiref
api_name:
- FreeNapComponentRegistrationInfoArray
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df823ad8086c57a6ee193bd0d58678786cfe325b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105418"
---
# <a name="freenapcomponentregistrationinfoarray-function"></a><span data-ttu-id="ac17b-104">FreeNapComponentRegistrationInfoArray fonction)</span><span class="sxs-lookup"><span data-stu-id="ac17b-104">FreeNapComponentRegistrationInfoArray function</span></span>

> [!Note]  
> <span data-ttu-id="ac17b-105">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="ac17b-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ac17b-106">La fonction **FreeNapComponentRegistrationInfoArray** libère un nombre spécifié de structures de données [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) à partir d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="ac17b-106">The **FreeNapComponentRegistrationInfoArray** function frees a specified number of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structures from an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac17b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac17b-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeNapComponentRegistrationInfoArray(
  _In_ UINT16                       count,
  _In_ NapComponentRegistrationInfo **info
);
```



## <a name="parameters"></a><span data-ttu-id="ac17b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac17b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac17b-109">*nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ac17b-109">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac17b-110">Nombre de structures [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) dans *info* à libérer.</span><span class="sxs-lookup"><span data-stu-id="ac17b-110">The number of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures in *info* to free.</span></span>

</dd> <dt>

<span data-ttu-id="ac17b-111">*informations* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ac17b-111">*info* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac17b-112">Pointeur vers un tableau de structures de données [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) à libérer.</span><span class="sxs-lookup"><span data-stu-id="ac17b-112">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structures to be freed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac17b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ac17b-113">Remarks</span></span>

<span data-ttu-id="ac17b-114">Toutes les interfaces COM prises en charge par le système NAP utilisent des règles de gestion de mémoire COM standard et les allocateurs de mémoire COM (**CoTaskMemAlloc** et **CoTaskMemFree**) :</span><span class="sxs-lookup"><span data-stu-id="ac17b-114">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="ac17b-115">Les paramètres **in** sont alloués et libérés par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="ac17b-115">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="ac17b-116">Les paramètres **out** sont alloués par l’appelé et libérés par l’appelant à l’aide de **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="ac17b-116">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="ac17b-117">Les paramètres **in/out** sont alloués par l’appelant, libérés et réalloués par l’appelé, et libérés au final par l’appelant, à l’aide de **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="ac17b-117">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="ac17b-118">Toutes les fonctions NAP pour libérer de la mémoire libèrent également tous les pointeurs incorporés.</span><span class="sxs-lookup"><span data-stu-id="ac17b-118">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac17b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac17b-119">Requirements</span></span>



| <span data-ttu-id="ac17b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac17b-120">Requirement</span></span> | <span data-ttu-id="ac17b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac17b-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac17b-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac17b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ac17b-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac17b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ac17b-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac17b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ac17b-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac17b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ac17b-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ac17b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac17b-127"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac17b-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="ac17b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ac17b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac17b-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac17b-129"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





