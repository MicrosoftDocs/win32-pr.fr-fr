---
description: La fonction ThunkConnect32 est utilisée par les pilotes de périphériques 16 bits (pour MS-DOS) qui appellent le noyau 32 bits.
ms.assetid: 3376ca67-04ea-4765-a2f4-15a84d5c84d4
title: ThunkConnect32 fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ThunkConnect32
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 7f22d7ceb59732e986c23c873133b11f358364cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542448"
---
# <a name="thunkconnect32-function"></a><span data-ttu-id="1a113-103">ThunkConnect32 fonction)</span><span class="sxs-lookup"><span data-stu-id="1a113-103">ThunkConnect32 function</span></span>

<span data-ttu-id="1a113-104">\[Cette fonction était prise en charge pour la compatibilité descendante, mais elle n’est pas présente dans les versions actuelles de Windows.</span><span class="sxs-lookup"><span data-stu-id="1a113-104">\[This function was supported for backward compatibility, but is not present in current versions of Windows.</span></span> <span data-ttu-id="1a113-105">Les nouveaux pilotes de périphérique doivent être de 32 ou 64 bits et n’ont pas besoin de cette fonction.\]</span><span class="sxs-lookup"><span data-stu-id="1a113-105">New device drivers should be 32- or 64-bit and do not need this function.\]</span></span>

<span data-ttu-id="1a113-106">La fonction **ThunkConnect32** est utilisée par les pilotes de périphériques 16 bits (pour MS-DOS) qui appellent le noyau 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1a113-106">The **ThunkConnect32** function is used by 16-bit device drivers (for MS-DOS) that call into the 32-bit kernel.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a113-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a113-107">Syntax</span></span>


```C++
BOOL ThunkConnect32(
   LPVOID lpThunkData32,
   LPSTR  pszThunkData16Name,
   LPSTR  pszDll16,
   LPSTR  pszDll32,
   HANDLE hInstance,
   DWORD  dwReason
);
```



## <a name="parameters"></a><span data-ttu-id="1a113-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a113-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a113-109">*lpThunkData32*</span><span class="sxs-lookup"><span data-stu-id="1a113-109">*lpThunkData32*</span></span> 
</dt> <dd>

<span data-ttu-id="1a113-110">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="1a113-110">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="1a113-111">*pszThunkData16Name*</span><span class="sxs-lookup"><span data-stu-id="1a113-111">*pszThunkData16Name*</span></span> 
</dt> <dd>

<span data-ttu-id="1a113-112">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="1a113-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="1a113-113">*pszDll16*</span><span class="sxs-lookup"><span data-stu-id="1a113-113">*pszDll16*</span></span> 
</dt> <dd>

<span data-ttu-id="1a113-114">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="1a113-114">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="1a113-115">*pszDll32*</span><span class="sxs-lookup"><span data-stu-id="1a113-115">*pszDll32*</span></span> 
</dt> <dd>

<span data-ttu-id="1a113-116">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="1a113-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="1a113-117">*hInstance*</span><span class="sxs-lookup"><span data-stu-id="1a113-117">*hInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="1a113-118">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="1a113-118">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="1a113-119">*dwReason*</span><span class="sxs-lookup"><span data-stu-id="1a113-119">*dwReason*</span></span> 
</dt> <dd>

<span data-ttu-id="1a113-120">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="1a113-120">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a113-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a113-121">Return value</span></span>

<span data-ttu-id="1a113-122">Retourne toujours **false**.</span><span class="sxs-lookup"><span data-stu-id="1a113-122">Always returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a113-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a113-123">Requirements</span></span>



| <span data-ttu-id="1a113-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a113-124">Requirement</span></span> | <span data-ttu-id="1a113-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a113-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a113-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1a113-126">DLL</span></span><br/> | <dl> <span data-ttu-id="1a113-127"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a113-127"><dt>Kernel32.dll</dt></span></span> </dl> |



 

 




