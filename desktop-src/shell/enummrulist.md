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
ms.openlocfilehash: 1e6e4bd0820d35fec2a108a81eb1030567493e6a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843160"
---
# <a name="enummrulistw-function"></a><span data-ttu-id="b9e77-104">EnumMRUListW fonction)</span><span class="sxs-lookup"><span data-stu-id="b9e77-104">EnumMRUListW function</span></span>

<span data-ttu-id="b9e77-105">\[Cette fonction est disponible via Windows XP avec Service Pack 2 (SP2) et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b9e77-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="b9e77-106">Il peut être modifié ou non disponible dans les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="b9e77-106">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="b9e77-107">\]</span><span class="sxs-lookup"><span data-stu-id="b9e77-107">\]</span></span>

<span data-ttu-id="b9e77-108">Énumère le contenu de la liste des derniers fichiers utilisés.</span><span class="sxs-lookup"><span data-stu-id="b9e77-108">Enumerates the contents of the most recently used (MRU) list.</span></span> <span data-ttu-id="b9e77-109">Récupère éventuellement un élément de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="b9e77-109">Optionally retrieves an item from the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9e77-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9e77-110">Syntax</span></span>


```C++
int EnumMRUListW(
  _In_  HANDLE hMRU,
  _In_  int    nItem,
  _Out_ void   *lpData,
  _In_  UINT   uLen
);
```



## <a name="parameters"></a><span data-ttu-id="b9e77-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9e77-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9e77-112">*hMRU* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b9e77-112">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9e77-113">Type : **handle**</span><span class="sxs-lookup"><span data-stu-id="b9e77-113">Type: **HANDLE**</span></span>

<span data-ttu-id="b9e77-114">Handle de la liste MRU, obtenu lors de la création de la liste.</span><span class="sxs-lookup"><span data-stu-id="b9e77-114">The handle of the MRU list, obtained when the list was created.</span></span>

</dd> <dt>

<span data-ttu-id="b9e77-115">*nItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b9e77-115">*nItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9e77-116">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="b9e77-116">Type: **int**</span></span>

<span data-ttu-id="b9e77-117">Élément à retourner.</span><span class="sxs-lookup"><span data-stu-id="b9e77-117">The item to return.</span></span> <span data-ttu-id="b9e77-118">Si cette valeur est inférieure à 0, la fonction retourne le nombre d’éléments dans la liste MRU.</span><span class="sxs-lookup"><span data-stu-id="b9e77-118">If this value is less than 0, the function returns the number of items in the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="b9e77-119">*lpData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b9e77-119">*lpData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9e77-120">Type : **void \***</span><span class="sxs-lookup"><span data-stu-id="b9e77-120">Type: **void\***</span></span>

<span data-ttu-id="b9e77-121">Pointeur vers une mémoire tampon qui reçoit l’élément demandé dans *nItem*.</span><span class="sxs-lookup"><span data-stu-id="b9e77-121">A pointer to a buffer that receives the item requested in *nItem*.</span></span> <span data-ttu-id="b9e77-122">Si *nItem* est inférieur à 0, le contenu de cette mémoire tampon n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="b9e77-122">If *nItem* is less than 0, the contents of this buffer are unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="b9e77-123">*uLen* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b9e77-123">*uLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9e77-124">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="b9e77-124">Type: **UINT**</span></span>

<span data-ttu-id="b9e77-125">Taille de la mémoire tampon, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="b9e77-125">The size of the buffer, including the terminating null character.</span></span> <span data-ttu-id="b9e77-126">Si la liste MRU a été créée avec l’indicateur **\_ binaire MRU** , il s’agit de la taille en octets.</span><span class="sxs-lookup"><span data-stu-id="b9e77-126">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="b9e77-127">Dans le cas contraire, il s’agit de la taille en caractères.</span><span class="sxs-lookup"><span data-stu-id="b9e77-127">Otherwise, it is the size in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9e77-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b9e77-128">Return value</span></span>

<span data-ttu-id="b9e77-129">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="b9e77-129">Type: **int**</span></span>

<span data-ttu-id="b9e77-130">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b9e77-130">Returns one of the following values.</span></span>

-   <span data-ttu-id="b9e77-131">Retourne le nombre d’éléments dans l’énumération, si *nItem* est inférieur à 0.</span><span class="sxs-lookup"><span data-stu-id="b9e77-131">Returns the number of items in the enumeration, if *nItem* is less than 0.</span></span>
-   <span data-ttu-id="b9e77-132">Retourne-1 si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b9e77-132">Returns -1 if an error occurred.</span></span>
-   <span data-ttu-id="b9e77-133">Sinon, retourne la taille de la chaîne retournée dans *lpData*, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="b9e77-133">Otherwise, returns the size of the string returned in *lpData*, including the terminating null character.</span></span> <span data-ttu-id="b9e77-134">Si la liste MRU a été créée avec l’indicateur **\_ binaire MRU** , il s’agit de la taille en octets.</span><span class="sxs-lookup"><span data-stu-id="b9e77-134">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="b9e77-135">Dans le cas contraire, il s’agit de la taille en caractères.</span><span class="sxs-lookup"><span data-stu-id="b9e77-135">Otherwise, it is the size in characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9e77-136">Notes</span><span class="sxs-lookup"><span data-stu-id="b9e77-136">Remarks</span></span>

<span data-ttu-id="b9e77-137">Cette fonction n’est pas incluse dans un en-tête public ou une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b9e77-137">This function is not included in a public header or library.</span></span> <span data-ttu-id="b9e77-138">Il est accessible par le biais de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ou extrait de comctl32.dll par son ordinal, qui est 403 pour **EnumMRUListW**.</span><span class="sxs-lookup"><span data-stu-id="b9e77-138">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 403 for **EnumMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9e77-139">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b9e77-139">Requirements</span></span>



| <span data-ttu-id="b9e77-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9e77-140">Requirement</span></span> | <span data-ttu-id="b9e77-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9e77-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9e77-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9e77-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b9e77-143">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b9e77-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b9e77-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9e77-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b9e77-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b9e77-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b9e77-146">DLL</span><span class="sxs-lookup"><span data-stu-id="b9e77-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9e77-147"><dt>Comctl32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="b9e77-147"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="b9e77-148">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="b9e77-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b9e77-149">**EnumMRUListW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="b9e77-149">**EnumMRUListW** (Unicode)</span></span><br/>                                                                          |



## <a name="see-also"></a><span data-ttu-id="b9e77-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9e77-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9e77-151">**CreateMRUListW**</span><span class="sxs-lookup"><span data-stu-id="b9e77-151">**CreateMRUListW**</span></span>](createmrulist.md)
</dt> <dt>

[<span data-ttu-id="b9e77-152">**MRUINFO**</span><span class="sxs-lookup"><span data-stu-id="b9e77-152">**MRUINFO**</span></span>](mruinfo.md)
</dt> </dl>

 

 
