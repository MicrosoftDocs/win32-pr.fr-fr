---
description: Annule l’inscription d’une classe de fenêtre inscrite par LinkWindow \_ registerClass.
ms.assetid: 9e5c4326-efd1-43ca-a087-a436fe3f9bbd
title: LinkWindow_UnregisterClass fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_UnregisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 604cea299156444a1fedf34a46c50b5b397a65da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973382"
---
# <a name="linkwindow_unregisterclass-function"></a><span data-ttu-id="22eef-103">LinkWindow \_ fonction UnregisterClass</span><span class="sxs-lookup"><span data-stu-id="22eef-103">LinkWindow\_UnregisterClass function</span></span>

<span data-ttu-id="22eef-104">\[Cette fonction est disponible via Windows XP avec Service Pack 2 (SP2) et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="22eef-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="22eef-105">Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="22eef-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="22eef-106">Annule l’inscription d’une classe de fenêtre inscrite par [**LinkWindow \_ registerClass**](linkwindow-registerclass.md).</span><span class="sxs-lookup"><span data-stu-id="22eef-106">Unregisters a window class registered by [**LinkWindow\_RegisterClass**](linkwindow-registerclass.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="22eef-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22eef-107">Syntax</span></span>


```C++
BOOL LinkWindow_UnregisterClass(void);
```



## <a name="parameters"></a><span data-ttu-id="22eef-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22eef-108">Parameters</span></span>

<span data-ttu-id="22eef-109">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="22eef-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="22eef-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22eef-110">Return value</span></span>

<span data-ttu-id="22eef-111">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="22eef-111">Type: **BOOL**</span></span>

<span data-ttu-id="22eef-112">Retourne la **valeur true** si l’opération a réussi ; **False** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="22eef-112">Returns **TRUE** if the operation was successful; **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="22eef-113">Notes</span><span class="sxs-lookup"><span data-stu-id="22eef-113">Remarks</span></span>

<span data-ttu-id="22eef-114">Cette fonction n’a pas de fichier d’en-tête ou de bibliothèque associé et doit donc être appelée par valeur ordinale.</span><span class="sxs-lookup"><span data-stu-id="22eef-114">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="22eef-115">Appelez [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) avec le nom de la dll Shell32.dll pour obtenir un handle de module.</span><span class="sxs-lookup"><span data-stu-id="22eef-115">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name Shell32.dll to obtain a module handle.</span></span> <span data-ttu-id="22eef-116">Appelez ensuite [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) avec ce handle de module et le numéro ordinal 259 pour utiliser cette fonction.</span><span class="sxs-lookup"><span data-stu-id="22eef-116">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the ordinal number 259 to use this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="22eef-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="22eef-117">Requirements</span></span>



| <span data-ttu-id="22eef-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22eef-118">Requirement</span></span> | <span data-ttu-id="22eef-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="22eef-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22eef-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22eef-120">Minimum supported client</span></span><br/> | <span data-ttu-id="22eef-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22eef-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="22eef-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22eef-122">Minimum supported server</span></span><br/> | <span data-ttu-id="22eef-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22eef-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="22eef-124">DLL</span><span class="sxs-lookup"><span data-stu-id="22eef-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22eef-125"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="22eef-125"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22eef-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22eef-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22eef-127">Vue d’ensemble des contrôles SysLink</span><span class="sxs-lookup"><span data-stu-id="22eef-127">Overview of SysLink Controls</span></span>](../controls/syslink-overview.md)
</dt> </dl>

 

 
