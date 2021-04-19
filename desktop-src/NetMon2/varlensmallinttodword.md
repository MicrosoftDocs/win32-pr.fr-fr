---
description: La fonction VarLenSmallIntToDword convertit un petit entier de longueur variable en valeur DWORD.
ms.assetid: e26dc206-ac85-4346-9fcf-93ebc8948ced
title: VarLenSmallIntToDword, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VarLenSmallIntToDword
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4b0e2fa0813c4b384b17ea45af45f9938bcd85c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518430"
---
# <a name="varlensmallinttodword-function"></a><span data-ttu-id="75d64-103">VarLenSmallIntToDword fonction)</span><span class="sxs-lookup"><span data-stu-id="75d64-103">VarLenSmallIntToDword function</span></span>

<span data-ttu-id="75d64-104">La fonction **VarLenSmallIntToDword** convertit un petit entier de longueur variable en valeur **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="75d64-104">The **VarLenSmallIntToDword** function converts a variable-length, small integer to a **DWORD**.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d64-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75d64-105">Syntax</span></span>


```C++
LPDWORD WINAPI VarLenSmallIntToDword(
   LPBYTE  pValue,
   WORD    ValueLen,
   BOOL    fIsByteswapped,
   LPDWORD lpDword
);
```



## <a name="parameters"></a><span data-ttu-id="75d64-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75d64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75d64-107">*pValue*</span><span class="sxs-lookup"><span data-stu-id="75d64-107">*pValue*</span></span> 
</dt> <dd>

<span data-ttu-id="75d64-108">Pointeur vers le petit entier de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="75d64-108">Pointer to the variable-length, small integer.</span></span>

</dd> <dt>

<span data-ttu-id="75d64-109">*ValueLen*</span><span class="sxs-lookup"><span data-stu-id="75d64-109">*ValueLen*</span></span> 
</dt> <dd>

<span data-ttu-id="75d64-110">Longueur (en octets) de l’entier de longueur variable, petit entier.</span><span class="sxs-lookup"><span data-stu-id="75d64-110">Length (in bytes) of the variable-length, small integer .</span></span>

</dd> <dt>

<span data-ttu-id="75d64-111">*fIsByteswapped*</span><span class="sxs-lookup"><span data-stu-id="75d64-111">*fIsByteswapped*</span></span> 
</dt> <dd>

<span data-ttu-id="75d64-112">Indicateur qui signale si le petit entier de longueur variable est échangé en octets.</span><span class="sxs-lookup"><span data-stu-id="75d64-112">Flag that indicates whether the variable length small integer is byte-swapped.</span></span>

</dd> <dt>

<span data-ttu-id="75d64-113">*lpDword*</span><span class="sxs-lookup"><span data-stu-id="75d64-113">*lpDword*</span></span> 
</dt> <dd>

<span data-ttu-id="75d64-114">**DWORD** dans lequel l’entier est converti.</span><span class="sxs-lookup"><span data-stu-id="75d64-114">The **DWORD** that the integer is converted to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75d64-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75d64-115">Return value</span></span>

<span data-ttu-id="75d64-116">La valeur de retour est un pointeur vers la valeur **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="75d64-116">The return value is a pointer to the **DWORD**.</span></span>

## <a name="requirements"></a><span data-ttu-id="75d64-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75d64-117">Requirements</span></span>



| <span data-ttu-id="75d64-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75d64-118">Requirement</span></span> | <span data-ttu-id="75d64-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="75d64-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75d64-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75d64-120">Minimum supported client</span></span><br/> | <span data-ttu-id="75d64-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75d64-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="75d64-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75d64-122">Minimum supported server</span></span><br/> | <span data-ttu-id="75d64-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75d64-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="75d64-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="75d64-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="75d64-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="75d64-125"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="75d64-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="75d64-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="75d64-127"><dt>Analyseur. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75d64-127"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="75d64-128">DLL</span><span class="sxs-lookup"><span data-stu-id="75d64-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75d64-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75d64-129"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




