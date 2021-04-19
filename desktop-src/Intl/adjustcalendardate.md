---
description: Obsolète. Ajuste une date d’un nombre spécifié d’années, de mois, de semaines ou de jours.
ms.assetid: be8d61fd-efa3-4386-969f-30216c282ebc
title: AdjustCalendarDate fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdjustCalendarDate
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: ce2f61fd7d7d6354130873b5b2b2376c856e3958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516445"
---
# <a name="adjustcalendardate-function"></a><span data-ttu-id="971fd-104">AdjustCalendarDate fonction)</span><span class="sxs-lookup"><span data-stu-id="971fd-104">AdjustCalendarDate function</span></span>

<span data-ttu-id="971fd-105">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="971fd-105">Deprecated.</span></span> <span data-ttu-id="971fd-106">Ajuste une date d’un nombre spécifié d’années, de mois, de semaines ou de jours.</span><span class="sxs-lookup"><span data-stu-id="971fd-106">Adjusts a date by a specified number of years, months, weeks, or days.</span></span>

## <a name="syntax"></a><span data-ttu-id="971fd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="971fd-107">Syntax</span></span>


```C++
BOOL AdjustCalendarDate(
  _Inout_ LPCALDATETIME        lpCalDateTime,
  _In_    CALDATETIME_DATEUNIT calUnit,
  _Out_   INT                  amount
);
```



## <a name="parameters"></a><span data-ttu-id="971fd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="971fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="971fd-109">*lpCalDateTime* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="971fd-109">*lpCalDateTime* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="971fd-110">Pointeur vers une structure [**CALDATETIME**](caldatetime.md) qui contient les informations de date et de calendrier à ajuster.</span><span class="sxs-lookup"><span data-stu-id="971fd-110">Pointer to a [**CALDATETIME**](caldatetime.md) structure that contains the date and calendar information to adjust.</span></span>

</dd> <dt>

<span data-ttu-id="971fd-111">*calUnit* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="971fd-111">*calUnit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="971fd-112">Valeur d’énumération [**CALDATETIME \_ DATEUNIT**](caldatetime-dateunit.md) indiquant l’unité de date, par exemple, DayUnit.</span><span class="sxs-lookup"><span data-stu-id="971fd-112">The [**CALDATETIME\_DATEUNIT**](caldatetime-dateunit.md) enumeration value indicating the date unit, for example, DayUnit.</span></span>

</dd> <dt>

<span data-ttu-id="971fd-113">*quantité* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="971fd-113">*amount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="971fd-114">Valeur d’ajustement de la date spécifiée.</span><span class="sxs-lookup"><span data-stu-id="971fd-114">The amount by which to adjust the specified date.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="971fd-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="971fd-115">Return value</span></span>

<span data-ttu-id="971fd-116">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="971fd-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="971fd-117">Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="971fd-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="971fd-118">\_date \_ d’erreur \_ hors \_ limites.</span><span class="sxs-lookup"><span data-stu-id="971fd-118">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="971fd-119">La date spécifiée était hors limites.</span><span class="sxs-lookup"><span data-stu-id="971fd-119">The specified date was out of range.</span></span>
-   <span data-ttu-id="971fd-120">ERREUR \_ \_ : paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="971fd-120">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="971fd-121">Les valeurs de paramètre ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="971fd-121">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="971fd-122">Notes</span><span class="sxs-lookup"><span data-stu-id="971fd-122">Remarks</span></span>

<span data-ttu-id="971fd-123">Cette fonction n’a pas de fichier d’en-tête ou de fichier de bibliothèque associé.</span><span class="sxs-lookup"><span data-stu-id="971fd-123">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="971fd-124">L’application peut appeler [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) avec le nom de la DLL (Kernel32.dll) pour obtenir un handle de module.</span><span class="sxs-lookup"><span data-stu-id="971fd-124">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="971fd-125">Il peut ensuite appeler [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) avec le handle de module et le nom de cette fonction pour récupérer l’adresse de la fonction.</span><span class="sxs-lookup"><span data-stu-id="971fd-125">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="971fd-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="971fd-126">Requirements</span></span>



| <span data-ttu-id="971fd-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="971fd-127">Requirement</span></span> | <span data-ttu-id="971fd-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="971fd-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="971fd-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="971fd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="971fd-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="971fd-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="971fd-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="971fd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="971fd-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="971fd-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="971fd-133">DLL</span><span class="sxs-lookup"><span data-stu-id="971fd-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="971fd-134"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="971fd-134"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="971fd-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="971fd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="971fd-136">Prise en charge des langues nationales</span><span class="sxs-lookup"><span data-stu-id="971fd-136">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="971fd-137">Fonctions de prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="971fd-137">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="971fd-138">NLS : exemple d’API basées sur un nom</span><span class="sxs-lookup"><span data-stu-id="971fd-138">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
