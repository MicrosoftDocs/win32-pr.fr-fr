---
description: Multiplie les entiers étendus.
ms.assetid: 6a59d211-4baf-4c7c-af2a-ffb0c5773445
title: RtlExtendedIntegerMultiply fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedIntegerMultiply
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b824080c28da3265be6dc0333f236b8c9a4cbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525430"
---
# <a name="rtlextendedintegermultiply-function"></a><span data-ttu-id="33432-103">RtlExtendedIntegerMultiply fonction)</span><span class="sxs-lookup"><span data-stu-id="33432-103">RtlExtendedIntegerMultiply function</span></span>

<span data-ttu-id="33432-104">\[La fonction **RtlExtendedIntegerMultiply** est exportée pour prendre en charge les binaires de pilote existants et est obsolète.</span><span class="sxs-lookup"><span data-stu-id="33432-104">\[The **RtlExtendedIntegerMultiply** function is exported to support existing driver binaries and is obsolete.</span></span> <span data-ttu-id="33432-105">Pour de meilleures performances, utilisez la prise en charge du compilateur pour les opérations d’entiers 64 bits.\]</span><span class="sxs-lookup"><span data-stu-id="33432-105">For better performance, use the compiler support for 64-bit integer operations.\]</span></span>

<span data-ttu-id="33432-106">Multiplie les entiers étendus.</span><span class="sxs-lookup"><span data-stu-id="33432-106">Multiplies extended integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="33432-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33432-107">Syntax</span></span>


```C++
LARGE_INTEGER RtlExtendedIntegerMultiply(
  _In_ LARGE_INTEGER Multiplicand,
  _In_ LONG          Multiplier
);
```



## <a name="parameters"></a><span data-ttu-id="33432-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33432-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33432-109">*Multiplicande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33432-109">*Multiplicand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33432-110">Multiplicande.</span><span class="sxs-lookup"><span data-stu-id="33432-110">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="33432-111">*Multiplicateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33432-111">*Multiplier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33432-112">Multiplicateur.</span><span class="sxs-lookup"><span data-stu-id="33432-112">Multiplier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33432-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33432-113">Return value</span></span>

<span data-ttu-id="33432-114">Retourne le résultat de la multiplication.</span><span class="sxs-lookup"><span data-stu-id="33432-114">Returns multiplication result.</span></span>

## <a name="remarks"></a><span data-ttu-id="33432-115">Notes</span><span class="sxs-lookup"><span data-stu-id="33432-115">Remarks</span></span>

<span data-ttu-id="33432-116">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="33432-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="33432-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33432-117">Requirements</span></span>



| <span data-ttu-id="33432-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33432-118">Requirement</span></span> | <span data-ttu-id="33432-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="33432-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="33432-120">DLL</span><span class="sxs-lookup"><span data-stu-id="33432-120">DLL</span></span><br/> | <dl> <span data-ttu-id="33432-121"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33432-121"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
