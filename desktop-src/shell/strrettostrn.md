---
description: 'Prend une structure STRRET retournée par IShellFolder :: GetDisplayNameOf, le convertit en une chaîne et place le résultat dans une mémoire tampon.'
title: StrRetToStrN fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrRetToStrN
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: a816fb5f-8320-4b63-a85d-dd4c59596ead
ms.openlocfilehash: 89a8d991e22e8615456bd8d4690c046ec0d325d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991809"
---
# <a name="strrettostrn-function"></a><span data-ttu-id="1c6ee-103">StrRetToStrN fonction)</span><span class="sxs-lookup"><span data-stu-id="1c6ee-103">StrRetToStrN function</span></span>

<span data-ttu-id="1c6ee-104">Prend une structure [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) retournée par [**IShellFolder :: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), le convertit en une chaîne et place le résultat dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="1c6ee-104">Takes an [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) structure returned by [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), converts it to a string, and places the result in a buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c6ee-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c6ee-105">Syntax</span></span>


```C++
BOOL StrRetToStrN(
  _Out_   LPTSTR        pszOut,
  _In_    UINT          cchOut,
  _Inout_ LPSTRRET      pStrRet,
  _In_    LPCITEMIDLIST pidl
);
```



## <a name="parameters"></a><span data-ttu-id="1c6ee-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c6ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c6ee-107">*pszOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1c6ee-107">*pszOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c6ee-108">Type : **LPTStr**</span><span class="sxs-lookup"><span data-stu-id="1c6ee-108">Type: **LPTSTR**</span></span>

<span data-ttu-id="1c6ee-109">Mémoire tampon devant contenir le nom complet.</span><span class="sxs-lookup"><span data-stu-id="1c6ee-109">Buffer to hold the display name.</span></span> <span data-ttu-id="1c6ee-110">Elle est retournée en tant que chaîne terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="1c6ee-110">It will be returned as a null-terminated string.</span></span> <span data-ttu-id="1c6ee-111">Si *cchOut* est trop petit, le nom sera tronqué pour s’ajuster.</span><span class="sxs-lookup"><span data-stu-id="1c6ee-111">If *cchOut* is too small, the name will be truncated to fit.</span></span>

</dd> <dt>

<span data-ttu-id="1c6ee-112">*cchOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c6ee-112">*cchOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c6ee-113">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="1c6ee-113">Type: **UINT**</span></span>

<span data-ttu-id="1c6ee-114">Taille de *pszOut*, en caractères.</span><span class="sxs-lookup"><span data-stu-id="1c6ee-114">Size of *pszOut*, in characters.</span></span> <span data-ttu-id="1c6ee-115">Si *cchOut* est trop petit, la chaîne est tronquée pour s’ajuster.</span><span class="sxs-lookup"><span data-stu-id="1c6ee-115">If *cchOut* is too small, the string will be truncated to fit.</span></span>

</dd> <dt>

<span data-ttu-id="1c6ee-116">*pStrRet* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1c6ee-116">*pStrRet* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c6ee-117">Type : **LPSTRRET**</span><span class="sxs-lookup"><span data-stu-id="1c6ee-117">Type: **LPSTRRET**</span></span>

<span data-ttu-id="1c6ee-118">Pointeur vers une structure [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) .</span><span class="sxs-lookup"><span data-stu-id="1c6ee-118">Pointer to an [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) structure.</span></span> <span data-ttu-id="1c6ee-119">Quand la fonction retourne, ce pointeur n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="1c6ee-119">When the function returns, this pointer will no longer be valid.</span></span>

</dd> <dt>

<span data-ttu-id="1c6ee-120">*PIDL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c6ee-120">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c6ee-121">Type : **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="1c6ee-121">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="1c6ee-122">Pointeur vers la structure [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) de l’élément.</span><span class="sxs-lookup"><span data-stu-id="1c6ee-122">Pointer to the item's [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c6ee-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1c6ee-123">Return value</span></span>

<span data-ttu-id="1c6ee-124">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="1c6ee-124">Type: **BOOL**</span></span>

<span data-ttu-id="1c6ee-125">**True** en cas de réussite, **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="1c6ee-125">**TRUE** for success, **FALSE** for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c6ee-126">Notes</span><span class="sxs-lookup"><span data-stu-id="1c6ee-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1c6ee-127">À partir de Shell32.dll version 5,0, l’appel de cette fonction équivaut à appeler [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).</span><span class="sxs-lookup"><span data-stu-id="1c6ee-127">As of Shell32.dll version 5.0, calling this function is equivalent to calling [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).</span></span>

 

<span data-ttu-id="1c6ee-128">**StrRetToStrN** n’est pas exporté par nom.</span><span class="sxs-lookup"><span data-stu-id="1c6ee-128">**StrRetToStrN** is not exported by name.</span></span> <span data-ttu-id="1c6ee-129">Pour l’utiliser, vous devez utiliser [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) et demander l’ordinal 96 de Shell32.dll pour obtenir un pointeur de fonction.</span><span class="sxs-lookup"><span data-stu-id="1c6ee-129">To use it, you must use [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 96 from Shell32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="1c6ee-130">Si le membre **uType** de la structure vers laquelle pointe *pStrRet* est défini sur **STRRET \_ WSTR**, le membre **pOleStr** de cette structure sera libéré au retour.</span><span class="sxs-lookup"><span data-stu-id="1c6ee-130">If the **uType** member of the structure pointed to by *pStrRet* is set to **STRRET\_WSTR**, the **pOleStr** member of that structure will be freed on return.</span></span>

<span data-ttu-id="1c6ee-131">Notez que cette fonction est exportée à partir de Shell32.dll plutôt que Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="1c6ee-131">Note that this function is exported from Shell32.dll rather than Shlwapi.dll.</span></span> <span data-ttu-id="1c6ee-132">Il est également inclus dans shlobj. h plutôt que sur Shlwapi. h.</span><span class="sxs-lookup"><span data-stu-id="1c6ee-132">It is also included in Shlobj.h rather than Shlwapi.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c6ee-133">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1c6ee-133">Requirements</span></span>



| <span data-ttu-id="1c6ee-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c6ee-134">Requirement</span></span> | <span data-ttu-id="1c6ee-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c6ee-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c6ee-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c6ee-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1c6ee-137">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c6ee-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1c6ee-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c6ee-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1c6ee-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c6ee-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1c6ee-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1c6ee-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c6ee-141"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="1c6ee-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c6ee-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c6ee-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c6ee-143">**StrRetToStr**</span><span class="sxs-lookup"><span data-stu-id="1c6ee-143">**StrRetToStr**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra)
</dt> <dt>

[<span data-ttu-id="1c6ee-144">**StrRetToBuf**</span><span class="sxs-lookup"><span data-stu-id="1c6ee-144">**StrRetToBuf**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)
</dt> </dl>

 

 
