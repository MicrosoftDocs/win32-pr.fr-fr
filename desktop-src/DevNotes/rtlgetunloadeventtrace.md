---
description: Permet au code de vidage d’obtenir les informations de module déchargées à partir de Ntdll.dll pour le stockage dans le minidump.
ms.assetid: 017398da-e13e-4261-bda5-6f400a91dbe3
title: RtlGetUnloadEventTrace fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTrace
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9297ba0019c89c5e93961d4b36e0fe16da04d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544474"
---
# <a name="rtlgetunloadeventtrace-function"></a><span data-ttu-id="e74cb-103">RtlGetUnloadEventTrace fonction)</span><span class="sxs-lookup"><span data-stu-id="e74cb-103">RtlGetUnloadEventTrace function</span></span>

<span data-ttu-id="e74cb-104">\[Cette fonction peut être modifiée ou supprimée de Windows sans préavis.\]</span><span class="sxs-lookup"><span data-stu-id="e74cb-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="e74cb-105">Permet au code de vidage d’obtenir les informations de module déchargées à partir de Ntdll.dll pour le stockage dans le minidump.</span><span class="sxs-lookup"><span data-stu-id="e74cb-105">Enables the dump code to get the unloaded module information from Ntdll.dll for storage in the minidump.</span></span>

## <a name="syntax"></a><span data-ttu-id="e74cb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e74cb-106">Syntax</span></span>


```C++
 PRTL_UNLOAD_EVENT_TRACE RtlGetUnloadEventTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="e74cb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e74cb-107">Parameters</span></span>

<span data-ttu-id="e74cb-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="e74cb-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e74cb-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e74cb-109">Return value</span></span>

<span data-ttu-id="e74cb-110">Cette fonction retourne un pointeur vers un tableau.</span><span class="sxs-lookup"><span data-stu-id="e74cb-110">This function returns a pointer to an array.</span></span> <span data-ttu-id="e74cb-111">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="e74cb-111">For more information, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="e74cb-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e74cb-112">Remarks</span></span>

<span data-ttu-id="e74cb-113">Le tableau RtlpUnloadEventTrace est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="e74cb-113">The RtlpUnloadEventTrace array is defined as follows:</span></span>

``` syntax
#define RTL_UNLOAD_EVENT_TRACE_NUMBER 64

typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;

RTL_UNLOAD_EVENT_TRACE RtlpUnloadEventTrace[RTL_UNLOAD_EVENT_TRACE_NUMBER];
```

<span data-ttu-id="e74cb-114">Cette fonction n’a aucun fichier d’en-tête associé.</span><span class="sxs-lookup"><span data-stu-id="e74cb-114">This function has no associated header file.</span></span> <span data-ttu-id="e74cb-115">La bibliothèque d’importation associée, ntdll. lib, est disponible dans le kit WDK (Windows Driver Kit).</span><span class="sxs-lookup"><span data-stu-id="e74cb-115">The associated import library, Ntdll.lib, is available in the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="e74cb-116">Vous pouvez également appeler cette fonction à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e74cb-116">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e74cb-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e74cb-117">Requirements</span></span>



| <span data-ttu-id="e74cb-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e74cb-118">Requirement</span></span> | <span data-ttu-id="e74cb-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e74cb-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e74cb-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e74cb-120">DLL</span></span><br/> | <dl> <span data-ttu-id="e74cb-121"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e74cb-121"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
