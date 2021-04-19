---
description: Libère un verrou partagé.
ms.assetid: c2e9eb68-aacb-4196-b09e-d2748efb7fd6
title: 'CShareLockNH :: ShareUnlock, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 80c4311f4bf66000440dac38da6300888a8e5d59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534977"
---
# <a name="csharelocknhshareunlock-method"></a><span data-ttu-id="35d86-103">CShareLockNH :: ShareUnlock, méthode</span><span class="sxs-lookup"><span data-stu-id="35d86-103">CShareLockNH::ShareUnlock method</span></span>

<span data-ttu-id="35d86-104">Libère un verrou partagé.</span><span class="sxs-lookup"><span data-stu-id="35d86-104">Releases a shared lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="35d86-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35d86-105">Syntax</span></span>


```C++
void ShareUnlock();
```



## <a name="parameters"></a><span data-ttu-id="35d86-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35d86-106">Parameters</span></span>

<span data-ttu-id="35d86-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="35d86-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="35d86-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35d86-108">Return value</span></span>

<span data-ttu-id="35d86-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="35d86-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="35d86-110">Notes</span><span class="sxs-lookup"><span data-stu-id="35d86-110">Remarks</span></span>

<span data-ttu-id="35d86-111">Chaque appel à [**ShareLock**](csharelocknh--sharelock.md) doit être associé à un seul appel à **ShareUnlock**.</span><span class="sxs-lookup"><span data-stu-id="35d86-111">Each call to [**ShareLock**](csharelocknh--sharelock.md) must be paired with exactly one call to **ShareUnlock**.</span></span> <span data-ttu-id="35d86-112">Seul un thread qui appelle avec succès **ShareLock** peut appeler **ShareUnlock**; dans le cas contraire, un interblocage peut se produire.</span><span class="sxs-lookup"><span data-stu-id="35d86-112">Only a thread that successfully calls **ShareLock** can call **ShareUnlock**; otherwise, a deadlock can occur.</span></span>

<span data-ttu-id="35d86-113">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="35d86-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="35d86-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35d86-114">Requirements</span></span>



| <span data-ttu-id="35d86-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35d86-115">Requirement</span></span> | <span data-ttu-id="35d86-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="35d86-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="35d86-117">DLL</span><span class="sxs-lookup"><span data-stu-id="35d86-117">DLL</span></span><br/> | <dl> <span data-ttu-id="35d86-118"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35d86-118"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35d86-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35d86-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35d86-120">**ShareLock**</span><span class="sxs-lookup"><span data-stu-id="35d86-120">**ShareLock**</span></span>](csharelocknh--sharelock.md)
</dt> </dl>

 

 
