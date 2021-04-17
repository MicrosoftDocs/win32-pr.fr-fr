---
description: La fonction LookupWordSetString retourne la chaîne correspondant à la valeur demandée d’un jeu étiqueté.
ms.assetid: e8d158a1-8544-4c10-b8e8-46888c1097e4
title: LookupWordSetString, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupWordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7487becb195571e1eb88044195293b2c0b226e8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526763"
---
# <a name="lookupwordsetstring-function"></a><span data-ttu-id="c7d98-103">LookupWordSetString fonction)</span><span class="sxs-lookup"><span data-stu-id="c7d98-103">LookupWordSetString function</span></span>

<span data-ttu-id="c7d98-104">La fonction **LookupWordSetString** retourne la chaîne correspondant à la valeur demandée d’un jeu étiqueté.</span><span class="sxs-lookup"><span data-stu-id="c7d98-104">The **LookupWordSetString** function returns the string corresponding to the requested value from a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7d98-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7d98-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupWordSetString(
   LPSET lpSet,
   WORD  Value
);
```



## <a name="parameters"></a><span data-ttu-id="c7d98-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7d98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7d98-107">*lpSet*</span><span class="sxs-lookup"><span data-stu-id="c7d98-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="c7d98-108">Jeu étiqueté à partir duquel vous extrayez l’étiquette de la valeur.</span><span class="sxs-lookup"><span data-stu-id="c7d98-108">Labeled set from which you extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="c7d98-109">*Valeur*</span><span class="sxs-lookup"><span data-stu-id="c7d98-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="c7d98-110">Valeur d’un jeu étiqueté.</span><span class="sxs-lookup"><span data-stu-id="c7d98-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7d98-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c7d98-111">Return value</span></span>

<span data-ttu-id="c7d98-112">Si la fonction réussit, la valeur de retour est une chaîne qui correspond à la valeur demandée.</span><span class="sxs-lookup"><span data-stu-id="c7d98-112">If the function is successful, the return value is a string that corresponds to the requested value.</span></span>

<span data-ttu-id="c7d98-113">Si la fonction échoue, la valeur spécifiée n’est pas dans l’ensemble, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="c7d98-113">If the function is unsuccessful, the specified value is not in the set, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7d98-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7d98-114">Requirements</span></span>



| <span data-ttu-id="c7d98-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7d98-115">Requirement</span></span> | <span data-ttu-id="c7d98-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7d98-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d98-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7d98-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c7d98-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7d98-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c7d98-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7d98-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c7d98-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7d98-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c7d98-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7d98-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7d98-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7d98-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7d98-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c7d98-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7d98-124"><dt>Analyseur. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7d98-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="c7d98-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c7d98-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7d98-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7d98-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




