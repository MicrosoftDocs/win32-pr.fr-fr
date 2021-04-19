---
description: Indique la version de CTL3D en cours d’exécution.
ms.assetid: 38c0842c-417f-4ca1-acc2-3bbadf45c804
title: Ctl3dGetVer fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dGetVer
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: e548d8933538ea85ba94f6e120032453079d69ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521694"
---
# <a name="ctl3dgetver-function"></a><span data-ttu-id="b7229-103">Ctl3dGetVer fonction)</span><span class="sxs-lookup"><span data-stu-id="b7229-103">Ctl3dGetVer function</span></span>

<span data-ttu-id="b7229-104">Indique la version de CTL3D en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="b7229-104">Indicates the version of CTL3D that is currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7229-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7229-105">Syntax</span></span>


```C++
WORD Ctl3dGetVer(void);
```



## <a name="parameters"></a><span data-ttu-id="b7229-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7229-106">Parameters</span></span>

<span data-ttu-id="b7229-107">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="b7229-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7229-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7229-108">Return value</span></span>

<span data-ttu-id="b7229-109">Retourne une valeur qui contient le numéro de version principale dans l’octet de poids fort et le numéro de version secondaire dans l’octet de poids faible.</span><span class="sxs-lookup"><span data-stu-id="b7229-109">Returns a value that contains the major version number in the high-order byte and the minor version number in the low-order byte.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7229-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b7229-110">Remarks</span></span>

<span data-ttu-id="b7229-111">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="b7229-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7229-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7229-112">Requirements</span></span>



| <span data-ttu-id="b7229-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7229-113">Requirement</span></span> | <span data-ttu-id="b7229-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7229-114">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7229-115">DLL</span><span class="sxs-lookup"><span data-stu-id="b7229-115">DLL</span></span><br/> | <dl> <span data-ttu-id="b7229-116"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7229-116"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
