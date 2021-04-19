---
description: La fonction IsWindowRedirectedForPrint détermine si la fenêtre spécifiée est actuellement redirigée pour l’impression.
ms.assetid: 49FD0D63-0F7F-48C6-81B6-25715294E7B7
title: IsWindowRedirectedForPrint fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsWindowRedirectedForPrint
api_type:
- DllExport
api_location:
- user32.dll
ms.openlocfilehash: b6648e5638ec6f05a2677ce279b0c3d7b160b49b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522417"
---
# <a name="iswindowredirectedforprint-function"></a><span data-ttu-id="21f1b-103">IsWindowRedirectedForPrint fonction)</span><span class="sxs-lookup"><span data-stu-id="21f1b-103">IsWindowRedirectedForPrint function</span></span>

<span data-ttu-id="21f1b-104">La fonction **IsWindowRedirectedForPrint** détermine si la fenêtre spécifiée est actuellement redirigée pour l’impression.</span><span class="sxs-lookup"><span data-stu-id="21f1b-104">The **IsWindowRedirectedForPrint** function determines whether the specified window is currently redirected for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="21f1b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21f1b-105">Syntax</span></span>


```C++
BOOL WINAPI IsWindowRedirectedForPrint(
  _In_   HWND hWnd
);
```



## <a name="parameters"></a><span data-ttu-id="21f1b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21f1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21f1b-107">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="21f1b-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f1b-108">Handle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="21f1b-108">The handle of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21f1b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="21f1b-109">Return value</span></span>

<span data-ttu-id="21f1b-110">Si la fenêtre est actuellement redirigée pour impression, la fonction retourne une valeur différente de zéro ; Sinon, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="21f1b-110">If the window is currently redirected for printing, the function returns a nonzero value; otherwise, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="21f1b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="21f1b-111">Remarks</span></span>

<span data-ttu-id="21f1b-112">Une fenêtre est redirigée pour impression quand elle traite un appel à [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow).</span><span class="sxs-lookup"><span data-stu-id="21f1b-112">A window is redirected for printing when it processes a call to [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow).</span></span> <span data-ttu-id="21f1b-113">Dans un appel à **PrintWindow**, une fenêtre affiche son contenu dans un contexte de périphérique hors écran.</span><span class="sxs-lookup"><span data-stu-id="21f1b-113">In a call to **PrintWindow**, a window renders its content to an off-screen device context.</span></span>

<span data-ttu-id="21f1b-114">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="21f1b-114">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="21f1b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21f1b-115">Requirements</span></span>



| <span data-ttu-id="21f1b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21f1b-116">Requirement</span></span> | <span data-ttu-id="21f1b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="21f1b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21f1b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21f1b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="21f1b-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21f1b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="21f1b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21f1b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="21f1b-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21f1b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="21f1b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="21f1b-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21f1b-123"><dt>User32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21f1b-123"><dt>User32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21f1b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21f1b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21f1b-125">**PrintWindow**</span><span class="sxs-lookup"><span data-stu-id="21f1b-125">**PrintWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-printwindow)
</dt> <dt>

[<span data-ttu-id="21f1b-126">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="21f1b-126">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="21f1b-127">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="21f1b-127">**LoadLibrary**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="21f1b-128">**\_impression WM**</span><span class="sxs-lookup"><span data-stu-id="21f1b-128">**WM\_PRINT**</span></span>](/windows/desktop/gdi/wm-print)
</dt> <dt>

[<span data-ttu-id="21f1b-129">**\_PRINTCLIENT WM**</span><span class="sxs-lookup"><span data-stu-id="21f1b-129">**WM\_PRINTCLIENT**</span></span>](/windows/desktop/gdi/wm-printclient)
</dt> </dl>

 

