---
description: La fonction LookupDwordSetString retourne la chaîne correspondant à la valeur spécifiée d’un jeu étiqueté.
ms.assetid: ee2b1b7a-6b64-4c8c-a71d-de970b66d46e
title: LookupDwordSetString, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupDwordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57688edab7421f939e03322b8b244219b00d31fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752188"
---
# <a name="lookupdwordsetstring-function"></a><span data-ttu-id="91ddb-103">LookupDwordSetString fonction)</span><span class="sxs-lookup"><span data-stu-id="91ddb-103">LookupDwordSetString function</span></span>

<span data-ttu-id="91ddb-104">La fonction **LookupDwordSetString** retourne la chaîne correspondant à la valeur spécifiée d’un jeu étiqueté.</span><span class="sxs-lookup"><span data-stu-id="91ddb-104">The **LookupDwordSetString** function returns the string corresponding to the specified value of a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="91ddb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91ddb-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupDwordSetString(
   LPSET lpSet,
   DWORD Value
);
```



## <a name="parameters"></a><span data-ttu-id="91ddb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91ddb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91ddb-107">*lpSet*</span><span class="sxs-lookup"><span data-stu-id="91ddb-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="91ddb-108">Ensemble étiqueté, à partir duquel vous pouvez extraire l’étiquette de la valeur.</span><span class="sxs-lookup"><span data-stu-id="91ddb-108">Labeled set, from which you can extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="91ddb-109">*Valeur*</span><span class="sxs-lookup"><span data-stu-id="91ddb-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="91ddb-110">Valeur d’un jeu étiqueté.</span><span class="sxs-lookup"><span data-stu-id="91ddb-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91ddb-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91ddb-111">Return value</span></span>

<span data-ttu-id="91ddb-112">Si la fonction réussit, la valeur de retour est la chaîne qui correspond à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="91ddb-112">If the function is successful, the return value is the string that corresponds to the specified value.</span></span>

<span data-ttu-id="91ddb-113">Si la fonction échoue, la valeur spécifiée n’est pas dans l’ensemble, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="91ddb-113">If the function is unsuccessful, the specified value is not in the set, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="91ddb-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91ddb-114">Requirements</span></span>



| <span data-ttu-id="91ddb-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91ddb-115">Requirement</span></span> | <span data-ttu-id="91ddb-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="91ddb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91ddb-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91ddb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="91ddb-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91ddb-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="91ddb-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91ddb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="91ddb-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91ddb-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91ddb-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="91ddb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="91ddb-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="91ddb-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="91ddb-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="91ddb-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="91ddb-124"><dt>Analyseur. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91ddb-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="91ddb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="91ddb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91ddb-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91ddb-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




