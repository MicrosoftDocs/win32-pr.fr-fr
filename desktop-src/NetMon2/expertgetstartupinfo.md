---
description: La fonction ExpertGetStartupInfo récupère les informations de configuration de démarrage de l’expert.
ms.assetid: 15f080ed-50b7-40c6-b283-dbe416a2b0e9
title: ExpertGetStartupInfo, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetStartupInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f34ecc3d0c3eeb085d2a7c0f8c4cb0426663093c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393415"
---
# <a name="expertgetstartupinfo-function"></a><span data-ttu-id="5322c-103">ExpertGetStartupInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="5322c-103">ExpertGetStartupInfo function</span></span>

<span data-ttu-id="5322c-104">La fonction **ExpertGetStartupInfo** récupère les informations de configuration de démarrage de l’expert.</span><span class="sxs-lookup"><span data-stu-id="5322c-104">The **ExpertGetStartupInfo** function retrieves the startup configuration information for the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="5322c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5322c-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertGetStartupInfo(
  _In_  HEXPERTKEY         hExpertKey,
  _Out_ PEXPERTSTARTUPINFO pExpertStartupInfo
);
```



## <a name="parameters"></a><span data-ttu-id="5322c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5322c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5322c-107">*hExpertKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5322c-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5322c-108">Identificateur d’expert unique.</span><span class="sxs-lookup"><span data-stu-id="5322c-108">Unique expert identifier.</span></span> <span data-ttu-id="5322c-109">Moniteur réseau transmet *hExpertKey* à l’expert lorsqu’il appelle la fonction [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="5322c-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="5322c-110">*pExpertStartupInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5322c-110">*pExpertStartupInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5322c-111">Pointeur vers une structure [EXPERTSTARTUPINFO](expertstartupinfo.md) qui contient des informations de démarrage.</span><span class="sxs-lookup"><span data-stu-id="5322c-111">Pointer to an [EXPERTSTARTUPINFO](expertstartupinfo.md) structure that contains startup information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5322c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5322c-112">Return value</span></span>

<span data-ttu-id="5322c-113">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5322c-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5322c-114">Si la fonction échoue, la valeur de retour est NMERR.</span><span class="sxs-lookup"><span data-stu-id="5322c-114">If the function is unsuccessful, the return value is NMERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="5322c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5322c-115">Remarks</span></span>

<span data-ttu-id="5322c-116">La fonction **ExpertGetStartupInfo** est utilisée si l’expert doit déterminer les informations de démarrage utilisées.</span><span class="sxs-lookup"><span data-stu-id="5322c-116">The **ExpertGetStartupInfo** function is used if the expert must determine the startup information that is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="5322c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5322c-117">Requirements</span></span>



| <span data-ttu-id="5322c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5322c-118">Requirement</span></span> | <span data-ttu-id="5322c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5322c-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5322c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5322c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5322c-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5322c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5322c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5322c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5322c-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5322c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5322c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="5322c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5322c-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5322c-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="5322c-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5322c-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="5322c-127"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5322c-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="5322c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5322c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5322c-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5322c-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




