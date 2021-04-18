---
description: Inscrit une application en tant que client de CTL3D.
ms.assetid: 38a4a04a-6322-4eb8-b272-ae9b90f84e0f
title: Ctl3dRegister fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dRegister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 4b855c162d9d5f1c43a15d1ebd7219da6f847f37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528961"
---
# <a name="ctl3dregister-function"></a><span data-ttu-id="994f7-103">Ctl3dRegister fonction)</span><span class="sxs-lookup"><span data-stu-id="994f7-103">Ctl3dRegister function</span></span>

<span data-ttu-id="994f7-104">Inscrit une application en tant que client de CTL3D.</span><span class="sxs-lookup"><span data-stu-id="994f7-104">Registers an application as a client of CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="994f7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="994f7-105">Syntax</span></span>


```C++
BOOL Ctl3dRegister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="994f7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="994f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="994f7-107">*hinstApp*</span><span class="sxs-lookup"><span data-stu-id="994f7-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="994f7-108">Handle de l’application à inscrire en tant que client.</span><span class="sxs-lookup"><span data-stu-id="994f7-108">A handle to the application to be registered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="994f7-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="994f7-109">Return value</span></span>

<span data-ttu-id="994f7-110">Retourne la **valeur true** si les effets 3D sont actifs ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="994f7-110">Returns **TRUE** if 3D effects are active; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="994f7-111">Notes</span><span class="sxs-lookup"><span data-stu-id="994f7-111">Remarks</span></span>

<span data-ttu-id="994f7-112">Une application qui utilise CTL3D doit appeler cette fonction dans WinMain.</span><span class="sxs-lookup"><span data-stu-id="994f7-112">An application that uses CTL3D should call this function in WinMain.</span></span>

<span data-ttu-id="994f7-113">les effets 3D ne sont pas disponibles sur les systèmes qui ont une résolution inférieure à VGA.</span><span class="sxs-lookup"><span data-stu-id="994f7-113">3D effects are not available on systems that have less than VGA resolution.</span></span>

<span data-ttu-id="994f7-114">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="994f7-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="994f7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="994f7-115">Requirements</span></span>



| <span data-ttu-id="994f7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="994f7-116">Requirement</span></span> | <span data-ttu-id="994f7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="994f7-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="994f7-118">DLL</span><span class="sxs-lookup"><span data-stu-id="994f7-118">DLL</span></span><br/> | <dl> <span data-ttu-id="994f7-119"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="994f7-119"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
