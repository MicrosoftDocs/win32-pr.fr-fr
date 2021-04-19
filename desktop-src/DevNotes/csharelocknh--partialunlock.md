---
description: Libère un verrou partiel afin que d’autres acquisitions de verrous exclusifs ou partiels puissent maintenant entrer.
ms.assetid: 95a3e0d1-4e8b-4e30-b4fd-709b9db465de
title: CShareLockNH ::P méthode artialUnlock
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 930c0f51e199c1668a70f2dd017b0280939b0710
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545448"
---
# <a name="csharelocknhpartialunlock-method"></a><span data-ttu-id="23848-103">CShareLockNH ::P méthode artialUnlock</span><span class="sxs-lookup"><span data-stu-id="23848-103">CShareLockNH::PartialUnlock method</span></span>

<span data-ttu-id="23848-104">Libère un verrou partiel afin que d’autres acquisitions de verrous exclusifs ou partiels puissent maintenant entrer.</span><span class="sxs-lookup"><span data-stu-id="23848-104">Releases a partial lock so that other exclusive or partial lock acquirers can now enter.</span></span>

## <a name="syntax"></a><span data-ttu-id="23848-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23848-105">Syntax</span></span>


```C++
void PartialUnlock();
```



## <a name="parameters"></a><span data-ttu-id="23848-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23848-106">Parameters</span></span>

<span data-ttu-id="23848-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="23848-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="23848-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="23848-108">Return value</span></span>

<span data-ttu-id="23848-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="23848-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="23848-110">Notes</span><span class="sxs-lookup"><span data-stu-id="23848-110">Remarks</span></span>

<span data-ttu-id="23848-111">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="23848-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="23848-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23848-112">Requirements</span></span>



| <span data-ttu-id="23848-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23848-113">Requirement</span></span> | <span data-ttu-id="23848-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="23848-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="23848-115">DLL</span><span class="sxs-lookup"><span data-stu-id="23848-115">DLL</span></span><br/> | <dl> <span data-ttu-id="23848-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23848-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
