---
description: Récupère la taille et l’emplacement de la liste des modules déchargés de manière dynamique pour le processus en cours.
ms.assetid: 53ac9a7f-aa4a-412d-a6f7-a3a73bede5c2
title: RtlGetUnloadEventTraceEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTraceEx
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 05b9e076041d0cd2298799970670478e9d358d32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533162"
---
# <a name="rtlgetunloadeventtraceex-function"></a><span data-ttu-id="4b055-103">RtlGetUnloadEventTraceEx fonction)</span><span class="sxs-lookup"><span data-stu-id="4b055-103">RtlGetUnloadEventTraceEx function</span></span>

<span data-ttu-id="4b055-104">Récupère la taille et l’emplacement de la liste des modules déchargés de manière dynamique pour le processus en cours.</span><span class="sxs-lookup"><span data-stu-id="4b055-104">Retrieves the size and location of the dynamically unloaded module list for the current process.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b055-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b055-105">Syntax</span></span>


```C++
VOID WINAPI RtlGetUnloadEventTraceEx(
  _Out_ PULONG *ElementSize,
  _Out_ PULONG *ElementCount,
  _Out_ PVOID  *EventTrace
);
```



## <a name="parameters"></a><span data-ttu-id="4b055-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b055-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b055-107">*Éléments* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4b055-107">*ElementSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b055-108">Pointeur vers une variable qui contient la taille d’un élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="4b055-108">A pointer to a variable that contains the size of an element in the list.</span></span>

</dd> <dt>

<span data-ttu-id="4b055-109">*ElementCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4b055-109">*ElementCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b055-110">Pointeur vers une variable qui contient le nombre d’éléments dans la liste.</span><span class="sxs-lookup"><span data-stu-id="4b055-110">A pointer to a variable that contains the number of elements in the list.</span></span>

</dd> <dt>

<span data-ttu-id="4b055-111">*EventTrace* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4b055-111">*EventTrace* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b055-112">Pointeur vers un tableau de structures **de \_ \_ \_ trace d’événements de déchargement RTL** .</span><span class="sxs-lookup"><span data-stu-id="4b055-112">A pointer to an array of **RTL\_UNLOAD\_EVENT\_TRACE** structures.</span></span> <span data-ttu-id="4b055-113">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4b055-113">For more information, see Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b055-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4b055-114">Return value</span></span>

<span data-ttu-id="4b055-115">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4b055-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b055-116">Notes</span><span class="sxs-lookup"><span data-stu-id="4b055-116">Remarks</span></span>

<span data-ttu-id="4b055-117">Le chargeur stocke les informations sur les événements déchargés dans des emplacements pouvant être lus entre les processus en tirant parti du fait que Ntdll.dll est chargé à la même adresse de base dans tous les processus.</span><span class="sxs-lookup"><span data-stu-id="4b055-117">The loader stores unloaded event information in locations that can be read across processes by taking advantage of the fact that Ntdll.dll is loaded at the same base address in all processes.</span></span> <span data-ttu-id="4b055-118">Lorsqu’un débogueur doit interroger des informations de module déchargées, il appelle cette fonction pour déterminer l’adresse à laquelle les variables résident, puis interroge la mémoire virtuelle dans le processus cible à ces adresses pour lire les valeurs réelles.</span><span class="sxs-lookup"><span data-stu-id="4b055-118">When a debugger needs to query unloaded module information, it calls this function to determine the address at which the variables reside, then queries the virtual memory in the target process at those addresses to read the actual values.</span></span>

<span data-ttu-id="4b055-119">Chaque élément de la liste est défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="4b055-119">Each element in the list is defined as follows.</span></span>

``` syntax
typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;
```

<span data-ttu-id="4b055-120">Cette fonction n’a aucun fichier d’en-tête associé.</span><span class="sxs-lookup"><span data-stu-id="4b055-120">This function has no associated header file.</span></span> <span data-ttu-id="4b055-121">La bibliothèque d’importation associée, ntdll. lib, est disponible dans le kit WDK (Windows Driver Kit).</span><span class="sxs-lookup"><span data-stu-id="4b055-121">The associated import library, Ntdll.lib, is available in the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="4b055-122">Vous pouvez également appeler cette fonction à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4b055-122">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b055-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b055-123">Requirements</span></span>



| <span data-ttu-id="4b055-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b055-124">Requirement</span></span> | <span data-ttu-id="4b055-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b055-125">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4b055-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4b055-126">DLL</span></span><br/> | <dl> <span data-ttu-id="4b055-127"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b055-127"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
