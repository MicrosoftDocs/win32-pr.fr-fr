---
description: Vide le cache de base de données de shims. Cette fonction doit être appelée après l’installation d’une nouvelle base de données de shims.
ms.assetid: 7e5bbdca-7b58-4c51-9cd1-105b05ee7fbe
title: ShimFlushCache fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShimFlushCache
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 35e279c5036142ec87c5bad6d7c512388033bc94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033574"
---
# <a name="shimflushcache-function"></a><span data-ttu-id="dd6b6-104">ShimFlushCache fonction)</span><span class="sxs-lookup"><span data-stu-id="dd6b6-104">ShimFlushCache function</span></span>

<span data-ttu-id="dd6b6-105">Vide le cache de base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-105">Flushes the shim database cache.</span></span> <span data-ttu-id="dd6b6-106">Cette fonction doit être appelée après l’installation d’une nouvelle base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-106">This function should be called after installing a new shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd6b6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd6b6-107">Syntax</span></span>


```C++
BOOL WINAPI ShimFlushCache(
  _In_opt_ HWND      hwnd,
  _In_opt_ HINSTANCE hInstance,
  _In_opt_ LPCSTR    lpszCmdLine,
  _In_     int       nCmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="dd6b6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd6b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd6b6-109">*HWND* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="dd6b6-109">*hwnd* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dd6b6-110">Inutilisé doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-110">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="dd6b6-111">*HINSTANCE* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="dd6b6-111">*hInstance* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dd6b6-112">Inutilisé doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-112">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="dd6b6-113">*lpszCmdLine* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="dd6b6-113">*lpszCmdLine* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dd6b6-114">Inutilisé doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-114">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="dd6b6-115">*nCmdShow* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd6b6-115">*nCmdShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd6b6-116">Inutilisé doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-116">Unused; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd6b6-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd6b6-117">Return value</span></span>

<span data-ttu-id="dd6b6-118">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-118">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd6b6-119">Notes</span><span class="sxs-lookup"><span data-stu-id="dd6b6-119">Remarks</span></span>

<span data-ttu-id="dd6b6-120">L’appelant doit être un administrateur.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-120">The caller must be an administrator.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd6b6-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd6b6-121">Requirements</span></span>



| <span data-ttu-id="dd6b6-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd6b6-122">Requirement</span></span> | <span data-ttu-id="dd6b6-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd6b6-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd6b6-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd6b6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dd6b6-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd6b6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dd6b6-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd6b6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dd6b6-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd6b6-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dd6b6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="dd6b6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd6b6-129"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd6b6-129"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd6b6-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd6b6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd6b6-131">**BaseFlushAppcompatCache**</span><span class="sxs-lookup"><span data-stu-id="dd6b6-131">**BaseFlushAppcompatCache**</span></span>](baseflushappcompatcache.md)
</dt> </dl>

 

 




