---
description: Convertit une chaîne en GUID.
ms.assetid: 109b99e6-7409-44e0-932c-658be66651f4
title: Fonction GUIDFromString
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUIDFromString
- GUIDFromStringA
- GUIDFromStringW
api_type:
- DllExport
api_location:
- Shell32.dll
- API-MS-Win-shlwapi-ie-l1-1-0.dll
- shlwapi.dll
ms.openlocfilehash: a29a2138f4bcc7435a0d7864f65dd60ab16519c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864938"
---
# <a name="guidfromstring-function"></a><span data-ttu-id="37189-103">Fonction GUIDFromString</span><span class="sxs-lookup"><span data-stu-id="37189-103">GUIDFromString function</span></span>

<span data-ttu-id="37189-104">\[**GUIDFromString** est disponible via Windows XP avec Service Pack 2 (SP2) ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="37189-104">\[**GUIDFromString** is available through Windows XP with Service Pack 2 (SP2) or Windows Vista.</span></span> <span data-ttu-id="37189-105">Il peut être modifié ou non disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="37189-105">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="37189-106">Les applications doivent utiliser [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) ou [**échec iidfromstring**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) à la place de cette fonction.\]</span><span class="sxs-lookup"><span data-stu-id="37189-106">Applications should use [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) or [**IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) in place of this function.\]</span></span>

<span data-ttu-id="37189-107">Convertit une chaîne en GUID.</span><span class="sxs-lookup"><span data-stu-id="37189-107">Converts a string to a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="37189-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37189-108">Syntax</span></span>


```C++
BOOL GUIDFromString(
  _In_  LPCTSTR psz,
  _Out_ LPGUID  pguid
);
```



## <a name="parameters"></a><span data-ttu-id="37189-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37189-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37189-110">*PSZ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37189-110">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37189-111">Type : **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="37189-111">Type: **LPCTSTR**</span></span>

<span data-ttu-id="37189-112">Pointeur vers la chaîne se terminant par null à convertir.</span><span class="sxs-lookup"><span data-stu-id="37189-112">A pointer to the null-terminated string to convert.</span></span> <span data-ttu-id="37189-113">La chaîne doit se présenter sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="37189-113">The string should be in the following form:</span></span>

{00000000-0000-0000-0000-000000000000}

</dd> <dt>

<span data-ttu-id="37189-114">*pguid* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="37189-114">*pguid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37189-115">Type : **LPGUID**</span><span class="sxs-lookup"><span data-stu-id="37189-115">Type: **LPGUID**</span></span>

<span data-ttu-id="37189-116">Pointeur vers une mémoire tampon destinée à recevoir le GUID lorsque cette méthode est retournée.</span><span class="sxs-lookup"><span data-stu-id="37189-116">Pointer to a buffer to receive the GUID when this method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37189-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="37189-117">Return value</span></span>

<span data-ttu-id="37189-118">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="37189-118">Type: **BOOL**</span></span>

<span data-ttu-id="37189-119">**True** si le GUID a été créé avec succès ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="37189-119">**TRUE** if the GUID was created successfully; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="37189-120">Notes</span><span class="sxs-lookup"><span data-stu-id="37189-120">Remarks</span></span>

<span data-ttu-id="37189-121">Cette fonction n’est pas déclarée dans un en-tête ou exportée par nom à partir d’un fichier. dll.</span><span class="sxs-lookup"><span data-stu-id="37189-121">This function is not declared in a header or exported by name from a .dll file.</span></span> <span data-ttu-id="37189-122">Elle doit être chargée à partir de Shell32.dll en tant qu’ordinal 703 pour **GUIDFromStringA** et ordinal 704 pour **GUIDFromStringW**.</span><span class="sxs-lookup"><span data-stu-id="37189-122">It must be loaded from Shell32.dll as ordinal 703 for **GUIDFromStringA** and ordinal 704 for **GUIDFromStringW**.</span></span>

<span data-ttu-id="37189-123">Elle est également accessible à partir de Shlwapi.dll en tant qu’ordinal 269 pour **GUIDFromStringA** et ordinal 270 pour **GUIDFromStringW**.</span><span class="sxs-lookup"><span data-stu-id="37189-123">It can also be accessed from Shlwapi.dll as ordinal 269 for **GUIDFromStringA** and ordinal 270 for **GUIDFromStringW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="37189-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="37189-124">Requirements</span></span>



| <span data-ttu-id="37189-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37189-125">Requirement</span></span> | <span data-ttu-id="37189-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="37189-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37189-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37189-127">Minimum supported client</span></span><br/> | <span data-ttu-id="37189-128">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37189-128">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="37189-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37189-129">Minimum supported server</span></span><br/> | <span data-ttu-id="37189-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37189-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="37189-131">DLL</span><span class="sxs-lookup"><span data-stu-id="37189-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37189-132"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37189-132"><dt>Shell32.dll</dt></span></span> </dl> |
| <span data-ttu-id="37189-133">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="37189-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="37189-134">**GUIDFromStringW** (Unicode) et **GUIDFromStringA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="37189-134">**GUIDFromStringW** (Unicode) and **GUIDFromStringA** (ANSI)</span></span><br/>                |



 

 
