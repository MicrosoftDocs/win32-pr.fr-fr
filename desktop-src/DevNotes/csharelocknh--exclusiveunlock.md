---
description: Libère un verrou acquis à l’aide de ExclusiveLock en mode partagé.
ms.assetid: d38354f0-2eb3-4924-99b5-1331e587ce32
title: 'CShareLockNH :: ExclusiveUnlock, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: f5fae5d6131bfcb386d52880b530f3def9464442
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540021"
---
# <a name="csharelocknhexclusiveunlock-method"></a><span data-ttu-id="78f11-103">CShareLockNH :: ExclusiveUnlock, méthode</span><span class="sxs-lookup"><span data-stu-id="78f11-103">CShareLockNH::ExclusiveUnlock method</span></span>

<span data-ttu-id="78f11-104">Libère un verrou acquis à l’aide de [**ExclusiveLock**](csharelocknh--exclusivelock.md) en mode partagé.</span><span class="sxs-lookup"><span data-stu-id="78f11-104">Releases a lock acquired by using [**ExclusiveLock**](csharelocknh--exclusivelock.md) to shared mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="78f11-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78f11-105">Syntax</span></span>


```C++
void ExclusiveUnlock();
```



## <a name="parameters"></a><span data-ttu-id="78f11-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78f11-106">Parameters</span></span>

<span data-ttu-id="78f11-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="78f11-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="78f11-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="78f11-108">Return value</span></span>

<span data-ttu-id="78f11-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="78f11-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78f11-110">Notes</span><span class="sxs-lookup"><span data-stu-id="78f11-110">Remarks</span></span>

<span data-ttu-id="78f11-111">Chaque appel à [**ExclusiveLock**](csharelocknh--exclusivelock.md) doit être associé à un seul appel à **ExclusiveUnlock** pour éviter le risque d’un blocage.</span><span class="sxs-lookup"><span data-stu-id="78f11-111">Each call to [**ExclusiveLock**](csharelocknh--exclusivelock.md) must be paired with exactly one call to **ExclusiveUnlock** to avoid the risk of a deadlock.</span></span>

<span data-ttu-id="78f11-112">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="78f11-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="78f11-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78f11-113">Requirements</span></span>



| <span data-ttu-id="78f11-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78f11-114">Requirement</span></span> | <span data-ttu-id="78f11-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="78f11-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="78f11-116">DLL</span><span class="sxs-lookup"><span data-stu-id="78f11-116">DLL</span></span><br/> | <dl> <span data-ttu-id="78f11-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78f11-117"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78f11-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78f11-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78f11-119">**ExclusiveLock**</span><span class="sxs-lookup"><span data-stu-id="78f11-119">**ExclusiveLock**</span></span>](csharelocknh--exclusivelock.md)
</dt> </dl>

 

 
