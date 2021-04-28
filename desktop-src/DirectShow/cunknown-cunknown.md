---
description: Méthode constructeur CUnknown. CUnknown.
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: Constructeur CUnknown. CUnknown (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32859871f8ef69ce357fe204f0741356314fbb06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084607"
---
# <a name="cunknowncunknown-constructor"></a><span data-ttu-id="aae98-103">Constructeur CUnknown. CUnknown</span><span class="sxs-lookup"><span data-stu-id="aae98-103">CUnknown.CUnknown constructor</span></span>

<span data-ttu-id="aae98-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="aae98-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aae98-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aae98-105">Syntax</span></span>


```C++
CUnknown(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="aae98-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aae98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aae98-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="aae98-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="aae98-108">Chaîne contenant le nom de l’objet. utilisé dans le constructeur [**CBaseObject**](cbaseobject.md) pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="aae98-108">String containing the name of the object; used in the [**CBaseObject**](cbaseobject.md) constructor for debugging.</span></span>

</dd> <dt>

<span data-ttu-id="aae98-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="aae98-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="aae98-110">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="aae98-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="aae98-111">Si l’objet est agrégé, passer un pointeur vers l’interface IUnknown de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="aae98-111">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="aae98-112">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="aae98-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aae98-113">Notes </span><span class="sxs-lookup"><span data-stu-id="aae98-113">Remarks</span></span>

<span data-ttu-id="aae98-114">L’objet est initialisé avec un nombre de références égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="aae98-114">The object is initialized with a reference count of zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="aae98-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aae98-115">Requirements</span></span>



| <span data-ttu-id="aae98-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aae98-116">Requirement</span></span> | <span data-ttu-id="aae98-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="aae98-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aae98-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="aae98-118">Header</span></span><br/>  | <dl> <span data-ttu-id="aae98-119"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aae98-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aae98-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="aae98-120">Library</span></span><br/> | <dl> <span data-ttu-id="aae98-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="aae98-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




