---
description: Empêche plusieurs threads de terminer l’acquisition d’un verrou.
ms.assetid: 9cdcc6d5-b2f1-4c88-b859-1c15a80e70a9
title: CShareLockNH ::P méthode artialLock
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 0b7b7d55c9fd8d979aa14f12939df922e7a89099
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525446"
---
# <a name="csharelocknhpartiallock-method"></a><span data-ttu-id="a374c-103">CShareLockNH ::P méthode artialLock</span><span class="sxs-lookup"><span data-stu-id="a374c-103">CShareLockNH::PartialLock method</span></span>

<span data-ttu-id="a374c-104">Empêche plusieurs threads de terminer l’acquisition d’un verrou.</span><span class="sxs-lookup"><span data-stu-id="a374c-104">Prevents more than one thread from completing acquiring a lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="a374c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a374c-105">Syntax</span></span>


```C++
void PartialLock();
```



## <a name="parameters"></a><span data-ttu-id="a374c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a374c-106">Parameters</span></span>

<span data-ttu-id="a374c-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a374c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a374c-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a374c-108">Return value</span></span>

<span data-ttu-id="a374c-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a374c-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a374c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a374c-110">Remarks</span></span>

<span data-ttu-id="a374c-111">Alors que **PartialLock** est activé, les autres threads appelant [**ShareLock**](csharelocknh--sharelock.md) peuvent entrer le verrou.</span><span class="sxs-lookup"><span data-stu-id="a374c-111">While **PartialLock** is in effect, other threads calling [**ShareLock**](csharelocknh--sharelock.md) can enter the lock.</span></span>

<span data-ttu-id="a374c-112">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="a374c-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a374c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a374c-113">Requirements</span></span>



| <span data-ttu-id="a374c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a374c-114">Requirement</span></span> | <span data-ttu-id="a374c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a374c-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a374c-116">DLL</span><span class="sxs-lookup"><span data-stu-id="a374c-116">DLL</span></span><br/> | <dl> <span data-ttu-id="a374c-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a374c-117"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
