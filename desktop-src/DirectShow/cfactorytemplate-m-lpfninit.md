---
description: Pointeur vers une fonction qui est appelée à partir du point d’entrée de la DLL. Sa valeur peut être NULL.
ms.assetid: 0769f55b-6f0d-4a89-9d3f-64f211426342
title: 'CFactoryTemplate :: m_lpfnInit, membre (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnInit
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b44181f926f77ecc7cc22673622d4a0d3dcb7d26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534768"
---
# <a name="cfactorytemplatem_lpfninit-member"></a><span data-ttu-id="a4bb5-104">CFactoryTemplate :: m \_ lpfnInit, membre</span><span class="sxs-lookup"><span data-stu-id="a4bb5-104">CFactoryTemplate::m\_lpfnInit member</span></span>

<span data-ttu-id="a4bb5-105">Pointeur vers une fonction qui est appelée à partir du point d’entrée de la DLL.</span><span class="sxs-lookup"><span data-stu-id="a4bb5-105">Pointer to a function that gets called from the DLL entry point.</span></span> <span data-ttu-id="a4bb5-106">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a4bb5-106">Can be **NULL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4bb5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4bb5-107">Syntax</span></span>


```C++
LPFNInitRoutine m_lpfnInit;
```



## <a name="remarks"></a><span data-ttu-id="a4bb5-108">Notes</span><span class="sxs-lookup"><span data-stu-id="a4bb5-108">Remarks</span></span>

<span data-ttu-id="a4bb5-109">Le type de pointeur de fonction est [**LPFNInitRoutine**](lpfninitroutine.md).</span><span class="sxs-lookup"><span data-stu-id="a4bb5-109">The function pointer type is [**LPFNInitRoutine**](lpfninitroutine.md).</span></span> <span data-ttu-id="a4bb5-110">Si vous fournissez cette fonction dans votre DLL, la fonction de point d’entrée DLL l’appelle avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="a4bb5-110">If you provide this function in your DLL, the DLL entry-point function calls it with following parameters:</span></span>

-   <span data-ttu-id="a4bb5-111">*bLoading*: **true** lorsque la dll est chargée, **false** lorsque la dll est déchargée.</span><span class="sxs-lookup"><span data-stu-id="a4bb5-111">*bLoading*: **TRUE** when the DLL is loaded, **FALSE** when the DLL is unloaded.</span></span>
-   <span data-ttu-id="a4bb5-112">*rclsid*: pointeur vers CLISD de l’objet, spécifié dans la variable de membre [**CFactoryTemplate :: m \_ ClsID**](cfactorytemplate-m-clsid.md) .</span><span class="sxs-lookup"><span data-stu-id="a4bb5-112">*rclsid*: Pointer to the object's CLISD, specified in the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4bb5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4bb5-113">Requirements</span></span>



| <span data-ttu-id="a4bb5-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4bb5-114">Requirement</span></span> | <span data-ttu-id="a4bb5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4bb5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4bb5-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="a4bb5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a4bb5-117"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4bb5-117"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a4bb5-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a4bb5-118">Library</span></span><br/> | <dl> <span data-ttu-id="a4bb5-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a4bb5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4bb5-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4bb5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4bb5-121">**CFactoryTemplate, classe**</span><span class="sxs-lookup"><span data-stu-id="a4bb5-121">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




