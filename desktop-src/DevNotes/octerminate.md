---
description: Ferme le gestionnaire OC.
ms.assetid: feba9954-03b2-4b57-b7ba-933e171751ff
title: OcTerminate fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcTerminate
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: 2e747c19db5e5a79e2827dc3bcfb88b97fae2ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532568"
---
# <a name="octerminate-function"></a><span data-ttu-id="eac34-103">OcTerminate fonction)</span><span class="sxs-lookup"><span data-stu-id="eac34-103">OcTerminate function</span></span>

<span data-ttu-id="eac34-104">Ferme le gestionnaire OC.</span><span class="sxs-lookup"><span data-stu-id="eac34-104">Closes the OC manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="eac34-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eac34-105">Syntax</span></span>


```C++
VOID OcTerminate(
  _Inout_ PVOID *OcManagerContext
);
```



## <a name="parameters"></a><span data-ttu-id="eac34-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eac34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eac34-107">*OcManagerContext* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eac34-107">*OcManagerContext* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eac34-108">En entrée, contient le pointeur de contexte du gestionnaire OC retourné par [**OcInitialize**](ocinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="eac34-108">On input, contains the OC manager context pointer returned by [**OcInitialize**](ocinitialize.md).</span></span> <span data-ttu-id="eac34-109">Lors de la sortie, reçoit la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="eac34-109">On output, receives **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eac34-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eac34-110">Return value</span></span>

<span data-ttu-id="eac34-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="eac34-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eac34-112">Notes</span><span class="sxs-lookup"><span data-stu-id="eac34-112">Remarks</span></span>

<span data-ttu-id="eac34-113">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="eac34-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="eac34-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eac34-114">Requirements</span></span>



| <span data-ttu-id="eac34-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eac34-115">Requirement</span></span> | <span data-ttu-id="eac34-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="eac34-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eac34-117">DLL</span><span class="sxs-lookup"><span data-stu-id="eac34-117">DLL</span></span><br/> | <dl> <span data-ttu-id="eac34-118"><dt>OcManage.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eac34-118"><dt>OcManage.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eac34-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eac34-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eac34-120">**OcInitialize**</span><span class="sxs-lookup"><span data-stu-id="eac34-120">**OcInitialize**</span></span>](ocinitialize.md)
</dt> </dl>

 

 
