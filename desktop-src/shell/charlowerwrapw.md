---
description: Convertit une chaîne de caractères Unicode ou un caractère unique en minuscules.
ms.assetid: 09b7cf8e-6aed-40f4-9dfa-29be3559ae89
title: CharLowerWrapW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharLowerWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 3911e0366d30f3eb9420391f9d06867ded73530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525401"
---
# <a name="charlowerwrapw-function"></a><span data-ttu-id="b97d7-103">CharLowerWrapW fonction)</span><span class="sxs-lookup"><span data-stu-id="b97d7-103">CharLowerWrapW function</span></span>

<span data-ttu-id="b97d7-104">\[**CharLowerWrapW** peut être utilisé dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b97d7-104">\[**CharLowerWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="b97d7-105">Elle n’est peut-être pas disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b97d7-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="b97d7-106">Vous devez utiliser [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="b97d7-106">You should use [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) in its place.\]</span></span>

<span data-ttu-id="b97d7-107">Convertit une chaîne de caractères Unicode ou un caractère unique en minuscules.</span><span class="sxs-lookup"><span data-stu-id="b97d7-107">Converts a Unicode character string or a single character to lowercase.</span></span> <span data-ttu-id="b97d7-108">Si l’opérande est une chaîne de caractères, la fonction convertit les caractères sur place.</span><span class="sxs-lookup"><span data-stu-id="b97d7-108">If the operand is a character string, the function converts the characters in place.</span></span>

> [!Note]  
> <span data-ttu-id="b97d7-109">**CharLowerWrapW** est un wrapper pour la fonction **CharLowerW** .</span><span class="sxs-lookup"><span data-stu-id="b97d7-109">**CharLowerWrapW** is a wrapper for the **CharLowerW** function.</span></span> <span data-ttu-id="b97d7-110">Pour plus d’informations sur les remarques d’utilisation, consultez la page [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera) .</span><span class="sxs-lookup"><span data-stu-id="b97d7-110">See the [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b97d7-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b97d7-111">Syntax</span></span>


```C++
LPWSTR CharLowerWrapW(
  _Inout_ LPWSTR pch
);
```



## <a name="parameters"></a><span data-ttu-id="b97d7-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b97d7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b97d7-113">*PCH* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b97d7-113">*pch* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b97d7-114">Type : **LPWStr**</span><span class="sxs-lookup"><span data-stu-id="b97d7-114">Type: **LPWSTR**</span></span>

<span data-ttu-id="b97d7-115">Pointeur vers une chaîne Unicode terminée par le caractère null ou un caractère unique.</span><span class="sxs-lookup"><span data-stu-id="b97d7-115">A pointer to a null-terminated Unicode string or a single character.</span></span> <span data-ttu-id="b97d7-116">Si le mot de poids fort de ce paramètre est égal à zéro, le mot de poids faible ne doit contenir qu’un seul caractère à convertir.</span><span class="sxs-lookup"><span data-stu-id="b97d7-116">If the high-order word of this parameter is zero, the low-order word must contain only a single character to be converted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b97d7-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b97d7-117">Return value</span></span>

<span data-ttu-id="b97d7-118">Type : **LPWStr**</span><span class="sxs-lookup"><span data-stu-id="b97d7-118">Type: **LPWSTR**</span></span>

<span data-ttu-id="b97d7-119">Si *PCH* est une chaîne de caractères, la fonction retourne un pointeur vers la chaîne convertie.</span><span class="sxs-lookup"><span data-stu-id="b97d7-119">If *pch* is a character string, the function returns a pointer to the converted string.</span></span> <span data-ttu-id="b97d7-120">Étant donné que la chaîne est convertie sur place, la valeur de retour est égale à *PCH*.</span><span class="sxs-lookup"><span data-stu-id="b97d7-120">Since the string is converted in place, the return value is equal to *pch*.</span></span>

<span data-ttu-id="b97d7-121">Si *PCH* est un caractère unique, la valeur de retour est une valeur 32 bits dont le mot de poids fort est égal à zéro et le mot de poids faible contient le caractère converti.</span><span class="sxs-lookup"><span data-stu-id="b97d7-121">If *pch* is a single character, the return value is a 32-bit value whose high-order word is zero, and low-order word contains the converted character.</span></span>

<span data-ttu-id="b97d7-122">Il n’existe aucune indication de réussite ou d’échec.</span><span class="sxs-lookup"><span data-stu-id="b97d7-122">There is no indication of success or failure.</span></span> <span data-ttu-id="b97d7-123">L’échec est rare.</span><span class="sxs-lookup"><span data-stu-id="b97d7-123">Failure is rare.</span></span> <span data-ttu-id="b97d7-124">Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="b97d7-124">There is no extended error information for this function; do not call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="b97d7-125">Notes</span><span class="sxs-lookup"><span data-stu-id="b97d7-125">Remarks</span></span>

<span data-ttu-id="b97d7-126">La méthode recommandée consiste à utiliser [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) conjointement avec la couche Microsoft pour Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="b97d7-126">The preferred method is to use [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="b97d7-127">**CharLowerWrapW** doit être appelé directement à partir de Shlwapi.dll, à l’aide de l’ordinal 38.</span><span class="sxs-lookup"><span data-stu-id="b97d7-127">**CharLowerWrapW** must be called directly from Shlwapi.dll, using ordinal 38.</span></span>

## <a name="requirements"></a><span data-ttu-id="b97d7-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b97d7-128">Requirements</span></span>



| <span data-ttu-id="b97d7-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b97d7-129">Requirement</span></span> | <span data-ttu-id="b97d7-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="b97d7-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b97d7-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b97d7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b97d7-132">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b97d7-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b97d7-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b97d7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b97d7-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b97d7-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b97d7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b97d7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b97d7-136"><dt>Shlwapi.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="b97d7-136"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b97d7-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b97d7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b97d7-138">**CharLower**</span><span class="sxs-lookup"><span data-stu-id="b97d7-138">**CharLower**</span></span>](/windows/win32/api/winuser/nf-winuser-charlowera)
</dt> </dl>

 

 
