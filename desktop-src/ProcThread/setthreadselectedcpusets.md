---
description: Définit l’affectation de jeux d’UC sélectionnée pour le thread spécifié. Cette assignation remplace l’attribution de processus par défaut, si celle-ci est définie.
ms.assetid: A73F7118-CC4A-45E6-869A-DFF6924D10C8
title: SetThreadSelectedCpuSets, fonction (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: b8b1f7c382d034e804d4ac7e63d58b8ec5853620
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865058"
---
# <a name="setthreadselectedcpusets-function"></a><span data-ttu-id="132a2-104">SetThreadSelectedCpuSets fonction)</span><span class="sxs-lookup"><span data-stu-id="132a2-104">SetThreadSelectedCpuSets function</span></span>

<span data-ttu-id="132a2-105">Définit l’affectation de jeux d’UC sélectionnée pour le thread spécifié.</span><span class="sxs-lookup"><span data-stu-id="132a2-105">Sets the selected CPU Sets assignment for the specified thread.</span></span> <span data-ttu-id="132a2-106">Cette assignation remplace l’attribution de processus par défaut, si celle-ci est définie.</span><span class="sxs-lookup"><span data-stu-id="132a2-106">This assignment overrides the process default assignment, if one is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="132a2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="132a2-107">Syntax</span></span>


```C++
BOOL WINAPI SetThreadSelectedCpuSets(
  _In_       HANDLE Thread,
  _In_ const ULONG  *CpuSetIds,
  _In_       ULONG  CpuSetIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="132a2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="132a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="132a2-109">*Thread* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="132a2-109">*Thread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="132a2-110">Spécifie le thread sur lequel définir l’affectation de l’ensemble d’UC.</span><span class="sxs-lookup"><span data-stu-id="132a2-110">Specifies the thread on which to set the CPU Set assignment.</span></span> <span data-ttu-id="132a2-111">Ce descripteur doit disposer \_ du \_ \_ droit d’accès limité aux informations du thread.</span><span class="sxs-lookup"><span data-stu-id="132a2-111">This handle must have the THREAD\_SET\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="132a2-112">La valeur retournée par [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) peut également être utilisée.</span><span class="sxs-lookup"><span data-stu-id="132a2-112">The value returned by [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) can also be used.</span></span>

</dd> <dt>

<span data-ttu-id="132a2-113">*CpuSetIds* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="132a2-113">*CpuSetIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="132a2-114">Spécifie la liste des ID de jeu d’UC à définir comme l’ensemble d’UC sélectionné du thread.</span><span class="sxs-lookup"><span data-stu-id="132a2-114">Specifies the list of CPU Set IDs to set as the thread selected CPU set.</span></span> <span data-ttu-id="132a2-115">Si la valeur est NULL, l’API efface toutes les affectations, ce qui revient à traiter l’affectation par défaut si elle est définie.</span><span class="sxs-lookup"><span data-stu-id="132a2-115">If this is NULL, the API clears out any assignment, reverting to process default assignment if one is set.</span></span>

</dd> <dt>

<span data-ttu-id="132a2-116">*CpuSetIdCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="132a2-116">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="132a2-117">Spécifie le nombre d’ID dans la liste passée dans l’argument **CpuSetIds** .</span><span class="sxs-lookup"><span data-stu-id="132a2-117">Specifies the number of IDs in the list passed in the **CpuSetIds** argument.</span></span> <span data-ttu-id="132a2-118">Si cette valeur est NULL, la valeur doit être 0.</span><span class="sxs-lookup"><span data-stu-id="132a2-118">If that value is NULL, this should be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="132a2-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="132a2-119">Return value</span></span>

<span data-ttu-id="132a2-120">Cette fonction ne peut pas échouer quand des paramètres valides sont passés.</span><span class="sxs-lookup"><span data-stu-id="132a2-120">This function cannot fail when passed valid parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="132a2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="132a2-121">Requirements</span></span>



| <span data-ttu-id="132a2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="132a2-122">Requirement</span></span> | <span data-ttu-id="132a2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="132a2-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="132a2-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="132a2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="132a2-125">Applications Windows 10 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="132a2-125">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="132a2-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="132a2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="132a2-127">Applications de bureau Windows Server 2016 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="132a2-127">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="132a2-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="132a2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="132a2-129"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="132a2-129"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="132a2-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="132a2-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="132a2-131"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="132a2-131"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="132a2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="132a2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="132a2-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="132a2-133"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

 
