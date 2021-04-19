---
description: Sous-classe et ajoute automatiquement des effets 3D à toutes les boîtes de dialogue de l’application.
ms.assetid: 96555052-c564-4cc7-9b24-e527f8e2f879
title: Ctl3dAutoSubclass fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85f4c85d1d608ff97147a935806b090162f5a78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525612"
---
# <a name="ctl3dautosubclass-function"></a><span data-ttu-id="c0648-103">Ctl3dAutoSubclass fonction)</span><span class="sxs-lookup"><span data-stu-id="c0648-103">Ctl3dAutoSubclass function</span></span>

<span data-ttu-id="c0648-104">Sous-classe et ajoute automatiquement des effets 3D à toutes les boîtes de dialogue de l’application.</span><span class="sxs-lookup"><span data-stu-id="c0648-104">Automatically subclasses and adds 3D effects to all dialog boxes in the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0648-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0648-105">Syntax</span></span>


```C++
PUBLIC BOOL FAR PASCAL Ctl3dAutoSubclass(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="c0648-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0648-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0648-107">*hinstApp*</span><span class="sxs-lookup"><span data-stu-id="c0648-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="c0648-108">Handle de l’application à inscrire en tant que client.</span><span class="sxs-lookup"><span data-stu-id="c0648-108">A handle to the application to be registered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0648-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c0648-109">Return value</span></span>

<span data-ttu-id="c0648-110">Retourne la **valeur true** , sauf si l’une des conditions suivantes existe, auquel cas elle retourne **false**:</span><span class="sxs-lookup"><span data-stu-id="c0648-110">Returns **TRUE** unless one of the following conditions exists, in which case it returns **FALSE**:</span></span>

-   <span data-ttu-id="c0648-111">CTL3D s’exécute sous Windows version 3,0 ou antérieure.</span><span class="sxs-lookup"><span data-stu-id="c0648-111">CTL3D is running under Windows version 3.0 or earlier.</span></span>
-   <span data-ttu-id="c0648-112">CTL3D n’a pas d’espace disponible dans ses tables pour l’application actuelle.</span><span class="sxs-lookup"><span data-stu-id="c0648-112">CTL3D does not have space available in its tables for the current application.</span></span> <span data-ttu-id="c0648-113">CTL3D peut traiter jusqu’à 32 applications en même temps.</span><span class="sxs-lookup"><span data-stu-id="c0648-113">CTL3D can service up to 32 applications at the same time.</span></span>
-   <span data-ttu-id="c0648-114">CTL3D ne peut pas installer son Hook CBT.</span><span class="sxs-lookup"><span data-stu-id="c0648-114">CTL3D cannot install its CBT hook.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0648-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c0648-115">Remarks</span></span>

<span data-ttu-id="c0648-116">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c0648-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0648-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0648-117">Requirements</span></span>



| <span data-ttu-id="c0648-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0648-118">Requirement</span></span> | <span data-ttu-id="c0648-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0648-119">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0648-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c0648-120">DLL</span></span><br/> | <dl> <span data-ttu-id="c0648-121"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0648-121"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
