---
description: La fonction AMovieDllRegisterServer2 enregistre et annule l’enregistrement des filtres.
ms.assetid: 2122949d-0117-4c68-bfcd-c717b14dc970
title: AMovieDllRegisterServer2, fonction (DLLSETUP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec36290b7cad66b2b5f27633d30ae76c3331eba9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529974"
---
# <a name="amoviedllregisterserver2-function"></a><span data-ttu-id="9d7a4-103">AMovieDllRegisterServer2 fonction)</span><span class="sxs-lookup"><span data-stu-id="9d7a4-103">AMovieDllRegisterServer2 function</span></span>

<span data-ttu-id="9d7a4-104">La fonction **AMovieDllRegisterServer2** enregistre et annule l’enregistrement des filtres.</span><span class="sxs-lookup"><span data-stu-id="9d7a4-104">The **AMovieDllRegisterServer2** function registers and unregisters filters.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d7a4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d7a4-105">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer2(
   BOOL bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="9d7a4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d7a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d7a4-107">*bRegister*</span><span class="sxs-lookup"><span data-stu-id="9d7a4-107">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="9d7a4-108">**True** indique que le filtre est inscrit, **false** indique son annulation de son inscription.</span><span class="sxs-lookup"><span data-stu-id="9d7a4-108">**TRUE** indicates register the filter, **FALSE** indicates unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d7a4-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d7a4-109">Return value</span></span>

<span data-ttu-id="9d7a4-110">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9d7a4-110">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9d7a4-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9d7a4-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d7a4-112">Notes</span><span class="sxs-lookup"><span data-stu-id="9d7a4-112">Remarks</span></span>

<span data-ttu-id="9d7a4-113">Utilisez cette fonction pour configurer vos filtres.</span><span class="sxs-lookup"><span data-stu-id="9d7a4-113">Use this function to set up your filters.</span></span> <span data-ttu-id="9d7a4-114">Pour plus d’informations, consultez [comment inscrire des filtres DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="9d7a4-114">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d7a4-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d7a4-115">Requirements</span></span>



| <span data-ttu-id="9d7a4-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d7a4-116">Requirement</span></span> | <span data-ttu-id="9d7a4-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d7a4-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d7a4-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d7a4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9d7a4-119"><dt>DLLSETUP. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d7a4-119"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9d7a4-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9d7a4-120">Library</span></span><br/> | <dl> <span data-ttu-id="9d7a4-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9d7a4-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d7a4-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d7a4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d7a4-123">**Fonctions de configuration des DLL**</span><span class="sxs-lookup"><span data-stu-id="9d7a4-123">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




