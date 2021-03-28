---
description: Inscrit une classe de fenêtre qui permet d’utiliser le contrôle commun SysLink dans une fenêtre.
ms.assetid: 1e6dd741-81be-40bb-a8b5-d565f593c4e9
title: LinkWindow_RegisterClass fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_RegisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 7b5bfd2e1a45ff3f65df7cf3d3cae41bf4926aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973383"
---
# <a name="linkwindow_registerclass-function"></a><span data-ttu-id="103b7-103">LinkWindow \_ registerClass, fonction</span><span class="sxs-lookup"><span data-stu-id="103b7-103">LinkWindow\_RegisterClass function</span></span>

<span data-ttu-id="103b7-104">\[Cette fonction est disponible via Windows XP avec Service Pack 2 (SP2) et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="103b7-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="103b7-105">Il peut être modifié ou non disponible dans les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="103b7-105">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="103b7-106">Utilisez [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="103b7-106">Use [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) instead.\]</span></span>

<span data-ttu-id="103b7-107">Inscrit une classe de fenêtre qui permet d’utiliser le contrôle commun [Syslink](../controls/syslink-overview.md) dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="103b7-107">Registers a window class that allows for the [SysLink](../controls/syslink-overview.md) common control to be used in a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="103b7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="103b7-108">Syntax</span></span>


```C++
BOOL LinkWindow_RegisterClass(void);
```



## <a name="parameters"></a><span data-ttu-id="103b7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="103b7-109">Parameters</span></span>

<span data-ttu-id="103b7-110">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="103b7-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="103b7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="103b7-111">Return value</span></span>

<span data-ttu-id="103b7-112">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="103b7-112">Type: **BOOL**</span></span>

<span data-ttu-id="103b7-113">Retourne la **valeur true** si l’inscription a réussi ; **False** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="103b7-113">Returns **TRUE** if registration was successful; **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="103b7-114">Notes</span><span class="sxs-lookup"><span data-stu-id="103b7-114">Remarks</span></span>

<span data-ttu-id="103b7-115">Cette fonction n’a pas de fichier d’en-tête ou de bibliothèque associé et doit donc être appelée par valeur ordinale.</span><span class="sxs-lookup"><span data-stu-id="103b7-115">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="103b7-116">Appelez [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) avec le nom de la dll Shell32.dll pour obtenir un handle de module.</span><span class="sxs-lookup"><span data-stu-id="103b7-116">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name Shell32.dll to obtain a module handle.</span></span> <span data-ttu-id="103b7-117">Appelez ensuite [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) avec ce handle de module et le numéro ordinal 258 pour utiliser cette fonction.</span><span class="sxs-lookup"><span data-stu-id="103b7-117">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the ordinal number 258 to use this function.</span></span>

<span data-ttu-id="103b7-118">Utilisez [**LinkWindow \_ UnregisterClass**](linkwindow-unregisterclass.md) pour annuler l’inscription de la classe après utilisation.</span><span class="sxs-lookup"><span data-stu-id="103b7-118">Use [**LinkWindow\_UnregisterClass**](linkwindow-unregisterclass.md) to unregister the class after use.</span></span>

## <a name="requirements"></a><span data-ttu-id="103b7-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="103b7-119">Requirements</span></span>



| <span data-ttu-id="103b7-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="103b7-120">Requirement</span></span> | <span data-ttu-id="103b7-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="103b7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="103b7-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="103b7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="103b7-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="103b7-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="103b7-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="103b7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="103b7-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="103b7-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="103b7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="103b7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="103b7-127"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="103b7-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="103b7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="103b7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="103b7-129">Vue d’ensemble des contrôles SysLink</span><span class="sxs-lookup"><span data-stu-id="103b7-129">Overview of SysLink Controls</span></span>](../controls/syslink-overview.md)
</dt> </dl>

 

 
