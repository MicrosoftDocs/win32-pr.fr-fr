---
description: La fonction AMovieSetupRegisterFilter2 enregistre les mérites, les codes confidentiels et les types de média d’un filtre dans le registre à l’aide de l’interface IFilterMapper2.
ms.assetid: 8e0f3485-9e5d-4b22-853d-4ad9b1fb71d2
title: AMovieSetupRegisterFilter2, fonction (DLLSETUP. h)
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
ms.openlocfilehash: 272b781cf70f1dede9d4eea64b45d3d9d793a119
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528826"
---
# <a name="amoviesetupregisterfilter2-function"></a><span data-ttu-id="e94d4-103">AMovieSetupRegisterFilter2 fonction)</span><span class="sxs-lookup"><span data-stu-id="e94d4-103">AMovieSetupRegisterFilter2 function</span></span>

<span data-ttu-id="e94d4-104">La fonction **AMovieSetupRegisterFilter2** enregistre les mérites, les codes confidentiels et les types de média d’un filtre dans le registre à l’aide de l’interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .</span><span class="sxs-lookup"><span data-stu-id="e94d4-104">The **AMovieSetupRegisterFilter2** function registers a filter's merit, pins, and media types in the registry using the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e94d4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e94d4-105">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper2             *pIFM2,
         BOOL                       bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="e94d4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e94d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e94d4-107">*psetupdata*</span><span class="sxs-lookup"><span data-stu-id="e94d4-107">*psetupdata*</span></span> 
</dt> <dd>

<span data-ttu-id="e94d4-108">Pointeur vers les données de [**\_ filtre AMOVIESETUP**](amoviesetup-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="e94d4-108">Pointer to the [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) data.</span></span>

</dd> <dt>

<span data-ttu-id="e94d4-109">*pIFM2*</span><span class="sxs-lookup"><span data-stu-id="e94d4-109">*pIFM2*</span></span> 
</dt> <dd>

<span data-ttu-id="e94d4-110">Pointeur vers l’interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .</span><span class="sxs-lookup"><span data-stu-id="e94d4-110">Pointer to [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e94d4-111">*bRegister*</span><span class="sxs-lookup"><span data-stu-id="e94d4-111">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="e94d4-112">Valeur indiquant s’il faut inscrire le filtre ; **True** indique que le filtre est inscrit, **false** indique son annulation de son inscription.</span><span class="sxs-lookup"><span data-stu-id="e94d4-112">Value indicating whether to register the filter; **TRUE** indicates register the filter, **FALSE** indicates unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e94d4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e94d4-113">Return value</span></span>

<span data-ttu-id="e94d4-114">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e94d4-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e94d4-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e94d4-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e94d4-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e94d4-116">Remarks</span></span>

<span data-ttu-id="e94d4-117">La fonction [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) appelle cette fonction d’assistance pour inscrire un filtre après l’inscription du serveur com.</span><span class="sxs-lookup"><span data-stu-id="e94d4-117">The [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function calls this helper function to register a filter after the COM server has been registered.</span></span>

<span data-ttu-id="e94d4-118">En règle générale, un filtre utilise [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) et n’appelle pas cette fonction directement.</span><span class="sxs-lookup"><span data-stu-id="e94d4-118">Typically, a filter will use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) and will not call this function directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="e94d4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e94d4-119">Requirements</span></span>



| <span data-ttu-id="e94d4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e94d4-120">Requirement</span></span> | <span data-ttu-id="e94d4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e94d4-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e94d4-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e94d4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e94d4-123"><dt>DLLSETUP. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e94d4-123"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e94d4-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e94d4-124">Library</span></span><br/> | <dl> <span data-ttu-id="e94d4-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e94d4-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e94d4-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e94d4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e94d4-127">**Fonctions de configuration des DLL**</span><span class="sxs-lookup"><span data-stu-id="e94d4-127">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




