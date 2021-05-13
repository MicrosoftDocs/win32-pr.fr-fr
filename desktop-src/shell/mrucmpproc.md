---
description: Utilisé pour déterminer si un élément est présent dans une liste des derniers fichiers utilisés.
title: MRUCMPPROC fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MRUCMPPROC
- MRUCMPPROCA
- MRUCMPPROCW
api_type:
- UserDefined
api_location: ''
ms.assetid: 00f31d6b-2a96-4abd-9647-24a6e66aa22f
ms.openlocfilehash: 83020fbcd0d4cfcfbc643d1360e3671595de6f32
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840780"
---
# <a name="mrucmpproc-callback-function"></a><span data-ttu-id="4fdf6-103">MRUCMPPROC fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="4fdf6-103">MRUCMPPROC callback function</span></span>

<span data-ttu-id="4fdf6-104">Utilisé pour déterminer si un élément est présent dans une liste des derniers fichiers utilisés.</span><span class="sxs-lookup"><span data-stu-id="4fdf6-104">Used to determine whether an item is present in a most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fdf6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4fdf6-105">Syntax</span></span>


```C++
int CALLBACK MRUCMPPROC(
   LPCTSTR pString1,
   LPCTSTR pString2
);
```



## <a name="parameters"></a><span data-ttu-id="4fdf6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4fdf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fdf6-107">*pString1*</span><span class="sxs-lookup"><span data-stu-id="4fdf6-107">*pString1*</span></span> 
</dt> <dd>

<span data-ttu-id="4fdf6-108">Type : **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="4fdf6-108">Type: **LPCTSTR**</span></span>

<span data-ttu-id="4fdf6-109">Première chaîne.</span><span class="sxs-lookup"><span data-stu-id="4fdf6-109">The first string.</span></span>

</dd> <dt>

<span data-ttu-id="4fdf6-110">*pString2*</span><span class="sxs-lookup"><span data-stu-id="4fdf6-110">*pString2*</span></span> 
</dt> <dd>

<span data-ttu-id="4fdf6-111">Type : **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="4fdf6-111">Type: **LPCTSTR**</span></span>

<span data-ttu-id="4fdf6-112">Deuxième chaîne à comparer au premier.</span><span class="sxs-lookup"><span data-stu-id="4fdf6-112">A second string to compare to the first.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fdf6-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4fdf6-113">Return value</span></span>

<span data-ttu-id="4fdf6-114">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="4fdf6-114">Type: **int**</span></span>

<span data-ttu-id="4fdf6-115">Retourne 0 si les éléments sont identiques, une valeur différente de zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4fdf6-115">Returns 0 if the items are identical, a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fdf6-116">Notes</span><span class="sxs-lookup"><span data-stu-id="4fdf6-116">Remarks</span></span>

<span data-ttu-id="4fdf6-117">Cette fonction peut éventuellement être spécifiée pour être utilisée dans la structure [**MRUINFO**](mruinfo.md) transmise à [**CreateMRUListW**](createmrulist.md).</span><span class="sxs-lookup"><span data-stu-id="4fdf6-117">This function can be optionally specified for use in the [**MRUINFO**](mruinfo.md) structure passed to [**CreateMRUListW**](createmrulist.md).</span></span> <span data-ttu-id="4fdf6-118">Cela est utile lorsque la liste MRU a été créée avec l’indicateur **\_ binaire MRU** .</span><span class="sxs-lookup"><span data-stu-id="4fdf6-118">This is useful when the MRU list was created with the **MRU\_BINARY** flag.</span></span> <span data-ttu-id="4fdf6-119">Lorsque cette fonction n’est pas spécifiée, les fonctions de comparaison de chaînes standard sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="4fdf6-119">When this function is not specified, standard string comparison functions are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fdf6-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4fdf6-120">Requirements</span></span>



| <span data-ttu-id="4fdf6-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4fdf6-121">Requirement</span></span> | <span data-ttu-id="4fdf6-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fdf6-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="4fdf6-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fdf6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4fdf6-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4fdf6-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="4fdf6-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fdf6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4fdf6-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4fdf6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="4fdf6-127">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="4fdf6-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4fdf6-128">**MRUCMPPROCW** (Unicode) et **MRUCMPPROCA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4fdf6-128">**MRUCMPPROCW** (Unicode) and **MRUCMPPROCA** (ANSI)</span></span><br/> |



 

 




