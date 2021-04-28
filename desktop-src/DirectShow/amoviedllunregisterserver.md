---
description: Fonction AMovieDllUnregisterServer-obsolète. Utilisez AMovieDllRegisterServer2 à la place.
ms.assetid: 80f52109-6239-4e3d-a395-eb69f5278cd2
title: AMovieDllUnregisterServer, fonction (DLLSETUP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllUnregisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df7fb34246249298efc143b7ccc8e6332540867c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099927"
---
# <a name="amoviedllunregisterserver-function"></a><span data-ttu-id="26bdf-104">AMovieDllUnregisterServer fonction)</span><span class="sxs-lookup"><span data-stu-id="26bdf-104">AMovieDllUnregisterServer function</span></span>

<span data-ttu-id="26bdf-105">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="26bdf-105">Obsolete.</span></span> <span data-ttu-id="26bdf-106">Utilisez [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="26bdf-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="26bdf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26bdf-107">Syntax</span></span>


```C++
HRESULT AMovieDllUnregisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="26bdf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26bdf-108">Parameters</span></span>

<span data-ttu-id="26bdf-109">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="26bdf-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="26bdf-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26bdf-110">Return value</span></span>

<span data-ttu-id="26bdf-111">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="26bdf-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="26bdf-112">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="26bdf-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="26bdf-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26bdf-113">Requirements</span></span>



| <span data-ttu-id="26bdf-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26bdf-114">Requirement</span></span> | <span data-ttu-id="26bdf-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="26bdf-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26bdf-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="26bdf-116">Header</span></span><br/>  | <dl> <span data-ttu-id="26bdf-117"><dt>DLLSETUP. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26bdf-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="26bdf-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="26bdf-118">Library</span></span><br/> | <dl> <span data-ttu-id="26bdf-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="26bdf-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26bdf-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26bdf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26bdf-121">**Fonctions de configuration des DLL**</span><span class="sxs-lookup"><span data-stu-id="26bdf-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




