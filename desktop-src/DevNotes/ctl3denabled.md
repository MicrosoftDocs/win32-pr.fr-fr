---
description: Vérifie si les contrôles peuvent utiliser des effets 3D.
ms.assetid: fb7b892f-2580-41ac-b2ef-938da3cc1dc2
title: Ctl3dEnabled fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dEnabled
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: d0eecec5650ecc00b69c0745e58a3e1d0f931a00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525604"
---
# <a name="ctl3denabled-function"></a><span data-ttu-id="95480-103">Ctl3dEnabled fonction)</span><span class="sxs-lookup"><span data-stu-id="95480-103">Ctl3dEnabled function</span></span>

<span data-ttu-id="95480-104">Vérifie si les contrôles peuvent utiliser des effets 3D.</span><span class="sxs-lookup"><span data-stu-id="95480-104">Verifies whether controls can use 3D effects.</span></span>

## <a name="syntax"></a><span data-ttu-id="95480-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95480-105">Syntax</span></span>


```C++
BOOL Ctl3dEnabled(void);
```



## <a name="parameters"></a><span data-ttu-id="95480-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95480-106">Parameters</span></span>

<span data-ttu-id="95480-107">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="95480-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="95480-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95480-108">Return value</span></span>

<span data-ttu-id="95480-109">Retourne la **valeur true** si les contrôles peuvent utiliser des effets 3D. Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="95480-109">Returns **TRUE** if controls can use 3D effects; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="95480-110">Notes</span><span class="sxs-lookup"><span data-stu-id="95480-110">Remarks</span></span>

<span data-ttu-id="95480-111">Dans Windows 4,0 ou version ultérieure, **Ctl3dEnabled** et [**Ctl3dRegister**](ctl3dregister.md) retournent **false**.</span><span class="sxs-lookup"><span data-stu-id="95480-111">In Windows 4.0 or later, **Ctl3dEnabled** and [**Ctl3dRegister**](ctl3dregister.md) return **FALSE**.</span></span>

<span data-ttu-id="95480-112">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="95480-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="95480-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95480-113">Requirements</span></span>



| <span data-ttu-id="95480-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95480-114">Requirement</span></span> | <span data-ttu-id="95480-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="95480-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95480-116">DLL</span><span class="sxs-lookup"><span data-stu-id="95480-116">DLL</span></span><br/> | <dl> <span data-ttu-id="95480-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95480-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
