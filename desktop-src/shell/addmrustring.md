---
description: Ajoute une chaîne en haut de la liste des derniers fichiers utilisés.
title: AddMRUStringW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMRUStringW
- AddMRUStringW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: ad94a442-8492-412c-a4f2-ac6e7c5327d7
ms.openlocfilehash: b62e23cd0604273559e36e561970dd62f117c11d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841190"
---
# <a name="addmrustringw-function"></a><span data-ttu-id="ae952-103">AddMRUStringW fonction)</span><span class="sxs-lookup"><span data-stu-id="ae952-103">AddMRUStringW function</span></span>

<span data-ttu-id="ae952-104">\[Cette fonction est disponible via Windows XP avec Service Pack 2 (SP2) et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ae952-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="ae952-105">Il peut être modifié ou non disponible dans les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="ae952-105">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="ae952-106">\]</span><span class="sxs-lookup"><span data-stu-id="ae952-106">\]</span></span>

<span data-ttu-id="ae952-107">Ajoute une chaîne en haut de la liste des derniers fichiers utilisés.</span><span class="sxs-lookup"><span data-stu-id="ae952-107">Adds a string to the top of the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae952-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae952-108">Syntax</span></span>


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a><span data-ttu-id="ae952-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae952-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae952-110">*hMRU* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae952-110">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae952-111">Type : **handle**</span><span class="sxs-lookup"><span data-stu-id="ae952-111">Type: **HANDLE**</span></span>

<span data-ttu-id="ae952-112">Handle de la liste MRU.</span><span class="sxs-lookup"><span data-stu-id="ae952-112">The handle of the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="ae952-113">*szString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae952-113">*szString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae952-114">Type : **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="ae952-114">Type: **LPCTSTR**</span></span>

<span data-ttu-id="ae952-115">Pointeur vers les données.</span><span class="sxs-lookup"><span data-stu-id="ae952-115">A pointer to the data.</span></span> <span data-ttu-id="ae952-116">Il peut s’agir d’une chaîne ou, si la liste MRU a été créée avec l’indicateur **\_ binaire MRU** , données binaires.</span><span class="sxs-lookup"><span data-stu-id="ae952-116">This can be either a string or, if the MRU list was created with the **MRU\_BINARY** flag, binary data.</span></span> <span data-ttu-id="ae952-117">Dans le cas de données binaires, la première **valeur DWORD** indique sa taille.</span><span class="sxs-lookup"><span data-stu-id="ae952-117">In the case of binary data, the first **DWORD** indicates its size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae952-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ae952-118">Return value</span></span>

<span data-ttu-id="ae952-119">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="ae952-119">Type: **int**</span></span>

<span data-ttu-id="ae952-120">Retourne une valeur non négative en cas de réussite,-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ae952-120">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae952-121">Notes</span><span class="sxs-lookup"><span data-stu-id="ae952-121">Remarks</span></span>

<span data-ttu-id="ae952-122">Cette fonction n’est pas incluse dans un en-tête public ou une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="ae952-122">This function is not included in a public header or library.</span></span> <span data-ttu-id="ae952-123">Il est accessible par le biais de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) ou extrait de comctl32.dll par son ordinal, qui est 401 pour **AddMRUStringW**.</span><span class="sxs-lookup"><span data-stu-id="ae952-123">It can be accessed through [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 401 for **AddMRUStringW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae952-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ae952-124">Requirements</span></span>



| <span data-ttu-id="ae952-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae952-125">Requirement</span></span> | <span data-ttu-id="ae952-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae952-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae952-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae952-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ae952-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae952-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ae952-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae952-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ae952-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae952-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ae952-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ae952-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae952-132"><dt>Comctl32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="ae952-132"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="ae952-133">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="ae952-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ae952-134">**AddMRUStringW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="ae952-134">**AddMRUStringW** (Unicode)</span></span><br/>                                                                         |



 

