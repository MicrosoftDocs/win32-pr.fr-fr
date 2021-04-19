---
description: Commence la surveillance de l’inactivité.
ms.assetid: fed5e4ae-2c2b-4b00-9230-b71aec9335c8
title: BeginIdleDetection fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BeginIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: 06cd016dc4102ef2f5b0f351aa4836a7f9980645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539943"
---
# <a name="beginidledetection-function"></a><span data-ttu-id="bdc87-103">BeginIdleDetection fonction)</span><span class="sxs-lookup"><span data-stu-id="bdc87-103">BeginIdleDetection function</span></span>

<span data-ttu-id="bdc87-104">\[Cette fonction n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="bdc87-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="bdc87-105">Utilisez plutôt la fonction **GetLastInputInfo** .\]</span><span class="sxs-lookup"><span data-stu-id="bdc87-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="bdc87-106">Commence la surveillance de l’inactivité.</span><span class="sxs-lookup"><span data-stu-id="bdc87-106">Begins monitoring inactivity.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdc87-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdc87-107">Syntax</span></span>


```C++
DWORD WINAPI BeginIdleDetection(
   _IDLECALLBACK pfnCallback,
   DWORD         dwIdleMin,
   DWORD         dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="bdc87-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdc87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdc87-109">*pfnCallback*</span><span class="sxs-lookup"><span data-stu-id="bdc87-109">*pfnCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="bdc87-110">Fonction appelée lorsque l’état inactif change.</span><span class="sxs-lookup"><span data-stu-id="bdc87-110">The function that is called when the idle state changes.</span></span> <span data-ttu-id="bdc87-111">Ce rappel est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="bdc87-111">This callback is defined as follows:</span></span>

``` syntax
typedef void (WINAPI* _IDLECALLBACK) (DWORD dwState);

#define STATE_USER_IDLE_BEGIN       1
#define STATE_USER_IDLE_END         2
```

</dd> <dt>

<span data-ttu-id="bdc87-112">*dwIdleMin*</span><span class="sxs-lookup"><span data-stu-id="bdc87-112">*dwIdleMin*</span></span> 
</dt> <dd>

<span data-ttu-id="bdc87-113">Nombre de minutes d’inactivité avant l’appel à la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="bdc87-113">The number of minutes of inactivity before the call is made to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="bdc87-114">*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="bdc87-114">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="bdc87-115">Ce paramètre doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="bdc87-115">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdc87-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bdc87-116">Return value</span></span>

<span data-ttu-id="bdc87-117">Retourne 0 si la fonction est réussie ; Sinon, elle retourne un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="bdc87-117">Returns 0 if the function succeeds; otherwise, it returns an error code.</span></span> <span data-ttu-id="bdc87-118">Par exemple, si *dwReserved* est autre chose que 0, **les \_ \_ données non valides** de l’erreur sont retournées.</span><span class="sxs-lookup"><span data-stu-id="bdc87-118">For example, if *dwReserved* is anything other than 0, **ERROR\_INVALID\_DATA** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdc87-119">Notes</span><span class="sxs-lookup"><span data-stu-id="bdc87-119">Remarks</span></span>

<span data-ttu-id="bdc87-120">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="bdc87-120">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="bdc87-121">Cette fonction n’est pas exportée par nom ; Spécifiez l’ordinal 3 lors de l’appel de **GetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="bdc87-121">This function is not exported by name; specify ordinal 3 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdc87-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdc87-122">Requirements</span></span>



| <span data-ttu-id="bdc87-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bdc87-123">Requirement</span></span> | <span data-ttu-id="bdc87-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdc87-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdc87-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bdc87-125">DLL</span></span><br/> | <dl> <span data-ttu-id="bdc87-126"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdc87-126"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdc87-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdc87-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdc87-128">**GetLastInputInfo**</span><span class="sxs-lookup"><span data-stu-id="bdc87-128">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
