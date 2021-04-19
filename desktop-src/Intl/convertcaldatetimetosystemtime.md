---
description: Obsolète. Convertit une structure CALDATETIME spécifiée en une structure SYSTEMTIME.
ms.assetid: 0c3f602d-62de-4c27-95d9-d35738f3279d
title: ConvertCalDateTimeToSystemTime fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertCalDateTimeToSystemTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 9c317a31904e2d1b0b2110f6b2dc367ac3e2e0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534295"
---
# <a name="convertcaldatetimetosystemtime-function"></a><span data-ttu-id="0e598-104">ConvertCalDateTimeToSystemTime fonction)</span><span class="sxs-lookup"><span data-stu-id="0e598-104">ConvertCalDateTimeToSystemTime function</span></span>

<span data-ttu-id="0e598-105">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0e598-105">Deprecated.</span></span> <span data-ttu-id="0e598-106">Convertit une structure [**CALDATETIME**](caldatetime.md) spécifiée en une structure [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="0e598-106">Converts a specified [**CALDATETIME**](caldatetime.md) structure to a [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e598-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e598-107">Syntax</span></span>


```C++
BOOL ConvertCalDateTimeToSystemTime(
  _In_  const LPCALDATETIME lpCalDateTime,
  _Out_       SYSTEMTIME    *lpSysTime
);
```



## <a name="parameters"></a><span data-ttu-id="0e598-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e598-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e598-109">*lpCalDateTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e598-109">*lpCalDateTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e598-110">Pointeur vers la structure [**CALDATETIME**](caldatetime.md) à convertir.</span><span class="sxs-lookup"><span data-stu-id="0e598-110">Pointer to the [**CALDATETIME**](caldatetime.md) structure to convert.</span></span>

</dd> <dt>

<span data-ttu-id="0e598-111">*lpSysTime* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0e598-111">*lpSysTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e598-112">Pointeur vers la structure [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) équivalente.</span><span class="sxs-lookup"><span data-stu-id="0e598-112">Pointer to the equivalent [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e598-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e598-113">Return value</span></span>

<span data-ttu-id="0e598-114">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0e598-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="0e598-115">Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="0e598-115">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="0e598-116">\_date \_ d’erreur \_ hors \_ limites.</span><span class="sxs-lookup"><span data-stu-id="0e598-116">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="0e598-117">La date spécifiée était hors limites.</span><span class="sxs-lookup"><span data-stu-id="0e598-117">The specified date was out of range.</span></span>
-   <span data-ttu-id="0e598-118">ERREUR \_ \_ : paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="0e598-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="0e598-119">Les valeurs de paramètre ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="0e598-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e598-120">Notes</span><span class="sxs-lookup"><span data-stu-id="0e598-120">Remarks</span></span>

<span data-ttu-id="0e598-121">Cette fonction n’a pas de fichier d’en-tête ou de fichier de bibliothèque associé.</span><span class="sxs-lookup"><span data-stu-id="0e598-121">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="0e598-122">L’application peut appeler [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) avec le nom de la DLL (Kernel32.dll) pour obtenir un handle de module.</span><span class="sxs-lookup"><span data-stu-id="0e598-122">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="0e598-123">Il peut ensuite appeler [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) avec le handle de module et le nom de cette fonction pour récupérer l’adresse de la fonction.</span><span class="sxs-lookup"><span data-stu-id="0e598-123">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e598-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e598-124">Requirements</span></span>



| <span data-ttu-id="0e598-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e598-125">Requirement</span></span> | <span data-ttu-id="0e598-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e598-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e598-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e598-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0e598-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e598-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0e598-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e598-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0e598-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e598-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0e598-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0e598-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e598-132"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e598-132"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e598-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e598-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e598-134">Prise en charge des langues nationales</span><span class="sxs-lookup"><span data-stu-id="0e598-134">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="0e598-135">Fonctions de prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="0e598-135">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="0e598-136">Récupération des informations de date et d’heure</span><span class="sxs-lookup"><span data-stu-id="0e598-136">Retrieving Time and Date Information</span></span>](time-and-date.md)
</dt> </dl>

 

 
