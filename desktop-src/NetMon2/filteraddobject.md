---
description: La fonction FilterAddObject ajoute un objet unique à un filtre d’affichage.
ms.assetid: 796216f4-a407-4a8c-98b3-8c3761d91913
title: FilterAddObject, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilterAddObject
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7fc6c41a675bfe560c060e271e4f9f48f88cd58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484329"
---
# <a name="filteraddobject-function"></a><span data-ttu-id="88344-103">FilterAddObject fonction)</span><span class="sxs-lookup"><span data-stu-id="88344-103">FilterAddObject function</span></span>

<span data-ttu-id="88344-104">La fonction **FilterAddObject** ajoute un objet unique à un [*filtre d’affichage*](d.md).</span><span class="sxs-lookup"><span data-stu-id="88344-104">The **FilterAddObject** function adds a single object to a [*display filter*](d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="88344-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88344-105">Syntax</span></span>


```C++
DWORD WINAPI FilterAddObject(
  _In_  HFILTER        hFilter,
  _Out_ LPFILTEROBJECT lpFilterObject
);
```



## <a name="parameters"></a><span data-ttu-id="88344-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88344-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88344-107">*hFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="88344-107">*hFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88344-108">Handle sur le filtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="88344-108">Handle to the display filter.</span></span>

</dd> <dt>

<span data-ttu-id="88344-109">*lpFilterObject* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="88344-109">*lpFilterObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88344-110">Pointeur vers une structure [FILTEROBJECT](filterobject.md) qui définit l’objet à ajouter au filtre.</span><span class="sxs-lookup"><span data-stu-id="88344-110">Pointer to a [FILTEROBJECT](filterobject.md) structure that defines the object to be added to the filter.</span></span> <span data-ttu-id="88344-111">Chaque objet peut être un opérateur, une valeur ou une propriété.</span><span class="sxs-lookup"><span data-stu-id="88344-111">Each object can be an operator, value, or property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88344-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="88344-112">Return value</span></span>

<span data-ttu-id="88344-113">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="88344-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="88344-114">Si la fonction échoue, la valeur de retour est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="88344-114">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="88344-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="88344-115">Return code</span></span>                                                                                              | <span data-ttu-id="88344-116">Description</span><span class="sxs-lookup"><span data-stu-id="88344-116">Description</span></span>                                                                  |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="88344-117"><dt>**\_paramètre NMERR non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="88344-117"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="88344-118">La valeur du paramètre *hFilter* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="88344-118">The *hFilter* parameter has an invalid value.</span></span><br/>                     |
| <dl> <span data-ttu-id="88344-119"><dt>**NMERR \_ \_ de \_ mémoire insuffisante**</dt></span><span class="sxs-lookup"><span data-stu-id="88344-119"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="88344-120">Moniteur réseau ne dispose pas de suffisamment de mémoire pour créer l’objet.</span><span class="sxs-lookup"><span data-stu-id="88344-120">Network Monitor does not have enough memory to create the object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="88344-121">Notes</span><span class="sxs-lookup"><span data-stu-id="88344-121">Remarks</span></span>

<span data-ttu-id="88344-122">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **FilterAddObject** .</span><span class="sxs-lookup"><span data-stu-id="88344-122">[*Experts*](e.md) and [*parsers*](p.md) can call the **FilterAddObject** function.</span></span>

<span data-ttu-id="88344-123">La fonction **FilterAddObject** est appelée chaque fois qu’un objet de filtre est ajouté au filtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="88344-123">The **FilterAddObject** function is called each time a filter object is added to the display filter.</span></span> <span data-ttu-id="88344-124">Le filtre d’affichage est une pile suffixée d’objets qui peut être un opérateur, une valeur ou une propriété.</span><span class="sxs-lookup"><span data-stu-id="88344-124">The display filter is a postfix stack of objects that can be an operator, value, or property.</span></span>

## <a name="requirements"></a><span data-ttu-id="88344-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88344-125">Requirements</span></span>



| <span data-ttu-id="88344-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88344-126">Requirement</span></span> | <span data-ttu-id="88344-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="88344-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="88344-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88344-128">Minimum supported client</span></span><br/> | <span data-ttu-id="88344-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88344-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="88344-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88344-130">Minimum supported server</span></span><br/> | <span data-ttu-id="88344-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88344-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="88344-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="88344-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="88344-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="88344-133"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="88344-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="88344-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="88344-135"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88344-135"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="88344-136">DLL</span><span class="sxs-lookup"><span data-stu-id="88344-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88344-137"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88344-137"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88344-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88344-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88344-139">FILTEROBJECT</span><span class="sxs-lookup"><span data-stu-id="88344-139">FILTEROBJECT</span></span>](filterobject.md)
</dt> </dl>

 

 




