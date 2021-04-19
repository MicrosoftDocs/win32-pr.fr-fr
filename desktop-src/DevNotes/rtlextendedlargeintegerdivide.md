---
description: Divise des entiers étendus.
ms.assetid: d46f65f0-6c41-4cb2-9882-5b11f7aae3ca
title: RtlExtendedLargeIntegerDivide fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedLargeIntegerDivide
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: b17c89a744748214d74dc24abdaa8a12ac71e960
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531009"
---
# <a name="rtlextendedlargeintegerdivide-function"></a><span data-ttu-id="35238-103">RtlExtendedLargeIntegerDivide fonction)</span><span class="sxs-lookup"><span data-stu-id="35238-103">RtlExtendedLargeIntegerDivide function</span></span>

<span data-ttu-id="35238-104">\[La fonction **RtlExtendedLargeIntegerDivide** est exportée pour prendre en charge les binaires de pilote existants et est obsolète.</span><span class="sxs-lookup"><span data-stu-id="35238-104">\[The **RtlExtendedLargeIntegerDivide** function is exported to support existing driver binaries and is obsolete.</span></span> <span data-ttu-id="35238-105">Pour de meilleures performances, utilisez la prise en charge du compilateur pour les opérations d’entiers 64 bits.\]</span><span class="sxs-lookup"><span data-stu-id="35238-105">For better performance, use the compiler support for 64-bit integer operations.\]</span></span>

<span data-ttu-id="35238-106">Divise des entiers étendus.</span><span class="sxs-lookup"><span data-stu-id="35238-106">Divides extended integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="35238-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35238-107">Syntax</span></span>


```C++
LARGE_INTEGER RtlExtendedLargeIntegerDivide(
  _In_    LARGE_INTEGER Dividend,
  _In_    ULONG         Divisor,
  _Inout_ PULONG        Remainder
);
```



## <a name="parameters"></a><span data-ttu-id="35238-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35238-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35238-109">*Dividende* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35238-109">*Dividend* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35238-110">Détaché.</span><span class="sxs-lookup"><span data-stu-id="35238-110">Dividend.</span></span>

</dd> <dt>

<span data-ttu-id="35238-111">*Diviseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35238-111">*Divisor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35238-112">Division.</span><span class="sxs-lookup"><span data-stu-id="35238-112">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="35238-113">*Reste* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="35238-113">*Remainder* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="35238-114">Pointeur vers le reste de la Division.</span><span class="sxs-lookup"><span data-stu-id="35238-114">Pointer to division remainder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35238-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35238-115">Return value</span></span>

<span data-ttu-id="35238-116">Retourne le résultat de l’opération de division.</span><span class="sxs-lookup"><span data-stu-id="35238-116">Returns the result of the division operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="35238-117">Notes</span><span class="sxs-lookup"><span data-stu-id="35238-117">Remarks</span></span>

<span data-ttu-id="35238-118">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="35238-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="35238-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35238-119">Requirements</span></span>



| <span data-ttu-id="35238-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35238-120">Requirement</span></span> | <span data-ttu-id="35238-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="35238-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="35238-122">DLL</span><span class="sxs-lookup"><span data-stu-id="35238-122">DLL</span></span><br/> | <dl> <span data-ttu-id="35238-123"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35238-123"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
