---
description: Permet à un débogueur d’examiner les informations de table de fonctions dynamiques.
ms.assetid: 32fd0dfd-ca7c-45e4-9d59-2b3318d7e13d
title: RtlGetFunctionTableListHead fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetFunctionTableListHead
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3dde476ee9958952d85c66816a113b92529aa13e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529942"
---
# <a name="rtlgetfunctiontablelisthead-function"></a><span data-ttu-id="ddff8-103">RtlGetFunctionTableListHead fonction)</span><span class="sxs-lookup"><span data-stu-id="ddff8-103">RtlGetFunctionTableListHead function</span></span>

<span data-ttu-id="ddff8-104">\[Cette fonction peut être modifiée ou supprimée de Windows sans préavis.\]</span><span class="sxs-lookup"><span data-stu-id="ddff8-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="ddff8-105">Permet à un débogueur d’examiner les informations de table de fonctions dynamiques.</span><span class="sxs-lookup"><span data-stu-id="ddff8-105">Enables a debugger to examine dynamic function table information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddff8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ddff8-106">Syntax</span></span>


```C++
PLIST_ENTRY RtlGetFunctionTableListHead(void);
```



## <a name="parameters"></a><span data-ttu-id="ddff8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ddff8-107">Parameters</span></span>

<span data-ttu-id="ddff8-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="ddff8-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ddff8-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ddff8-109">Return value</span></span>

<span data-ttu-id="ddff8-110">Retourne un pointeur vers le début de la liste de tables de fonctions.</span><span class="sxs-lookup"><span data-stu-id="ddff8-110">Returns a pointer to the head of the function table list.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddff8-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ddff8-111">Remarks</span></span>

<span data-ttu-id="ddff8-112">Notez que le fichier d’en-tête Windows Driver Kit (WDK) Ntdef. h est requis pour certaines définitions.</span><span class="sxs-lookup"><span data-stu-id="ddff8-112">Note that the Windows Driver Kit (WDK) header file Ntdef.h is required for some definitions.</span></span> <span data-ttu-id="ddff8-113">La bibliothèque d’importation associée, ntdll. lib, est disponible dans le kit WDK.</span><span class="sxs-lookup"><span data-stu-id="ddff8-113">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="ddff8-114">Vous pouvez également utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="ddff8-114">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddff8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddff8-115">Requirements</span></span>



| <span data-ttu-id="ddff8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddff8-116">Requirement</span></span> | <span data-ttu-id="ddff8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddff8-117">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ddff8-118">DLL</span><span class="sxs-lookup"><span data-stu-id="ddff8-118">DLL</span></span><br/> | <dl> <span data-ttu-id="ddff8-119"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddff8-119"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
