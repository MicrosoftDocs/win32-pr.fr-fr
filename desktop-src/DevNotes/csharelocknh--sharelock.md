---
description: Obtient un verrou partagé.
ms.assetid: dff9a842-573a-4530-820d-6fd9001e502a
title: 'CShareLockNH :: ShareLock, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: d0c77564deceab29a8bee0cbffbd477559117cbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530501"
---
# <a name="csharelocknhsharelock-method"></a><span data-ttu-id="c1b52-103">CShareLockNH :: ShareLock, méthode</span><span class="sxs-lookup"><span data-stu-id="c1b52-103">CShareLockNH::ShareLock method</span></span>

<span data-ttu-id="c1b52-104">Obtient un verrou partagé.</span><span class="sxs-lookup"><span data-stu-id="c1b52-104">Obtains a shared lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1b52-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1b52-105">Syntax</span></span>


```C++
void ShareLock();
```



## <a name="parameters"></a><span data-ttu-id="c1b52-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1b52-106">Parameters</span></span>

<span data-ttu-id="c1b52-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c1b52-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c1b52-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c1b52-108">Return value</span></span>

<span data-ttu-id="c1b52-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c1b52-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1b52-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c1b52-110">Remarks</span></span>

<span data-ttu-id="c1b52-111">Chaque appel à **ShareLock** doit être associé à un seul appel à [**ShareUnlock**](csharelocknh--shareunlock.md).</span><span class="sxs-lookup"><span data-stu-id="c1b52-111">Each call to **ShareLock** must be paired with exactly one call to [**ShareUnlock**](csharelocknh--shareunlock.md).</span></span> <span data-ttu-id="c1b52-112">Seul un thread qui appelle avec succès **ShareLock** peut appeler **ShareUnlock**; dans le cas contraire, un interblocage peut se produire.</span><span class="sxs-lookup"><span data-stu-id="c1b52-112">Only a thread that successfully calls **ShareLock** can call **ShareUnlock**; otherwise, a deadlock can occur.</span></span>

<span data-ttu-id="c1b52-113">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c1b52-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1b52-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1b52-114">Requirements</span></span>



| <span data-ttu-id="c1b52-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1b52-115">Requirement</span></span> | <span data-ttu-id="c1b52-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1b52-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c1b52-117">DLL</span><span class="sxs-lookup"><span data-stu-id="c1b52-117">DLL</span></span><br/> | <dl> <span data-ttu-id="c1b52-118"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1b52-118"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1b52-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1b52-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1b52-120">**ShareUnlock**</span><span class="sxs-lookup"><span data-stu-id="c1b52-120">**ShareUnlock**</span></span>](csharelocknh--shareunlock.md)
</dt> </dl>

 

 
