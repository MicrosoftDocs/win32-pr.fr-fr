---
description: Récupère un handle d’objet pour l’objet spécifié associé au processus spécifié.
ms.assetid: c7b371c3-02c0-4137-ad9d-dd07a74fe2a5
title: ObFindHandleForObject, fonction (Ntosp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObFindHandleForObject
api_type:
- LibDef
api_location:
- Ntoskrnl.lib
- Ntoskrnl.dll
ms.openlocfilehash: 7ba87d05d4264f3bb160bae16053a338e38e2145
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860789"
---
# <a name="obfindhandleforobject-function"></a><span data-ttu-id="d7ca6-103">ObFindHandleForObject fonction)</span><span class="sxs-lookup"><span data-stu-id="d7ca6-103">ObFindHandleForObject function</span></span>

<span data-ttu-id="d7ca6-104">\[Cette fonction est obsolète et peut être modifiée ou non disponible dans les futures versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="d7ca6-104">\[This function is obsolete and may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="d7ca6-105">Évitez d’utiliser cette fonction.\]</span><span class="sxs-lookup"><span data-stu-id="d7ca6-105">Avoid using this function.\]</span></span>

<span data-ttu-id="d7ca6-106">Récupère un handle d’objet pour l’objet spécifié associé au processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="d7ca6-106">Retrieves an object handle for the specified object associated with the specified process.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ca6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7ca6-107">Syntax</span></span>


```C++
BOOLEAN WINAPI ObFindHandleForObject(
  _In_     PEPROCESS Process,
  _In_     PVOID     Object,
  _In_opt_ PVOID     Reserved1,
  _In_opt_ PVOID     Reserved2,
  _Out_    PHANDLE   Handle
);
```



## <a name="parameters"></a><span data-ttu-id="d7ca6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7ca6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7ca6-109">*Processus* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d7ca6-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7ca6-110">Processus.</span><span class="sxs-lookup"><span data-stu-id="d7ca6-110">The process.</span></span> <span data-ttu-id="d7ca6-111">Ce descripteur est retourné par la fonction **IoGetCurrentProcess** ou **PsGetCurrentProcess** .</span><span class="sxs-lookup"><span data-stu-id="d7ca6-111">This handle is returned by the **IoGetCurrentProcess** or **PsGetCurrentProcess** function.</span></span>

</dd> <dt>

<span data-ttu-id="d7ca6-112">*Objet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d7ca6-112">*Object* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7ca6-113">Pointeur vers l’objet.</span><span class="sxs-lookup"><span data-stu-id="d7ca6-113">A pointer to the object.</span></span>

</dd> <dt>

<span data-ttu-id="d7ca6-114">*Reserved1* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d7ca6-114">*Reserved1* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d7ca6-115">Réservé.</span><span class="sxs-lookup"><span data-stu-id="d7ca6-115">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d7ca6-116">*Reserved2* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d7ca6-116">*Reserved2* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d7ca6-117">Réservé.</span><span class="sxs-lookup"><span data-stu-id="d7ca6-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d7ca6-118">*Gérer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d7ca6-118">*Handle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7ca6-119">Handle d’objet.</span><span class="sxs-lookup"><span data-stu-id="d7ca6-119">The object handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7ca6-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7ca6-120">Return value</span></span>

<span data-ttu-id="d7ca6-121">La fonction retourne la **valeur true** si une correspondance est trouvée et la **valeur false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d7ca6-121">The function returns **TRUE** if a match is found and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7ca6-122">Notes</span><span class="sxs-lookup"><span data-stu-id="d7ca6-122">Remarks</span></span>

<span data-ttu-id="d7ca6-123">Cette fonction est disponible dans Ntoskrnl.exe et peut être appelée uniquement à partir du mode noyau.</span><span class="sxs-lookup"><span data-stu-id="d7ca6-123">This function is available in Ntoskrnl.exe and can be called only from kernel mode.</span></span> <span data-ttu-id="d7ca6-124">La bibliothèque d’importation correspondante est disponible via le kit WDK (Windows Driver Kit).</span><span class="sxs-lookup"><span data-stu-id="d7ca6-124">The corresponding import library is available through the Windows Driver Kit (WDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7ca6-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7ca6-125">Requirements</span></span>



| <span data-ttu-id="d7ca6-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7ca6-126">Requirement</span></span> | <span data-ttu-id="d7ca6-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7ca6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ca6-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7ca6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d7ca6-129">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7ca6-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d7ca6-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7ca6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d7ca6-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7ca6-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7ca6-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7ca6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7ca6-133"><dt>Ntosp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7ca6-133"><dt>Ntosp.h</dt></span></span> </dl>      |
| <span data-ttu-id="d7ca6-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d7ca6-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7ca6-135"><dt>Ntoskrnl. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7ca6-135"><dt>Ntoskrnl.lib</dt></span></span> </dl> |



 

 




