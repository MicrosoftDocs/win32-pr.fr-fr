---
description: La fonction LookupByteSetString retourne la chaîne correspondant à la valeur spécifiée d’un jeu étiqueté.
ms.assetid: 295891f9-dc8d-4dbe-aac9-7d0a96993cfa
title: LookupByteSetString, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupByteSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7a2b5bffbfcb30ed8ec00da42fbc9ad6008fd5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545791"
---
# <a name="lookupbytesetstring-function"></a><span data-ttu-id="ad7f8-103">LookupByteSetString fonction)</span><span class="sxs-lookup"><span data-stu-id="ad7f8-103">LookupByteSetString function</span></span>

<span data-ttu-id="ad7f8-104">La fonction **LookupByteSetString** retourne la chaîne correspondant à la valeur spécifiée d’un jeu étiqueté.</span><span class="sxs-lookup"><span data-stu-id="ad7f8-104">The **LookupByteSetString** function returns the string corresponding to the specified value of a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad7f8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad7f8-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupByteSetString(
   LPSET lpSet,
   BYTE  Value
);
```



## <a name="parameters"></a><span data-ttu-id="ad7f8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad7f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad7f8-107">*lpSet*</span><span class="sxs-lookup"><span data-stu-id="ad7f8-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="ad7f8-108">Pointeur vers un jeu étiqueté, à partir duquel vous pouvez extraire l’étiquette de la valeur.</span><span class="sxs-lookup"><span data-stu-id="ad7f8-108">Pointer to a labeled set, from which you can extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="ad7f8-109">*Valeur*</span><span class="sxs-lookup"><span data-stu-id="ad7f8-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="ad7f8-110">Valeur d’un jeu étiqueté.</span><span class="sxs-lookup"><span data-stu-id="ad7f8-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad7f8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad7f8-111">Return value</span></span>

<span data-ttu-id="ad7f8-112">Si la fonction réussit, la valeur de retour est une chaîne qui correspond à la valeur fournie.</span><span class="sxs-lookup"><span data-stu-id="ad7f8-112">If the function is successful, the return value is a string corresponding to the value provided.</span></span>

<span data-ttu-id="ad7f8-113">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="ad7f8-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad7f8-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad7f8-114">Requirements</span></span>



| <span data-ttu-id="ad7f8-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad7f8-115">Requirement</span></span> | <span data-ttu-id="ad7f8-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad7f8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad7f8-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad7f8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ad7f8-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad7f8-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ad7f8-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad7f8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ad7f8-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad7f8-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ad7f8-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad7f8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad7f8-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad7f8-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="ad7f8-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ad7f8-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="ad7f8-124"><dt>Analyseur. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad7f8-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="ad7f8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ad7f8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad7f8-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad7f8-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




