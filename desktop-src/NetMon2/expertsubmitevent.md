---
description: La fonction ExpertSubmitEvent indique qu’il existe une condition d’événement et fournit une structure de données qui décrit la condition.
ms.assetid: 2339b530-427b-4028-aef6-c2cdd1353f77
title: ExpertSubmitEvent, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertSubmitEvent
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 448d77e9cb009b8aced0aba752526dc08b503066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318081"
---
# <a name="expertsubmitevent-function"></a><span data-ttu-id="71d07-103">ExpertSubmitEvent fonction)</span><span class="sxs-lookup"><span data-stu-id="71d07-103">ExpertSubmitEvent function</span></span>

<span data-ttu-id="71d07-104">La fonction **ExpertSubmitEvent** indique qu’il existe une condition d’événement et fournit une structure de données qui décrit la condition.</span><span class="sxs-lookup"><span data-stu-id="71d07-104">The **ExpertSubmitEvent** function indicates that an event condition exists and provides a data structure that describes the condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="71d07-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71d07-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertSubmitEvent(
  _In_ HEXPERTKEY   hExpertKey,
  _In_ PNMEVENTDATA pExpertEvent
);
```



## <a name="parameters"></a><span data-ttu-id="71d07-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71d07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71d07-107">*hExpertKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71d07-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71d07-108">Identificateur unique de l’expert.</span><span class="sxs-lookup"><span data-stu-id="71d07-108">Unique identifier of the expert.</span></span> <span data-ttu-id="71d07-109">Moniteur réseau transmet *hExpertKey* à l’expert lorsqu’il appelle la fonction [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="71d07-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="71d07-110">*pExpertEvent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71d07-110">*pExpertEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71d07-111">Pointeur vers une structure **NMEVENTDATA** qui décrit la condition d’événement.</span><span class="sxs-lookup"><span data-stu-id="71d07-111">A pointer to an **NMEVENTDATA** structure that describes the event condition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71d07-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71d07-112">Return value</span></span>

<span data-ttu-id="71d07-113">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="71d07-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="71d07-114">Si la fonction échoue, la valeur de retour indique la raison de l’échec.</span><span class="sxs-lookup"><span data-stu-id="71d07-114">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="71d07-115">Si la valeur de retour est NMERR \_ expert \_ Terminate, l’expert nettoie immédiatement et retourne.</span><span class="sxs-lookup"><span data-stu-id="71d07-115">If the return value is NMERR\_EXPERT\_TERMINATE, the expert immediately cleans up and returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="71d07-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71d07-116">Requirements</span></span>



| <span data-ttu-id="71d07-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71d07-117">Requirement</span></span> | <span data-ttu-id="71d07-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="71d07-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="71d07-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71d07-119">Minimum supported client</span></span><br/> | <span data-ttu-id="71d07-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71d07-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="71d07-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71d07-121">Minimum supported server</span></span><br/> | <span data-ttu-id="71d07-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71d07-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="71d07-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="71d07-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="71d07-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="71d07-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="71d07-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="71d07-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="71d07-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71d07-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="71d07-127">DLL</span><span class="sxs-lookup"><span data-stu-id="71d07-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71d07-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71d07-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




