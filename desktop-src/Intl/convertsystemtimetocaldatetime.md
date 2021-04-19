---
description: Obsolète. Convertit une structure SYSTEMTIME spécifiée en une structure CALDATETIME.
ms.assetid: d21f75bc-1a93-4cb9-8b9b-6fa0e81886bf
title: ConvertSystemTimeToCalDateTime fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertSystemTimeToCalDateTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 738899c7307797f0edeade93f7e4e706919be900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534538"
---
# <a name="convertsystemtimetocaldatetime-function"></a><span data-ttu-id="da856-104">ConvertSystemTimeToCalDateTime fonction)</span><span class="sxs-lookup"><span data-stu-id="da856-104">ConvertSystemTimeToCalDateTime function</span></span>

<span data-ttu-id="da856-105">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="da856-105">Deprecated.</span></span> <span data-ttu-id="da856-106">Convertit une structure [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) spécifiée en une structure [**CALDATETIME**](caldatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="da856-106">Converts a specified [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure to a [**CALDATETIME**](caldatetime.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="da856-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da856-107">Syntax</span></span>


```C++
BOOL ConvertSystemTimeToCalDateTime(
  _In_  const SYSTEMTIME   *lpSysTime,
  _In_        CALID         calId,
  _Out_       LPCALDATETIME lpCalDateTime

);
```



## <a name="parameters"></a><span data-ttu-id="da856-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da856-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da856-109">*lpSysTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da856-109">*lpSysTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da856-110">Pointeur vers la structure [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) à convertir.</span><span class="sxs-lookup"><span data-stu-id="da856-110">Pointer to the [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure to convert.</span></span>

</dd> <dt>

<span data-ttu-id="da856-111">*calId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da856-111">*calId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da856-112">Identificateur de [calendrier](calendar-identifiers.md) système à utiliser lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="da856-112">The system [calendar identifier](calendar-identifiers.md) to use in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="da856-113">*lpCalDateTime* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="da856-113">*lpCalDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da856-114">Pointeur vers la structure [**CALDATETIME**](caldatetime.md) équivalente.</span><span class="sxs-lookup"><span data-stu-id="da856-114">Pointer to the equivalent [**CALDATETIME**](caldatetime.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da856-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da856-115">Return value</span></span>

<span data-ttu-id="da856-116">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="da856-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="da856-117">Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="da856-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="da856-118">ERREUR \_ \_ : paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="da856-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="da856-119">Les valeurs de paramètre ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="da856-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="da856-120">Notes</span><span class="sxs-lookup"><span data-stu-id="da856-120">Remarks</span></span>

<span data-ttu-id="da856-121">La première Date prise en charge par cette fonction est le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="da856-121">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="da856-122">Cette fonction n’a pas de fichier d’en-tête ou de fichier de bibliothèque associé.</span><span class="sxs-lookup"><span data-stu-id="da856-122">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="da856-123">L’application peut appeler [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) avec le nom de la DLL (Kernel32.dll) pour obtenir un handle de module.</span><span class="sxs-lookup"><span data-stu-id="da856-123">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="da856-124">Il peut ensuite appeler [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) avec le handle de module et le nom de cette fonction pour récupérer l’adresse de la fonction.</span><span class="sxs-lookup"><span data-stu-id="da856-124">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="da856-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da856-125">Requirements</span></span>



| <span data-ttu-id="da856-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da856-126">Requirement</span></span> | <span data-ttu-id="da856-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="da856-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da856-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da856-128">Minimum supported client</span></span><br/> | <span data-ttu-id="da856-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da856-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="da856-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da856-130">Minimum supported server</span></span><br/> | <span data-ttu-id="da856-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da856-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="da856-132">DLL</span><span class="sxs-lookup"><span data-stu-id="da856-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da856-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da856-133"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da856-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da856-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da856-135">Prise en charge des langues nationales</span><span class="sxs-lookup"><span data-stu-id="da856-135">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="da856-136">Fonctions de prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="da856-136">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="da856-137">Récupération des informations de date et d’heure</span><span class="sxs-lookup"><span data-stu-id="da856-137">Retrieving Time and Date Information</span></span>](time-and-date.md)
</dt> </dl>

 

 
