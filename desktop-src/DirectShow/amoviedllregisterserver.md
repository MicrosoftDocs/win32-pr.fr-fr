---
description: Obsolète. Utilisez AMovieDllRegisterServer2 à la place.
ms.assetid: d3be5fe0-f993-4a15-a3b8-3d761d51f289
title: AMovieDllRegisterServer, fonction (DLLSETUP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d93724c0f1ea6ed8b6cd2fa2b683a5ba9d45f0d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538133"
---
# <a name="amoviedllregisterserver-function"></a><span data-ttu-id="d1d7a-104">AMovieDllRegisterServer fonction)</span><span class="sxs-lookup"><span data-stu-id="d1d7a-104">AMovieDllRegisterServer function</span></span>

<span data-ttu-id="d1d7a-105">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="d1d7a-105">Obsolete.</span></span> <span data-ttu-id="d1d7a-106">Utilisez [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="d1d7a-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1d7a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1d7a-107">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="d1d7a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1d7a-108">Parameters</span></span>

<span data-ttu-id="d1d7a-109">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="d1d7a-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d1d7a-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1d7a-110">Return value</span></span>

<span data-ttu-id="d1d7a-111">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d1d7a-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d1d7a-112">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d1d7a-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1d7a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1d7a-113">Requirements</span></span>



| <span data-ttu-id="d1d7a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1d7a-114">Requirement</span></span> | <span data-ttu-id="d1d7a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1d7a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1d7a-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1d7a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d1d7a-117"><dt>DLLSETUP. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1d7a-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d1d7a-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d1d7a-118">Library</span></span><br/> | <dl> <span data-ttu-id="d1d7a-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d1d7a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1d7a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1d7a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1d7a-121">**Fonctions de configuration des DLL**</span><span class="sxs-lookup"><span data-stu-id="d1d7a-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




