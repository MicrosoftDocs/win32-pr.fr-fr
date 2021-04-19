---
description: Affiche la boîte de dialogue Gestionnaire de clés dans l’interface utilisateur.
ms.assetid: 65c2763f-42d5-4534-94f7-e753f6486014
title: KRShowKeyMgr fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KRShowKeyMgr
api_type:
- DllExport
api_location:
- Keymgr.dll
ms.openlocfilehash: 59b6b38cf7e78755c7d5c481a22a0a8b3854c8a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530284"
---
# <a name="krshowkeymgr-function"></a><span data-ttu-id="8ee1b-103">KRShowKeyMgr fonction)</span><span class="sxs-lookup"><span data-stu-id="8ee1b-103">KRShowKeyMgr function</span></span>

<span data-ttu-id="8ee1b-104">\[Cette fonction est incluse uniquement dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8ee1b-104">\[This function is included only in Windows XP.</span></span> <span data-ttu-id="8ee1b-105">Il n’est pas inclus dans les autres versions de Windows et ne devrait pas être inclus dans les futures versions de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8ee1b-105">It is not currently included in any other version of Windows, nor is it expected to be included in any future versions of Windows.\]</span></span>

<span data-ttu-id="8ee1b-106">Affiche la boîte de dialogue Gestionnaire de clés dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8ee1b-106">Brings up the key manager dialog into the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ee1b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ee1b-107">Syntax</span></span>


```C++
void KRShowKeyMgr(
   HWND      hwParent,
   HINSTANCE hInstance,
   LPWSTR    pszCmdLine,
   int       CmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="8ee1b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ee1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ee1b-109">*hwParent*</span><span class="sxs-lookup"><span data-stu-id="8ee1b-109">*hwParent*</span></span> 
</dt> <dd>

<span data-ttu-id="8ee1b-110">Handle de la fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8ee1b-110">A handle to the parent window of the dialog.</span></span> <span data-ttu-id="8ee1b-111">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8ee1b-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8ee1b-112">*hInstance*</span><span class="sxs-lookup"><span data-stu-id="8ee1b-112">*hInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="8ee1b-113">Ce paramètre n’est pas utilisé et doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="8ee1b-113">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8ee1b-114">*pszCmdLine*</span><span class="sxs-lookup"><span data-stu-id="8ee1b-114">*pszCmdLine*</span></span> 
</dt> <dd>

<span data-ttu-id="8ee1b-115">Ce paramètre n’est pas utilisé et doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="8ee1b-115">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8ee1b-116">*CmdShow*</span><span class="sxs-lookup"><span data-stu-id="8ee1b-116">*CmdShow*</span></span> 
</dt> <dd>

<span data-ttu-id="8ee1b-117">Ce paramètre n’est pas utilisé et doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="8ee1b-117">This parameter is not used and should be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ee1b-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8ee1b-118">Return value</span></span>

<span data-ttu-id="8ee1b-119">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8ee1b-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ee1b-120">Notes</span><span class="sxs-lookup"><span data-stu-id="8ee1b-120">Remarks</span></span>

<span data-ttu-id="8ee1b-121">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="8ee1b-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ee1b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ee1b-122">Requirements</span></span>



| <span data-ttu-id="8ee1b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ee1b-123">Requirement</span></span> | <span data-ttu-id="8ee1b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ee1b-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee1b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8ee1b-125">DLL</span></span><br/> | <dl> <span data-ttu-id="8ee1b-126"><dt>Keymgr.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ee1b-126"><dt>Keymgr.dll</dt></span></span> </dl> |



 

 
