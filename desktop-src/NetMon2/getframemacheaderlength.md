---
description: La fonction GetFrameMacHeaderLength retourne la longueur, en octets, de l’en-tête MAC du frame.
ms.assetid: 4a0f6a8c-04e0-47cb-abd1-b4011cd2d062
title: GetFrameMacHeaderLength, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacHeaderLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4d11a0efac2086884e984edae986720ef704cf81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106530828"
---
# <a name="getframemacheaderlength-function"></a><span data-ttu-id="5f8e0-103">GetFrameMacHeaderLength fonction)</span><span class="sxs-lookup"><span data-stu-id="5f8e0-103">GetFrameMacHeaderLength function</span></span>

<span data-ttu-id="5f8e0-104">La fonction **GetFrameMacHeaderLength** retourne la longueur, en octets, de l’en-tête Mac du frame.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-104">The **GetFrameMacHeaderLength** function returns the length, in bytes, of the MAC header of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f8e0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f8e0-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameMacHeaderLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="5f8e0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f8e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f8e0-107">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f8e0-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f8e0-108">Handle vers le frame.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f8e0-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f8e0-109">Return value</span></span>

<span data-ttu-id="5f8e0-110">Si la fonction réussit, la valeur de retour est la longueur en octets de l’en-tête MAC.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-110">If the function is successful, the return value is the length   in bytes   of the MAC header.</span></span>

<span data-ttu-id="5f8e0-111">Si la fonction échoue, ou si un type MAC inconnu est rencontré, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-111">If the function is not successful, or an unknown MAC type is encountered, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f8e0-112">Notes</span><span class="sxs-lookup"><span data-stu-id="5f8e0-112">Remarks</span></span>

<span data-ttu-id="5f8e0-113">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrameMacHeaderLength** .</span><span class="sxs-lookup"><span data-stu-id="5f8e0-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameMacHeaderLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f8e0-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f8e0-114">Requirements</span></span>



| <span data-ttu-id="5f8e0-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f8e0-115">Requirement</span></span> | <span data-ttu-id="5f8e0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f8e0-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5f8e0-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f8e0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5f8e0-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f8e0-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5f8e0-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f8e0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5f8e0-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f8e0-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5f8e0-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f8e0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f8e0-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f8e0-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="5f8e0-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5f8e0-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="5f8e0-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f8e0-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="5f8e0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5f8e0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f8e0-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f8e0-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




