---
description: Obsolète. Obtient la plage de dates prise en charge pour un calendrier spécifié.
ms.assetid: fe036ac5-77c0-4e83-8d70-db3fa0f7c803
title: GetCalendarSupportedDateRange fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarSupportedDateRange
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 57b1175ef7bcf5b6b5d91af63682ca565bc0f1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952413"
---
# <a name="getcalendarsupporteddaterange-function"></a><span data-ttu-id="49902-104">GetCalendarSupportedDateRange fonction)</span><span class="sxs-lookup"><span data-stu-id="49902-104">GetCalendarSupportedDateRange function</span></span>

<span data-ttu-id="49902-105">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="49902-105">Deprecated.</span></span> <span data-ttu-id="49902-106">Obtient la plage de dates prise en charge pour un calendrier spécifié.</span><span class="sxs-lookup"><span data-stu-id="49902-106">Gets the supported date range for a specified calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="49902-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49902-107">Syntax</span></span>


```C++
BOOL GetCalendarSupportedDateRange(
  _In_  CALID         Calendar,
  _Out_ LPCALDATETIME lpCalMinDateTime,
  _Out_ LPCALDATETIME lpCalMaxDateTime
);
```



## <a name="parameters"></a><span data-ttu-id="49902-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49902-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49902-109">*Calendrier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49902-109">*Calendar* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49902-110">[Identificateur de calendrier](calendar-identifiers.md) pour lequel obtenir la plage de dates prise en charge.</span><span class="sxs-lookup"><span data-stu-id="49902-110">[Calendar identifier](calendar-identifiers.md) for which to get the supported date range.</span></span>

</dd> <dt>

<span data-ttu-id="49902-111">*lpCalMinDateTime* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="49902-111">*lpCalMinDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49902-112">Pointeur vers une structure [**CALDATETIME**](caldatetime.md) définissant la date de prise en charge minimale.</span><span class="sxs-lookup"><span data-stu-id="49902-112">Pointer to a [**CALDATETIME**](caldatetime.md) structure defining the minimum supported date.</span></span>

</dd> <dt>

<span data-ttu-id="49902-113">*lpCalMaxDateTime* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="49902-113">*lpCalMaxDateTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49902-114">Pointeur vers une structure [**CALDATETIME**](caldatetime.md) définissant la date maximale prise en charge.</span><span class="sxs-lookup"><span data-stu-id="49902-114">Pointer to a [**CALDATETIME**](caldatetime.md) structure defining the maximum supported date.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49902-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49902-115">Return value</span></span>

<span data-ttu-id="49902-116">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="49902-116">Returns **TRUE** if successful or **FALSE** otherwise.</span></span> <span data-ttu-id="49902-117">Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="49902-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="49902-118">ERREUR \_ \_ : paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="49902-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="49902-119">Les valeurs de paramètre ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="49902-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="49902-120">Notes</span><span class="sxs-lookup"><span data-stu-id="49902-120">Remarks</span></span>

<span data-ttu-id="49902-121">La première Date prise en charge par cette fonction est le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="49902-121">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="49902-122">Cette fonction n’a pas de fichier d’en-tête ou de fichier de bibliothèque associé.</span><span class="sxs-lookup"><span data-stu-id="49902-122">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="49902-123">L’application peut appeler [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) avec le nom de la DLL (Kernel32.dll) pour obtenir un handle de module.</span><span class="sxs-lookup"><span data-stu-id="49902-123">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="49902-124">Il peut ensuite appeler [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) avec le handle de module et le nom de cette fonction pour récupérer l’adresse de la fonction.</span><span class="sxs-lookup"><span data-stu-id="49902-124">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="49902-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49902-125">Requirements</span></span>



| <span data-ttu-id="49902-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49902-126">Requirement</span></span> | <span data-ttu-id="49902-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="49902-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49902-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49902-128">Minimum supported client</span></span><br/> | <span data-ttu-id="49902-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49902-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="49902-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49902-130">Minimum supported server</span></span><br/> | <span data-ttu-id="49902-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49902-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="49902-132">DLL</span><span class="sxs-lookup"><span data-stu-id="49902-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49902-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49902-133"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49902-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49902-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49902-135">Prise en charge des langues nationales</span><span class="sxs-lookup"><span data-stu-id="49902-135">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="49902-136">Fonctions de prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="49902-136">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="49902-137">NLS : exemple d’API basées sur un nom</span><span class="sxs-lookup"><span data-stu-id="49902-137">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
