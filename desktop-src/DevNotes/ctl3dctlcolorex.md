---
description: Gère le \_ message WM CTLCOLOR pour les applications qui utilisent CTL3D.
ms.assetid: 8626a559-4856-4e7d-bf9c-edc48613b8f4
title: Ctl3dCtlColorEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dCtlColorEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 57df7ed5e439d75b2edbf71e743cac069f0ed75b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544108"
---
# <a name="ctl3dctlcolorex-function"></a><span data-ttu-id="3cc1e-103">Ctl3dCtlColorEx fonction)</span><span class="sxs-lookup"><span data-stu-id="3cc1e-103">Ctl3dCtlColorEx function</span></span>

<span data-ttu-id="3cc1e-104">Gère le message **WM \_ CTLCOLOR** pour les applications qui utilisent CTL3D.</span><span class="sxs-lookup"><span data-stu-id="3cc1e-104">Handles the **WM\_CTLCOLOR** message for applications that use CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cc1e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cc1e-105">Syntax</span></span>


```C++
HBRUSH Ctl3dCtlColorEx(
   UINT   wm,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="3cc1e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3cc1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cc1e-107">*wm*</span><span class="sxs-lookup"><span data-stu-id="3cc1e-107">*wm*</span></span> 
</dt> <dd>

<span data-ttu-id="3cc1e-108">Message **WM \_ CTLCOLOR** pour l’application.</span><span class="sxs-lookup"><span data-stu-id="3cc1e-108">The **WM\_CTLCOLOR** message for the application.</span></span>

</dd> <dt>

<span data-ttu-id="3cc1e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3cc1e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3cc1e-110">Handle vers le contexte d’affichage (DC).</span><span class="sxs-lookup"><span data-stu-id="3cc1e-110">A handle to the display context (DC).</span></span>

</dd> <dt>

<span data-ttu-id="3cc1e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3cc1e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3cc1e-112">Handle d’une fenêtre enfant (contrôle).</span><span class="sxs-lookup"><span data-stu-id="3cc1e-112">A handle to a child window (control).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cc1e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3cc1e-113">Return value</span></span>

<span data-ttu-id="3cc1e-114">Retourne un handle au pinceau approprié si la fonction est réussie ; dans le cas contraire, elle retourne `(HBRUSH)(0)` indiquant qu’une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3cc1e-114">Returns a handle to the appropriate brush if the function succeeds; otherwise, it returns `(HBRUSH)(0)` indicating that an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cc1e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3cc1e-115">Remarks</span></span>

<span data-ttu-id="3cc1e-116">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="3cc1e-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cc1e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3cc1e-117">Requirements</span></span>



| <span data-ttu-id="3cc1e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3cc1e-118">Requirement</span></span> | <span data-ttu-id="3cc1e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="3cc1e-119">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cc1e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="3cc1e-120">DLL</span></span><br/> | <dl> <span data-ttu-id="3cc1e-121"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cc1e-121"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
