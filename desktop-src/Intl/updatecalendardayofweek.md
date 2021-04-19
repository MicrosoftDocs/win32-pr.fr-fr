---
description: Obsolète. Obtient le jour de la semaine qui correspond à un jour spécifié et remplit le membre DayOfWeek dans la structure CALDATETIME spécifiée avec cette valeur.
ms.assetid: b9ae250a-73bb-4ec2-bb0d-e1f8b25c173c
title: UpdateCalendarDayOfWeek fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateCalendarDayOfWeek
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 316af539e6ca0476f0f8d575a160fcd7c3219e90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545163"
---
# <a name="updatecalendardayofweek-function"></a><span data-ttu-id="12a53-104">UpdateCalendarDayOfWeek fonction)</span><span class="sxs-lookup"><span data-stu-id="12a53-104">UpdateCalendarDayOfWeek function</span></span>

<span data-ttu-id="12a53-105">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="12a53-105">Deprecated.</span></span> <span data-ttu-id="12a53-106">Obtient le jour de la semaine qui correspond à un jour spécifié et remplit le membre **DayOfWeek** dans la structure [**CALDATETIME**](caldatetime.md) spécifiée avec cette valeur.</span><span class="sxs-lookup"><span data-stu-id="12a53-106">Gets the day of the week that corresponds to a specified day and populates the **DayOfWeek** member in the specified [**CALDATETIME**](caldatetime.md) structure with that value.</span></span>

## <a name="syntax"></a><span data-ttu-id="12a53-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12a53-107">Syntax</span></span>


```C++
BOOL UpdateCalendarDayOfWeek(
  _Inout_ LPCALDATETIME lpCalDateTime
);
```



## <a name="parameters"></a><span data-ttu-id="12a53-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12a53-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12a53-109">*lpCalDateTime* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="12a53-109">*lpCalDateTime* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="12a53-110">Pointeur vers la structure [**CALDATETIME**](caldatetime.md) contenant la date pour laquelle définir le jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="12a53-110">Pointer to the [**CALDATETIME**](caldatetime.md) structure containing the date for which to set the day of the week.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12a53-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12a53-111">Return value</span></span>

<span data-ttu-id="12a53-112">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="12a53-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="12a53-113">Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="12a53-113">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="12a53-114">\_date \_ d’erreur \_ hors \_ limites.</span><span class="sxs-lookup"><span data-stu-id="12a53-114">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="12a53-115">La date spécifiée était hors limites.</span><span class="sxs-lookup"><span data-stu-id="12a53-115">The specified date was out of range.</span></span>
-   <span data-ttu-id="12a53-116">ERREUR \_ \_ : paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="12a53-116">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="12a53-117">Les valeurs de paramètre ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="12a53-117">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="12a53-118">Notes</span><span class="sxs-lookup"><span data-stu-id="12a53-118">Remarks</span></span>

<span data-ttu-id="12a53-119">Cette fonction n’a pas de fichier d’en-tête ou de fichier de bibliothèque associé.</span><span class="sxs-lookup"><span data-stu-id="12a53-119">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="12a53-120">L’application peut appeler [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) avec le nom de la DLL (Kernel32.dll) pour obtenir un handle de module.</span><span class="sxs-lookup"><span data-stu-id="12a53-120">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="12a53-121">Il peut ensuite appeler [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) avec ce handle de module et le nom de cette fonction pour recevoir l’adresse de la fonction.</span><span class="sxs-lookup"><span data-stu-id="12a53-121">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="12a53-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12a53-122">Requirements</span></span>



| <span data-ttu-id="12a53-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12a53-123">Requirement</span></span> | <span data-ttu-id="12a53-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="12a53-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12a53-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12a53-125">Minimum supported client</span></span><br/> | <span data-ttu-id="12a53-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12a53-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="12a53-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12a53-127">Minimum supported server</span></span><br/> | <span data-ttu-id="12a53-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12a53-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="12a53-129">DLL</span><span class="sxs-lookup"><span data-stu-id="12a53-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12a53-130"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12a53-130"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12a53-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12a53-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12a53-132">Prise en charge des langues nationales</span><span class="sxs-lookup"><span data-stu-id="12a53-132">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="12a53-133">Fonctions de prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="12a53-133">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="12a53-134">**CALDATETIME**</span><span class="sxs-lookup"><span data-stu-id="12a53-134">**CALDATETIME**</span></span>](caldatetime.md)
</dt> </dl>

 

 
