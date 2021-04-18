---
description: Obtient la durée, en minutes, depuis la dernière activité de l’utilisateur.
ms.assetid: 2d1e68ad-6f65-4e64-afbf-505b2c9d3423
title: GetIdleMinutes fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetIdleMinutes
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: da3064ea96eb8e9835ed1e9d2f564bf922d2f091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533016"
---
# <a name="getidleminutes-function"></a><span data-ttu-id="1a58f-103">GetIdleMinutes fonction)</span><span class="sxs-lookup"><span data-stu-id="1a58f-103">GetIdleMinutes function</span></span>

<span data-ttu-id="1a58f-104">\[Cette fonction n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="1a58f-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="1a58f-105">Utilisez plutôt la fonction **GetLastInputInfo** .\]</span><span class="sxs-lookup"><span data-stu-id="1a58f-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="1a58f-106">Obtient la durée, en minutes, depuis la dernière activité de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1a58f-106">Gets the length of time, in minutes, since the user's last activity.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a58f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a58f-107">Syntax</span></span>


```C++
DWORD WINAPI GetIdleMinutes(
   DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="1a58f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a58f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a58f-109">*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="1a58f-109">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="1a58f-110">Ce paramètre doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="1a58f-110">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a58f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a58f-111">Return value</span></span>

<span data-ttu-id="1a58f-112">Retourne le nombre de minutes depuis la dernière activité de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1a58f-112">Returns the number of minutes since the user's last activity.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a58f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="1a58f-113">Remarks</span></span>

<span data-ttu-id="1a58f-114">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="1a58f-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="1a58f-115">Cette fonction n’est pas exportée par nom ; Spécifiez l’ordinal 8 lors de l’appel de **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="1a58f-115">This function is not exported by name; specify ordinal 8 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a58f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a58f-116">Requirements</span></span>



| <span data-ttu-id="1a58f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a58f-117">Requirement</span></span> | <span data-ttu-id="1a58f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a58f-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a58f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="1a58f-119">DLL</span></span><br/> | <dl> <span data-ttu-id="1a58f-120"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a58f-120"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a58f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a58f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a58f-122">**GetLastInputInfo**</span><span class="sxs-lookup"><span data-stu-id="1a58f-122">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
