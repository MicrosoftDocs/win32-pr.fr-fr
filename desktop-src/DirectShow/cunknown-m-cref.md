---
description: Nombre de références.
ms.assetid: be619a85-ca73-4cee-9df7-20e7be21853b
title: 'CUnknown :: m_cRef, membre (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_cRef
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94ff5d88ca48feeb46a8b0411a55d6261aefcf6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537830"
---
# <a name="cunknownm_cref-member"></a><span data-ttu-id="cb179-103">CUnknown :: m, \_ membre CREF</span><span class="sxs-lookup"><span data-stu-id="cb179-103">CUnknown::m\_cRef member</span></span>

<span data-ttu-id="cb179-104">Nombre de références.</span><span class="sxs-lookup"><span data-stu-id="cb179-104">Reference count.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb179-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb179-105">Syntax</span></span>


```C++
LONG m_cRef;
```



## <a name="remarks"></a><span data-ttu-id="cb179-106">Notes</span><span class="sxs-lookup"><span data-stu-id="cb179-106">Remarks</span></span>

<span data-ttu-id="cb179-107">Utilisez cette variable membre si vous substituez la méthode [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) ou [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md) .</span><span class="sxs-lookup"><span data-stu-id="cb179-107">Use this member variable if you override the [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) or [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb179-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb179-108">Requirements</span></span>



| <span data-ttu-id="cb179-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb179-109">Requirement</span></span> | <span data-ttu-id="cb179-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb179-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb179-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb179-111">Header</span></span><br/>  | <dl> <span data-ttu-id="cb179-112"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb179-112"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cb179-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cb179-113">Library</span></span><br/> | <dl> <span data-ttu-id="cb179-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cb179-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




