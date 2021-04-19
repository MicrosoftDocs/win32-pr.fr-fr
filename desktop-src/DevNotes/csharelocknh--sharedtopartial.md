---
description: Remplace un verrou partagé par un verrou partiel.
ms.assetid: 82122671-b0bd-47ad-9a25-ee8ebd3779be
title: 'CShareLockNH :: SharedToPartial, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.SharedToPartial
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: a997c5a437063a4c55b74d837dc77fd506688158
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535959"
---
# <a name="csharelocknhsharedtopartial-method"></a><span data-ttu-id="d6553-103">CShareLockNH :: SharedToPartial, méthode</span><span class="sxs-lookup"><span data-stu-id="d6553-103">CShareLockNH::SharedToPartial method</span></span>

<span data-ttu-id="d6553-104">Remplace un verrou partagé par un verrou partiel.</span><span class="sxs-lookup"><span data-stu-id="d6553-104">Changes a shared lock to a partial lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6553-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6553-105">Syntax</span></span>


```C++
BOOL SharedToPartial();
```



## <a name="parameters"></a><span data-ttu-id="d6553-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6553-106">Parameters</span></span>

<span data-ttu-id="d6553-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d6553-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d6553-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d6553-108">Return value</span></span>

<span data-ttu-id="d6553-109">Retourne la **valeur true** si le verrou partiel est obtenu ; dans le cas contraire, elle retourne **false** et le verrou reste en mode partagé.</span><span class="sxs-lookup"><span data-stu-id="d6553-109">Returns **TRUE** if the partial lock is obtained; otherwise, it returns **FALSE** and the lock remains in shared mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6553-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d6553-110">Remarks</span></span>

<span data-ttu-id="d6553-111">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="d6553-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6553-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6553-112">Requirements</span></span>



| <span data-ttu-id="d6553-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6553-113">Requirement</span></span> | <span data-ttu-id="d6553-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6553-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d6553-115">DLL</span><span class="sxs-lookup"><span data-stu-id="d6553-115">DLL</span></span><br/> | <dl> <span data-ttu-id="d6553-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6553-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
