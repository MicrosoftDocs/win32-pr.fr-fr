---
description: Acquiert un verrou en lecture/écriture.
ms.assetid: fd212dd9-034b-4e0c-9111-e3460ea6f133
title: 'CShareLockNH :: ExclusiveLock, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8b35b544c10e6dde2887e75971d747feade5517e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526408"
---
# <a name="csharelocknhexclusivelock-method"></a><span data-ttu-id="27751-103">CShareLockNH :: ExclusiveLock, méthode</span><span class="sxs-lookup"><span data-stu-id="27751-103">CShareLockNH::ExclusiveLock method</span></span>

<span data-ttu-id="27751-104">Acquiert un verrou en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="27751-104">Acquires a reader/writer lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="27751-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27751-105">Syntax</span></span>


```C++
void ExclusiveLock();
```



## <a name="parameters"></a><span data-ttu-id="27751-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27751-106">Parameters</span></span>

<span data-ttu-id="27751-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="27751-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="27751-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="27751-108">Return value</span></span>

<span data-ttu-id="27751-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="27751-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="27751-110">Notes</span><span class="sxs-lookup"><span data-stu-id="27751-110">Remarks</span></span>

<span data-ttu-id="27751-111">Chaque appel à **ExclusiveLock** doit être associé à un seul appel à [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) pour éviter le risque d’un blocage.</span><span class="sxs-lookup"><span data-stu-id="27751-111">Each call to **ExclusiveLock** must be paired with exactly one call to [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) to avoid the risk of a deadlock.</span></span>

<span data-ttu-id="27751-112">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="27751-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="27751-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27751-113">Requirements</span></span>



| <span data-ttu-id="27751-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27751-114">Requirement</span></span> | <span data-ttu-id="27751-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="27751-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="27751-116">DLL</span><span class="sxs-lookup"><span data-stu-id="27751-116">DLL</span></span><br/> | <dl> <span data-ttu-id="27751-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27751-117"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27751-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27751-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27751-119">**ExclusiveUnlock**</span><span class="sxs-lookup"><span data-stu-id="27751-119">**ExclusiveUnlock**</span></span>](csharelocknh--exclusiveunlock.md)
</dt> </dl>

 

 
