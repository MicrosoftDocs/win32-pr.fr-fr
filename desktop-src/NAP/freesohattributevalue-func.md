---
title: FreeSoHAttributeValue, fonction (NapUtil. h)
description: Libère une structure de données SoHAttributeValue.
ms.assetid: 21647ee6-2ea2-45fd-b1f2-fb1836196f94
keywords:
- FreeSoHAttributeValue fonction NAP
topic_type:
- apiref
api_name:
- FreeSoHAttributeValue
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bd56049eb727554227bd5eb509969f6795670a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033188"
---
# <a name="freesohattributevalue-function"></a><span data-ttu-id="5fcd7-104">FreeSoHAttributeValue fonction)</span><span class="sxs-lookup"><span data-stu-id="5fcd7-104">FreeSoHAttributeValue function</span></span>

> [!Note]  
> <span data-ttu-id="5fcd7-105">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="5fcd7-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5fcd7-106">La fonction **FreeSoHAttributeValue** libère une structure de données [**SoHAttributeValue**](sohattributevalue-union.md) .</span><span class="sxs-lookup"><span data-stu-id="5fcd7-106">The **FreeSoHAttributeValue** function frees an [**SoHAttributeValue**](sohattributevalue-union.md) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fcd7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5fcd7-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeSoHAttributeValue(
  _In_ SoHAttributeType  type,
  _In_ SoHAttributeValue *value
);
```



## <a name="parameters"></a><span data-ttu-id="5fcd7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5fcd7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fcd7-109">*type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5fcd7-109">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fcd7-110">Valeur [**SoHAttributeType**](sohattributetype-enum.md) qui spécifie le type de valeur d’attribut SoH à libérer.</span><span class="sxs-lookup"><span data-stu-id="5fcd7-110">A [**SoHAttributeType**](sohattributetype-enum.md) value that specifies the type of SoH attribute value to free.</span></span>

</dd> <dt>

<span data-ttu-id="5fcd7-111">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5fcd7-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fcd7-112">Pointeur vers le [**SoHAttributeValue**](sohattributevalue-union.md) à libérer.</span><span class="sxs-lookup"><span data-stu-id="5fcd7-112">A pointer to the [**SoHAttributeValue**](sohattributevalue-union.md) to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5fcd7-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5fcd7-113">Remarks</span></span>

<span data-ttu-id="5fcd7-114">Toutes les interfaces COM prises en charge par le système NAP utilisent des règles de gestion de mémoire COM standard et les allocateurs de mémoire COM (**CoTaskMemAlloc** et **CoTaskMemFree**) :</span><span class="sxs-lookup"><span data-stu-id="5fcd7-114">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="5fcd7-115">Les paramètres **in** sont alloués et libérés par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="5fcd7-115">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="5fcd7-116">Les paramètres **out** sont alloués par l’appelé et libérés par l’appelant à l’aide de **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="5fcd7-116">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="5fcd7-117">Les paramètres **in/out** sont alloués par l’appelant, libérés et réalloués par l’appelé, et libérés au final par l’appelant, à l’aide de **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="5fcd7-117">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="5fcd7-118">Toutes les fonctions NAP pour libérer de la mémoire libèrent également tous les pointeurs incorporés.</span><span class="sxs-lookup"><span data-stu-id="5fcd7-118">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fcd7-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5fcd7-119">Requirements</span></span>



| <span data-ttu-id="5fcd7-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5fcd7-120">Requirement</span></span> | <span data-ttu-id="5fcd7-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fcd7-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5fcd7-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fcd7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5fcd7-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fcd7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5fcd7-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fcd7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5fcd7-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fcd7-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5fcd7-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="5fcd7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fcd7-127"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fcd7-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="5fcd7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5fcd7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fcd7-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fcd7-129"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





