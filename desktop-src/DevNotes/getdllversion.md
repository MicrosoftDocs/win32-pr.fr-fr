---
description: La fonction GetDllVersion récupère le numéro de version de Cabinet.dll.
ms.assetid: b324d5cd-1ede-473e-a10f-249c95eda057
title: GetDllVersion fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDllVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 1b1142bd2ece965a3f2fc58b6bb2f90586a8b391
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540398"
---
# <a name="getdllversion-function"></a><span data-ttu-id="0dbaa-103">GetDllVersion fonction)</span><span class="sxs-lookup"><span data-stu-id="0dbaa-103">GetDllVersion function</span></span>

<span data-ttu-id="0dbaa-104">\[Cette fonction n’étant plus prise en charge, son comportement ne peut pas être garanti.</span><span class="sxs-lookup"><span data-stu-id="0dbaa-104">\[This function is no longer supported, so its behavior cannot be guaranteed.</span></span> <span data-ttu-id="0dbaa-105">\]</span><span class="sxs-lookup"><span data-stu-id="0dbaa-105">\]</span></span>

<span data-ttu-id="0dbaa-106">La fonction **GetDllVersion** récupère le numéro de version de Cabinet.dll.</span><span class="sxs-lookup"><span data-stu-id="0dbaa-106">The **GetDllVersion** function retrieves the version number of Cabinet.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dbaa-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0dbaa-107">Syntax</span></span>


```C++
LPCSTR WINAPI GetDllVersion(void);
```



## <a name="parameters"></a><span data-ttu-id="0dbaa-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0dbaa-108">Parameters</span></span>

<span data-ttu-id="0dbaa-109">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="0dbaa-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0dbaa-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0dbaa-110">Return value</span></span>

<span data-ttu-id="0dbaa-111">Numéro de version du fichier (consultez la [ressource VERSIONINFO](../menurc/versioninfo-resource.md)).</span><span class="sxs-lookup"><span data-stu-id="0dbaa-111">The version number of the file (see [VERSIONINFO Resource](../menurc/versioninfo-resource.md)).</span></span>

## <a name="remarks"></a><span data-ttu-id="0dbaa-112">Notes</span><span class="sxs-lookup"><span data-stu-id="0dbaa-112">Remarks</span></span>

<span data-ttu-id="0dbaa-113">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="0dbaa-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dbaa-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0dbaa-114">Requirements</span></span>



| <span data-ttu-id="0dbaa-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0dbaa-115">Requirement</span></span> | <span data-ttu-id="0dbaa-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0dbaa-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0dbaa-117">DLL</span><span class="sxs-lookup"><span data-stu-id="0dbaa-117">DLL</span></span><br/> | <dl> <span data-ttu-id="0dbaa-118"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dbaa-118"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dbaa-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0dbaa-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dbaa-120">**DllGetVersion**</span><span class="sxs-lookup"><span data-stu-id="0dbaa-120">**DllGetVersion**</span></span>](dllgetversion.md)
</dt> </dl>

 

 
