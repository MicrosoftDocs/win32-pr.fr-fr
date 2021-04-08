---
description: La fonction GetPropertyInfo retourne un pointeur vers les informations de propriété d’un protocole donné.
ms.assetid: f65166ba-1d94-4d65-b9d7-edb84ada0826
title: GetPropertyInfo, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 007332a85f170f865604526199681cad6d68cdcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862006"
---
# <a name="getpropertyinfo-function"></a><span data-ttu-id="833f5-103">GetPropertyInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="833f5-103">GetPropertyInfo function</span></span>

<span data-ttu-id="833f5-104">La fonction **GetPropertyInfo** retourne un pointeur vers les informations de propriété d’un protocole donné.</span><span class="sxs-lookup"><span data-stu-id="833f5-104">The **GetPropertyInfo** function returns a pointer to the property information of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="833f5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="833f5-105">Syntax</span></span>


```C++
LPPROPERTYINFO WINAPI GetPropertyInfo(
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a><span data-ttu-id="833f5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="833f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="833f5-107">*hProperty* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="833f5-107">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="833f5-108">Handle vers une propriété.</span><span class="sxs-lookup"><span data-stu-id="833f5-108">Handle to a property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="833f5-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="833f5-109">Return value</span></span>

<span data-ttu-id="833f5-110">Si la fonction réussit, la valeur de retour est un pointeur désignant la propriété.</span><span class="sxs-lookup"><span data-stu-id="833f5-110">If the function is successful, the return value is a pointer to the property.</span></span>

<span data-ttu-id="833f5-111">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="833f5-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="833f5-112">Notes</span><span class="sxs-lookup"><span data-stu-id="833f5-112">Remarks</span></span>

<span data-ttu-id="833f5-113">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetPropertyInfo** .</span><span class="sxs-lookup"><span data-stu-id="833f5-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPropertyInfo** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="833f5-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="833f5-114">Requirements</span></span>



| <span data-ttu-id="833f5-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="833f5-115">Requirement</span></span> | <span data-ttu-id="833f5-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="833f5-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="833f5-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="833f5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="833f5-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="833f5-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="833f5-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="833f5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="833f5-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="833f5-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="833f5-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="833f5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="833f5-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="833f5-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="833f5-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="833f5-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="833f5-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="833f5-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="833f5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="833f5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="833f5-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="833f5-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




