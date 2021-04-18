---
description: Recherche l’instance suivante de la propriété spécifiée par le paramètre hProperty.
ms.assetid: f77cb92b-5936-4349-bf66-643c16e9e0df
title: FindPropertyInstanceRestart, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstanceRestart
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: d1e731bb00b28bb62862dd18fbd6031fa973fe38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519253"
---
# <a name="findpropertyinstancerestart-function"></a><span data-ttu-id="85070-103">FindPropertyInstanceRestart fonction)</span><span class="sxs-lookup"><span data-stu-id="85070-103">FindPropertyInstanceRestart function</span></span>

<span data-ttu-id="85070-104">La fonction **FindPropertyInstanceRestart** recherche l’instance suivante de la propriété spécifiée par le paramètre *hProperty* .</span><span class="sxs-lookup"><span data-stu-id="85070-104">The **FindPropertyInstanceRestart** function finds the next instance of the property specified by the *hProperty* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="85070-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85070-105">Syntax</span></span>


```C++
LPPROPERTYINST WINAPI FindPropertyInstanceRestart(
  _In_ HFRAME         hFrame,
  _In_ HPROPERTY      hProperty,
  _In_ LPPROPERTYINST *lpRestartKey,
  _In_ BOOL           DirForward
);
```



## <a name="parameters"></a><span data-ttu-id="85070-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85070-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85070-107">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="85070-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85070-108">Handle du frame.</span><span class="sxs-lookup"><span data-stu-id="85070-108">A handle to the frame.</span></span> <span data-ttu-id="85070-109">Le descripteur de frame peut être récupéré par un appel à la fonction [GetFrame](getframe.md) .</span><span class="sxs-lookup"><span data-stu-id="85070-109">The frame handle can be retrieved by a call to the [GetFrame](getframe.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="85070-110">*hProperty* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="85070-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85070-111">Handle vers la propriété à rechercher.</span><span class="sxs-lookup"><span data-stu-id="85070-111">A handle to the property to find.</span></span> <span data-ttu-id="85070-112">Le descripteur de propriété peut être récupéré par un appel à la fonction [GetProperty](getproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="85070-112">The property handle can be retrieved by a call to the [GetProperty](getproperty.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="85070-113">*lpRestartKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="85070-113">*lpRestartKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85070-114">Pointeur vers l’instance de propriété utilisée comme point de départ de la recherche.</span><span class="sxs-lookup"><span data-stu-id="85070-114">A pointer to the property instance used as the starting point of the search.</span></span> <span data-ttu-id="85070-115">Si le paramètre *lpRestartKey* a la valeur **null**, la recherche commence au début du frame ou à la fin du frame, selon la valeur du paramètre *DirForward* .</span><span class="sxs-lookup"><span data-stu-id="85070-115">If the *lpRestartKey* parameter is set to **NULL**, the search begins at beginning of the frame, or the end of the frame, depending on the value of the *DirForward* parameter.</span></span>

<span data-ttu-id="85070-116">Si *lpRestartKey* pointe vers la **valeur null**, la recherche commence au début du frame si *DirForward* a la **valeur true** ou à la fin du frame si le paramètre a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="85070-116">If *lpRestartKey* points to **NULL**, the search begins at the beginning of the frame if *DirForward* is **TRUE** or the at end of the frame if the parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="85070-117">*DirForward* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="85070-117">*DirForward* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85070-118">Indicateur du sens de la recherche.</span><span class="sxs-lookup"><span data-stu-id="85070-118">An indicator of the search direction.</span></span> <span data-ttu-id="85070-119">Si la valeur est **true**, la recherche passe de l’emplacement actuel à la fin du frame.</span><span class="sxs-lookup"><span data-stu-id="85070-119">If the value is **TRUE**, the search moves from the current location to the end of the frame.</span></span> <span data-ttu-id="85070-120">Si la valeur est **false**, la recherche passe de l’emplacement actuel au début du frame.</span><span class="sxs-lookup"><span data-stu-id="85070-120">If the value is **FALSE**, the search moves from the current location to the beginning of the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85070-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="85070-121">Return value</span></span>

<span data-ttu-id="85070-122">Si la fonction réussit, la valeur de retour est le prochain **LPPROPERTYINST** valide.</span><span class="sxs-lookup"><span data-stu-id="85070-122">If the function is successful, the return value is the next valid **LPPROPERTYINST**.</span></span>

<span data-ttu-id="85070-123">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="85070-123">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="85070-124">Notes</span><span class="sxs-lookup"><span data-stu-id="85070-124">Remarks</span></span>

<span data-ttu-id="85070-125">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **FindPropertyInstanceRestart** .</span><span class="sxs-lookup"><span data-stu-id="85070-125">[*Experts*](e.md) and [*parsers*](p.md) can call the **FindPropertyInstanceRestart** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="85070-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85070-126">Requirements</span></span>



| <span data-ttu-id="85070-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85070-127">Requirement</span></span> | <span data-ttu-id="85070-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="85070-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="85070-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85070-129">Minimum supported client</span></span><br/> | <span data-ttu-id="85070-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85070-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="85070-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85070-131">Minimum supported server</span></span><br/> | <span data-ttu-id="85070-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85070-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="85070-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="85070-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="85070-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="85070-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="85070-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="85070-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="85070-136"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85070-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="85070-137">DLL</span><span class="sxs-lookup"><span data-stu-id="85070-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85070-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85070-138"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85070-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85070-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85070-140">GetFrame</span><span class="sxs-lookup"><span data-stu-id="85070-140">GetFrame</span></span>](getframe.md)
</dt> <dt>

[<span data-ttu-id="85070-141">GetProperty</span><span class="sxs-lookup"><span data-stu-id="85070-141">GetProperty</span></span>](getproperty.md)
</dt> </dl>

 

 




