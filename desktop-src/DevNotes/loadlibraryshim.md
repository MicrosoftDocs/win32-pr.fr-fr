---
description: Charge une version spécifiée d’une DLL de bibliothèque .NET Framework.
ms.assetid: f001774d-ea9a-4820-aec0-99ce958b1e1d
title: LoadLibraryShim, fonction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadLibraryShim
api_type:
- DllExport
api_location:
- Mscoree.dll
ms.openlocfilehash: 3a2fd8ab6aef8d0309748cbbf37d56ccd032b050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532919"
---
# <a name="loadlibraryshim-function"></a><span data-ttu-id="c678f-103">LoadLibraryShim, fonction</span><span class="sxs-lookup"><span data-stu-id="c678f-103">LoadLibraryShim function</span></span>

<span data-ttu-id="c678f-104">Charge une version spécifiée d’une DLL de bibliothèque .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c678f-104">Loads a specified version of a .NET Framework library DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="c678f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c678f-105">Syntax</span></span>


```C++
HRESULT LoadLibraryShim(
  _In_  LPCWSTR szDllName,
  _In_  LPCWSTR szVersion,
        LPVOID  pvReserved,
  _Out_ HMODULE *phModDll
);
```



## <a name="parameters"></a><span data-ttu-id="c678f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c678f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c678f-107">*szDllName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c678f-107">*szDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c678f-108">Nom de la DLL à charger à partir du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c678f-108">The name of the DLL to be loaded from the .NET Framework.</span></span>

</dd> <dt>

<span data-ttu-id="c678f-109">*szVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c678f-109">*szVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c678f-110">Version de la DLL à charger.</span><span class="sxs-lookup"><span data-stu-id="c678f-110">The version of the DLL to be loaded.</span></span> <span data-ttu-id="c678f-111">Si *szVersion* a la **valeur null**, la version la plus récente de la DLL spécifiée est chargée.</span><span class="sxs-lookup"><span data-stu-id="c678f-111">If *szVersion* is **NULL**, the latest version of the specified DLL is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="c678f-112">*pvReserved*</span><span class="sxs-lookup"><span data-stu-id="c678f-112">*pvReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="c678f-113">Réservé.</span><span class="sxs-lookup"><span data-stu-id="c678f-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c678f-114">*phModDll* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c678f-114">*phModDll* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c678f-115">Handle du module.</span><span class="sxs-lookup"><span data-stu-id="c678f-115">A handle to the module.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c678f-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c678f-116">Return value</span></span>

<span data-ttu-id="c678f-117">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c678f-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c678f-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c678f-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c678f-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c678f-119">Remarks</span></span>

<span data-ttu-id="c678f-120">Cette fonction est utilisée pour charger les dll de bibliothèque qui sont incluses dans le package redistribuable .NET Framework, et non des dll générées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c678f-120">This function is used to load library DLLs that are included in the .NET Framework redistributable package, not user-generated DLLs.</span></span>

<span data-ttu-id="c678f-121">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c678f-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c678f-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c678f-122">Requirements</span></span>



| <span data-ttu-id="c678f-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c678f-123">Requirement</span></span> | <span data-ttu-id="c678f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c678f-124">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c678f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c678f-125">DLL</span></span><br/> | <dl> <span data-ttu-id="c678f-126"><dt>Mscoree.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c678f-126"><dt>Mscoree.dll</dt></span></span> </dl> |



 

 
