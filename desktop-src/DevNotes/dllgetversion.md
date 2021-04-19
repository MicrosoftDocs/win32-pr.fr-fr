---
description: La fonction DllGetVersion récupère le numéro de version de Cabinet.dll à l’aide de la structure CABINETDLLVERSIONINFO.
ms.assetid: 93f6c29e-6a62-46c2-a42b-8270fe522494
title: DllGetVersion fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: e04fd8bc520f037c89912af730c537159867219e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528466"
---
# <a name="dllgetversion-function"></a><span data-ttu-id="3346a-103">DllGetVersion fonction)</span><span class="sxs-lookup"><span data-stu-id="3346a-103">DllGetVersion function</span></span>

<span data-ttu-id="3346a-104">\[Cette fonction n’étant plus prise en charge, son comportement ne peut pas être garanti.\]</span><span class="sxs-lookup"><span data-stu-id="3346a-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="3346a-105">La fonction **DllGetVersion** récupère le numéro de version de Cabinet.dll à l’aide de la structure [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="3346a-105">The **DllGetVersion** function retrieves the version number of Cabinet.dll using the [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="3346a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3346a-106">Syntax</span></span>


```C++
VOID WINAPI DllGetVersion(
   PCABINETDLLVERSIONINFO pcdvi
);
```



## <a name="parameters"></a><span data-ttu-id="3346a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3346a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3346a-108">*pcdvi*</span><span class="sxs-lookup"><span data-stu-id="3346a-108">*pcdvi*</span></span> 
</dt> <dd>

<span data-ttu-id="3346a-109">Pointeur vers la structure [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) qui contient les informations de version.</span><span class="sxs-lookup"><span data-stu-id="3346a-109">Pointer to the [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) structure that contains the version information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3346a-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3346a-110">Return value</span></span>

<span data-ttu-id="3346a-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3346a-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3346a-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3346a-112">Remarks</span></span>

<span data-ttu-id="3346a-113">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="3346a-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3346a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3346a-114">Requirements</span></span>



| <span data-ttu-id="3346a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3346a-115">Requirement</span></span> | <span data-ttu-id="3346a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3346a-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3346a-117">DLL</span><span class="sxs-lookup"><span data-stu-id="3346a-117">DLL</span></span><br/> | <dl> <span data-ttu-id="3346a-118"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3346a-118"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3346a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3346a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3346a-120">**CABINETDLLVERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="3346a-120">**CABINETDLLVERSIONINFO**</span></span>](cabinetdllversioninfo.md)
</dt> <dt>

[<span data-ttu-id="3346a-121">**GetDllVersion**</span><span class="sxs-lookup"><span data-stu-id="3346a-121">**GetDllVersion**</span></span>](getdllversion.md)
</dt> </dl>

 

 
