---
description: Retourne la valeur actuelle d’un compteur de performance et, éventuellement, la fréquence du compteur de performance.
ms.assetid: ab8973b7-a358-4e50-85e8-9dbff4e67010
title: NtQueryPerformanceCounter fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryPerformanceCounter
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 5bf0aad74f6992212fb3b2238b3030c68cda2fc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532797"
---
# <a name="ntqueryperformancecounter-function"></a><span data-ttu-id="5ac26-103">NtQueryPerformanceCounter fonction)</span><span class="sxs-lookup"><span data-stu-id="5ac26-103">NtQueryPerformanceCounter function</span></span>

<span data-ttu-id="5ac26-104">\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="5ac26-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="5ac26-105">Utilisez les fonctions **QueryPerformanceCounter** et **QueryPerformanceFrequency** à la place.\]</span><span class="sxs-lookup"><span data-stu-id="5ac26-105">Use the **QueryPerformanceCounter** and **QueryPerformanceFrequency** functions instead.\]</span></span>

<span data-ttu-id="5ac26-106">Retourne la valeur actuelle d’un compteur de performance et, éventuellement, la fréquence du compteur de performance.</span><span class="sxs-lookup"><span data-stu-id="5ac26-106">Returns the current value of a performance counter and, optionally, the frequency of the performance counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ac26-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ac26-107">Syntax</span></span>


```C++
NTSTATUS NtQueryPerformanceCounter(
  _Out_     PLARGE_INTEGER PerformanceCounter,
  _Out_opt_ PLARGE_INTEGER PerformanceFrequency
);
```



## <a name="parameters"></a><span data-ttu-id="5ac26-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ac26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ac26-109">*PerformanceCounter* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5ac26-109">*PerformanceCounter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ac26-110">Adresse d’une variable devant recevoir la valeur actuelle du compteur de performance.</span><span class="sxs-lookup"><span data-stu-id="5ac26-110">The address of a variable to receive the current performance counter value.</span></span>

</dd> <dt>

<span data-ttu-id="5ac26-111">*Performancefrequency n'* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5ac26-111">*PerformanceFrequency* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5ac26-112">Adresse d’une variable qui doit recevoir la fréquence du compteur de performance.</span><span class="sxs-lookup"><span data-stu-id="5ac26-112">The address of a variable to receive the performance counter frequency.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ac26-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5ac26-113">Return value</span></span>

<span data-ttu-id="5ac26-114">Si la fonction réussit, elle retourne la **\_ réussite** de l’état du code **NTSTATUS** ; sinon, elle retourne un code d’erreur tel que **violation d' \_ accès \_ d’État**.</span><span class="sxs-lookup"><span data-stu-id="5ac26-114">If the function succeeds, it returns the **NTSTATUS** code **STATUS\_SUCCESS**; otherwise, it returns an error code such as **STATUS\_ACCESS\_VIOLATION**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ac26-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5ac26-115">Remarks</span></span>

<span data-ttu-id="5ac26-116">Aucun fichier d’en-tête n’est disponible pour **NtQueryPerformanceCounter**.</span><span class="sxs-lookup"><span data-stu-id="5ac26-116">No header file is available for **NtQueryPerformanceCounter**.</span></span> <span data-ttu-id="5ac26-117">Vous devez utiliser les autres fonctions nommées ci-dessus, bien que vous puissiez également utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="5ac26-117">You should use the alternative functions named above, although you can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

<span data-ttu-id="5ac26-118">La fréquence des performances correspond à la fréquence du compteur de performances en Hertz, en particulier en nombre par seconde.</span><span class="sxs-lookup"><span data-stu-id="5ac26-118">Performance frequency is the frequency of the performance counter in hertz, specifically in counts per second.</span></span> <span data-ttu-id="5ac26-119">Cette valeur dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="5ac26-119">This value is implementation dependent.</span></span> <span data-ttu-id="5ac26-120">Si l’implémentation n’a pas de matériel pour prendre en charge la synchronisation des performances, la valeur retournée est 0.</span><span class="sxs-lookup"><span data-stu-id="5ac26-120">If the implementation does not have hardware to support performance timing, the value returned is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ac26-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ac26-121">Requirements</span></span>



| <span data-ttu-id="5ac26-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ac26-122">Requirement</span></span> | <span data-ttu-id="5ac26-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ac26-123">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac26-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5ac26-124">DLL</span></span><br/> | <dl> <span data-ttu-id="5ac26-125"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ac26-125"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ac26-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ac26-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ac26-127">**QueryPerformanceCounter**</span><span class="sxs-lookup"><span data-stu-id="5ac26-127">**QueryPerformanceCounter**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> <dt>

[<span data-ttu-id="5ac26-128">**QueryPerformanceFrequency**</span><span class="sxs-lookup"><span data-stu-id="5ac26-128">**QueryPerformanceFrequency**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)
</dt> </dl>

 

 
