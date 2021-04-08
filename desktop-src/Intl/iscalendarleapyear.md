---
description: Obsolète. Identifie si l’année spécifiée est une année bissextile au sein de l’ère donnée pour le calendrier spécifique.
ms.assetid: 91f58915-f0c6-4c7a-9d9a-96e255d799fd
title: IsCalendarLeapYear fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCalendarLeapYear
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 484531f8107bacb70f9e24ba2537090317825e26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865490"
---
# <a name="iscalendarleapyear-function"></a><span data-ttu-id="516f4-104">IsCalendarLeapYear fonction)</span><span class="sxs-lookup"><span data-stu-id="516f4-104">IsCalendarLeapYear function</span></span>

<span data-ttu-id="516f4-105">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="516f4-105">Deprecated.</span></span> <span data-ttu-id="516f4-106">Identifie si l’année spécifiée est une année bissextile au sein de l’ère donnée pour le calendrier spécifique.</span><span class="sxs-lookup"><span data-stu-id="516f4-106">Identifies whether the specified year is a leap year within the given era for the specific calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="516f4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="516f4-107">Syntax</span></span>


```C++
BOOL IsCalendarLeapYear(
  _In_ CALID calId,
  _In_ UINT  year,
  _In_ UINT  era
);
```



## <a name="parameters"></a><span data-ttu-id="516f4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="516f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="516f4-109">*calId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="516f4-109">*calId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="516f4-110">[Identificateur de calendrier](calendar-identifiers.md) à utiliser pour vérifier l’année bissextile.</span><span class="sxs-lookup"><span data-stu-id="516f4-110">The [calendar identifier](calendar-identifiers.md) to use for checking leap year.</span></span>

</dd> <dt>

<span data-ttu-id="516f4-111">*année* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="516f4-111">*year* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="516f4-112">Année à vérifier.</span><span class="sxs-lookup"><span data-stu-id="516f4-112">The year to check.</span></span>

</dd> <dt>

<span data-ttu-id="516f4-113">*ère* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="516f4-113">*era* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="516f4-114">L’ère à vérifier.</span><span class="sxs-lookup"><span data-stu-id="516f4-114">The era to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="516f4-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="516f4-115">Return value</span></span>

<span data-ttu-id="516f4-116">Retourne la **valeur true** si l’année spécifiée est une année bissextile, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="516f4-116">Returns **TRUE** if the specified year is a leap year, or **FALSE** otherwise.</span></span> <span data-ttu-id="516f4-117">Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="516f4-117">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="516f4-118">ERREUR \_ \_ : paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="516f4-118">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="516f4-119">Les valeurs de paramètre ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="516f4-119">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="516f4-120">Notes</span><span class="sxs-lookup"><span data-stu-id="516f4-120">Remarks</span></span>

<span data-ttu-id="516f4-121">Cette fonction n’a pas de fichier d’en-tête ou de fichier de bibliothèque associé.</span><span class="sxs-lookup"><span data-stu-id="516f4-121">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="516f4-122">L’application peut appeler [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) avec le nom de la DLL (Kernel32.dll) pour obtenir un handle de module.</span><span class="sxs-lookup"><span data-stu-id="516f4-122">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="516f4-123">Il peut ensuite appeler [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) avec ce handle de module et le nom de cette fonction pour recevoir l’adresse de la fonction.</span><span class="sxs-lookup"><span data-stu-id="516f4-123">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="516f4-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="516f4-124">Requirements</span></span>



| <span data-ttu-id="516f4-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="516f4-125">Requirement</span></span> | <span data-ttu-id="516f4-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="516f4-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="516f4-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="516f4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="516f4-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="516f4-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="516f4-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="516f4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="516f4-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="516f4-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="516f4-131">DLL</span><span class="sxs-lookup"><span data-stu-id="516f4-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="516f4-132"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="516f4-132"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="516f4-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="516f4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="516f4-134">Prise en charge des langues nationales</span><span class="sxs-lookup"><span data-stu-id="516f4-134">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="516f4-135">Fonctions de prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="516f4-135">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> </dl>

 

 
