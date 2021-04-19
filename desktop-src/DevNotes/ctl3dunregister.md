---
description: Annule l’inscription d’une application en tant que client de CTL3D.
ms.assetid: 21990A79-F90D-4AE1-AB02-2B33583B47F5
title: Ctl3dUnregister fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnregister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85cd45062da9c01ef8af5a312a855bfaab6a6bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531075"
---
# <a name="ctl3dunregister-function"></a><span data-ttu-id="6fa01-103">Ctl3dUnregister fonction)</span><span class="sxs-lookup"><span data-stu-id="6fa01-103">Ctl3dUnregister function</span></span>

<span data-ttu-id="6fa01-104">Annule l’inscription d’une application en tant que client de CTL3D.</span><span class="sxs-lookup"><span data-stu-id="6fa01-104">Unregisters an application as a client of CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fa01-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fa01-105">Syntax</span></span>


```C++
BOOL Ctl3dUnregister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="6fa01-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fa01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fa01-107">*hinstApp*</span><span class="sxs-lookup"><span data-stu-id="6fa01-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="6fa01-108">Handle vers l’application dont l’inscription doit être annulée en tant que client.</span><span class="sxs-lookup"><span data-stu-id="6fa01-108">A handle to the application to be unregistered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fa01-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6fa01-109">Return value</span></span>

<span data-ttu-id="6fa01-110">Retourne la **valeur true** si l’inscription de l’application en tant que client de CTL3D est annulée. Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="6fa01-110">Returns **TRUE** if the application is unregistered as a client of CTL3D; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fa01-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6fa01-111">Remarks</span></span>

<span data-ttu-id="6fa01-112">Une application qui utilise CTL3D doit appeler cette fonction dans WinMain.</span><span class="sxs-lookup"><span data-stu-id="6fa01-112">An application that uses CTL3D should call this function in WinMain.</span></span>

<span data-ttu-id="6fa01-113">les effets 3D ne sont pas disponibles sur les systèmes qui ont une résolution inférieure à VGA.</span><span class="sxs-lookup"><span data-stu-id="6fa01-113">3D effects are not available on systems that have less than VGA resolution.</span></span>

<span data-ttu-id="6fa01-114">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="6fa01-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fa01-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fa01-115">Requirements</span></span>



| <span data-ttu-id="6fa01-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fa01-116">Requirement</span></span> | <span data-ttu-id="6fa01-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fa01-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa01-118">DLL</span><span class="sxs-lookup"><span data-stu-id="6fa01-118">DLL</span></span><br/> | <dl> <span data-ttu-id="6fa01-119"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fa01-119"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
