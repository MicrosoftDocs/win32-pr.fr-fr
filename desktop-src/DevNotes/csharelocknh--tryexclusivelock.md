---
description: Obtient un verrou exclusivement si aucun autre ne le contient actuellement.
ms.assetid: d655b89c-f2c8-4965-a21b-f539b1598296
title: 'CShareLockNH :: TryExclusiveLock, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.TryExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8465e247807c4229821acef552e0786a5604a3b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528717"
---
# <a name="csharelocknhtryexclusivelock-method"></a><span data-ttu-id="b466b-103">CShareLockNH :: TryExclusiveLock, méthode</span><span class="sxs-lookup"><span data-stu-id="b466b-103">CShareLockNH::TryExclusiveLock method</span></span>

<span data-ttu-id="b466b-104">Obtient un verrou exclusivement si aucun autre ne le contient actuellement.</span><span class="sxs-lookup"><span data-stu-id="b466b-104">Obtains a lock exclusively if no others are currently hold it.</span></span>

## <a name="syntax"></a><span data-ttu-id="b466b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b466b-105">Syntax</span></span>


```C++
BOOL TryExclusiveLock();
```



## <a name="parameters"></a><span data-ttu-id="b466b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b466b-106">Parameters</span></span>

<span data-ttu-id="b466b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b466b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b466b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b466b-108">Return value</span></span>

<span data-ttu-id="b466b-109">Retourne la **valeur true** si la fonction est réussie ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="b466b-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b466b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b466b-110">Remarks</span></span>

<span data-ttu-id="b466b-111">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="b466b-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b466b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b466b-112">Requirements</span></span>



| <span data-ttu-id="b466b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b466b-113">Requirement</span></span> | <span data-ttu-id="b466b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="b466b-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b466b-115">DLL</span><span class="sxs-lookup"><span data-stu-id="b466b-115">DLL</span></span><br/> | <dl> <span data-ttu-id="b466b-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b466b-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
