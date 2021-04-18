---
description: Gère les modifications de couleurs système pour les applications qui utilisent CTL3D.
ms.assetid: b1eadb7d-39a5-47e9-9ae5-62bd33557f6b
title: Ctl3dColorChange fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dColorChange
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 7e7b0d4480fde480ea24a6c2c0dd8a7a849fbc75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540499"
---
# <a name="ctl3dcolorchange-function"></a><span data-ttu-id="186ab-103">Ctl3dColorChange fonction)</span><span class="sxs-lookup"><span data-stu-id="186ab-103">Ctl3dColorChange function</span></span>

<span data-ttu-id="186ab-104">Gère les modifications de couleurs système pour les applications qui utilisent CTL3D.</span><span class="sxs-lookup"><span data-stu-id="186ab-104">Handles system color changes for applications that use CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="186ab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="186ab-105">Syntax</span></span>


```C++
BOOL Ctl3dColorChange(void);
```



## <a name="parameters"></a><span data-ttu-id="186ab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="186ab-106">Parameters</span></span>

<span data-ttu-id="186ab-107">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="186ab-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="186ab-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="186ab-108">Return value</span></span>

<span data-ttu-id="186ab-109">Retourne la **valeur true** si la fonction est réussie ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="186ab-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="186ab-110">Notes</span><span class="sxs-lookup"><span data-stu-id="186ab-110">Remarks</span></span>

<span data-ttu-id="186ab-111">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="186ab-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="186ab-112">Cette fonction doit être appelée dans la procédure de fenêtre principale de l’application pour le message **WM \_ SYSCOLORCHANGE** , comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="186ab-112">This function should be called in the application's main window procedure for the **WM\_SYSCOLORCHANGE** message, as shown below.</span></span>

## <a name="examples"></a><span data-ttu-id="186ab-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="186ab-113">Examples</span></span>

``` syntax
case WM_SYSCOLORCHANGE:
   Ctl3dColorChange();
   break;
```

## <a name="requirements"></a><span data-ttu-id="186ab-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="186ab-114">Requirements</span></span>



| <span data-ttu-id="186ab-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="186ab-115">Requirement</span></span> | <span data-ttu-id="186ab-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="186ab-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="186ab-117">DLL</span><span class="sxs-lookup"><span data-stu-id="186ab-117">DLL</span></span><br/> | <dl> <span data-ttu-id="186ab-118"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="186ab-118"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
