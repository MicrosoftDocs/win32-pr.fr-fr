---
description: Énumère le contenu de la liste des derniers fichiers utilisés. Récupère éventuellement un élément de l’énumération.
title: EnumMRUListW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMRUListW
- EnumMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 630e5f27-96bf-4e88-b01a-127b301cc051
ms.openlocfilehash: 6b6e9588588e44a2c3b40f6ac012b11f21c875e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867749"
---
# <a name="enummrulistw-function"></a><span data-ttu-id="8cab2-104">EnumMRUListW fonction)</span><span class="sxs-lookup"><span data-stu-id="8cab2-104">EnumMRUListW function</span></span>

<span data-ttu-id="8cab2-105">\[Cette fonction est disponible via Windows XP avec Service Pack 2 (SP2) et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8cab2-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="8cab2-106">Il peut être modifié ou non disponible dans les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="8cab2-106">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="8cab2-107">\]</span><span class="sxs-lookup"><span data-stu-id="8cab2-107">\]</span></span>

<span data-ttu-id="8cab2-108">Énumère le contenu de la liste des derniers fichiers utilisés.</span><span class="sxs-lookup"><span data-stu-id="8cab2-108">Enumerates the contents of the most recently used (MRU) list.</span></span> <span data-ttu-id="8cab2-109">Récupère éventuellement un élément de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="8cab2-109">Optionally retrieves an item from the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cab2-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8cab2-110">Syntax</span></span>


```C++
int EnumMRUListW(
  _In_  HANDLE hMRU,
  _In_  int    nItem,
  _Out_ void   *lpData,
  _In_  UINT   uLen
);
```



## <a name="parameters"></a><span data-ttu-id="8cab2-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8cab2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cab2-112">*hMRU* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8cab2-112">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cab2-113">Type : **handle**</span><span class="sxs-lookup"><span data-stu-id="8cab2-113">Type: **HANDLE**</span></span>

<span data-ttu-id="8cab2-114">Handle de la liste MRU, obtenu lors de la création de la liste.</span><span class="sxs-lookup"><span data-stu-id="8cab2-114">The handle of the MRU list, obtained when the list was created.</span></span>

</dd> <dt>

<span data-ttu-id="8cab2-115">*nItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8cab2-115">*nItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cab2-116">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="8cab2-116">Type: **int**</span></span>

<span data-ttu-id="8cab2-117">Élément à retourner.</span><span class="sxs-lookup"><span data-stu-id="8cab2-117">The item to return.</span></span> <span data-ttu-id="8cab2-118">Si cette valeur est inférieure à 0, la fonction retourne le nombre d’éléments dans la liste MRU.</span><span class="sxs-lookup"><span data-stu-id="8cab2-118">If this value is less than 0, the function returns the number of items in the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="8cab2-119">*lpData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8cab2-119">*lpData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cab2-120">Type : \**void \** _</span><span class="sxs-lookup"><span data-stu-id="8cab2-120">Type: \**void\** _</span></span>

<span data-ttu-id="8cab2-121">Pointeur vers une mémoire tampon qui reçoit l’élément demandé dans _nItem \*.</span><span class="sxs-lookup"><span data-stu-id="8cab2-121">A pointer to a buffer that receives the item requested in _nItem\*.</span></span> <span data-ttu-id="8cab2-122">Si *nItem* est inférieur à 0, le contenu de cette mémoire tampon n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="8cab2-122">If *nItem* is less than 0, the contents of this buffer are unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="8cab2-123">*uLen* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8cab2-123">*uLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cab2-124">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="8cab2-124">Type: **UINT**</span></span>

<span data-ttu-id="8cab2-125">Taille de la mémoire tampon, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="8cab2-125">The size of the buffer, including the terminating null character.</span></span> <span data-ttu-id="8cab2-126">Si la liste MRU a été créée avec l’indicateur **\_ binaire MRU** , il s’agit de la taille en octets.</span><span class="sxs-lookup"><span data-stu-id="8cab2-126">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="8cab2-127">Dans le cas contraire, il s’agit de la taille en caractères.</span><span class="sxs-lookup"><span data-stu-id="8cab2-127">Otherwise, it is the size in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cab2-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8cab2-128">Return value</span></span>

<span data-ttu-id="8cab2-129">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="8cab2-129">Type: **int**</span></span>

<span data-ttu-id="8cab2-130">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8cab2-130">Returns one of the following values.</span></span>

-   <span data-ttu-id="8cab2-131">Retourne le nombre d’éléments dans l’énumération, si *nItem* est inférieur à 0.</span><span class="sxs-lookup"><span data-stu-id="8cab2-131">Returns the number of items in the enumeration, if *nItem* is less than 0.</span></span>
-   <span data-ttu-id="8cab2-132">Retourne-1 si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8cab2-132">Returns -1 if an error occurred.</span></span>
-   <span data-ttu-id="8cab2-133">Sinon, retourne la taille de la chaîne retournée dans *lpData*, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="8cab2-133">Otherwise, returns the size of the string returned in *lpData*, including the terminating null character.</span></span> <span data-ttu-id="8cab2-134">Si la liste MRU a été créée avec l’indicateur **\_ binaire MRU** , il s’agit de la taille en octets.</span><span class="sxs-lookup"><span data-stu-id="8cab2-134">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="8cab2-135">Dans le cas contraire, il s’agit de la taille en caractères.</span><span class="sxs-lookup"><span data-stu-id="8cab2-135">Otherwise, it is the size in characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cab2-136">Notes</span><span class="sxs-lookup"><span data-stu-id="8cab2-136">Remarks</span></span>

<span data-ttu-id="8cab2-137">Cette fonction n’est pas incluse dans un en-tête public ou une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="8cab2-137">This function is not included in a public header or library.</span></span> <span data-ttu-id="8cab2-138">Il est accessible par le biais de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ou extrait de comctl32.dll par son ordinal, qui est 403 pour **EnumMRUListW**.</span><span class="sxs-lookup"><span data-stu-id="8cab2-138">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 403 for **EnumMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cab2-139">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8cab2-139">Requirements</span></span>



| <span data-ttu-id="8cab2-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8cab2-140">Requirement</span></span> | <span data-ttu-id="8cab2-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="8cab2-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cab2-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cab2-142">Minimum supported client</span></span><br/> | <span data-ttu-id="8cab2-143">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8cab2-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8cab2-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cab2-144">Minimum supported server</span></span><br/> | <span data-ttu-id="8cab2-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8cab2-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8cab2-146">DLL</span><span class="sxs-lookup"><span data-stu-id="8cab2-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cab2-147"><dt>Comctl32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="8cab2-147"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="8cab2-148">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="8cab2-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8cab2-149">**EnumMRUListW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="8cab2-149">**EnumMRUListW** (Unicode)</span></span><br/>                                                                          |



## <a name="see-also"></a><span data-ttu-id="8cab2-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cab2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cab2-151">**CreateMRUListW**</span><span class="sxs-lookup"><span data-stu-id="8cab2-151">**CreateMRUListW**</span></span>](createmrulist.md)
</dt> <dt>

[<span data-ttu-id="8cab2-152">**MRUINFO**</span><span class="sxs-lookup"><span data-stu-id="8cab2-152">**MRUINFO**</span></span>](mruinfo.md)
</dt> </dl>

 

 
