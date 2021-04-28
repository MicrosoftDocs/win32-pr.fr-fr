---
description: Fonction AMovieDllRegisterServer-obsolète. Utilisez AMovieDllRegisterServer2 à la place.
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
ms.openlocfilehash: 81b6e73b1988d3eb97abdf9a5d2415ecbd62d8c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099937"
---
# <a name="amoviedllregisterserver-function"></a><span data-ttu-id="48f65-104">AMovieDllRegisterServer fonction)</span><span class="sxs-lookup"><span data-stu-id="48f65-104">AMovieDllRegisterServer function</span></span>

<span data-ttu-id="48f65-105">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="48f65-105">Obsolete.</span></span> <span data-ttu-id="48f65-106">Utilisez [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="48f65-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="48f65-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48f65-107">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="48f65-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48f65-108">Parameters</span></span>

<span data-ttu-id="48f65-109">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="48f65-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="48f65-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="48f65-110">Return value</span></span>

<span data-ttu-id="48f65-111">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="48f65-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="48f65-112">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="48f65-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="48f65-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48f65-113">Requirements</span></span>



| <span data-ttu-id="48f65-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48f65-114">Requirement</span></span> | <span data-ttu-id="48f65-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="48f65-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48f65-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="48f65-116">Header</span></span><br/>  | <dl> <span data-ttu-id="48f65-117"><dt>DLLSETUP. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48f65-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="48f65-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="48f65-118">Library</span></span><br/> | <dl> <span data-ttu-id="48f65-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="48f65-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48f65-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48f65-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48f65-121">**Fonctions de configuration des DLL**</span><span class="sxs-lookup"><span data-stu-id="48f65-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




