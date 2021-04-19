---
description: En savoir plus sur la méthode du constructeur CMediaType. CMediaType (mtype. h). Cette méthode utilise le paramètre « MajorType ».
ms.assetid: 89356578-0509-46c1-abd4-421688017f1d
title: CMediaType. CMediaType, constructeur (mtype. h)-paramètre MajorType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a99717e41424a99b3c1e79674426fb14c5b57b9d
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "106540954"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---majortype-parameter"></a><span data-ttu-id="c99ce-104">CMediaType. CMediaType, constructeur (mtype. h)-paramètre MajorType</span><span class="sxs-lookup"><span data-stu-id="c99ce-104">CMediaType.CMediaType constructor (Mtype.h) - majortype parameter</span></span>

<span data-ttu-id="c99ce-105">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="c99ce-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c99ce-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c99ce-106">Syntax</span></span>


```C++
CMediaType(
   const GUID *majortype
);
```



## <a name="parameters"></a><span data-ttu-id="c99ce-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c99ce-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c99ce-108">*majortype*</span><span class="sxs-lookup"><span data-stu-id="c99ce-108">*majortype*</span></span> 
</dt> <dd>

<span data-ttu-id="c99ce-109">Pointeur vers un **GUID** de type principal.</span><span class="sxs-lookup"><span data-stu-id="c99ce-109">Pointer to a major type **GUID**.</span></span> <span data-ttu-id="c99ce-110">Le constructeur initialise le GUID de type principal à cette valeur.</span><span class="sxs-lookup"><span data-stu-id="c99ce-110">The constructor initializes the major type GUID to this value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c99ce-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c99ce-111">Remarks</span></span>

<span data-ttu-id="c99ce-112">Le constructeur appelle la méthode [**CMediaType :: InitMediaType**](cmediatype-initmediatype.md) pour initialiser le type de média.</span><span class="sxs-lookup"><span data-stu-id="c99ce-112">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c99ce-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c99ce-113">Requirements</span></span>

| <span data-ttu-id="c99ce-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c99ce-114">Requirement</span></span>                   | <span data-ttu-id="c99ce-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c99ce-115">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c99ce-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="c99ce-116">Header</span></span>  | <span data-ttu-id="c99ce-117">Mtype. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="c99ce-117">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="c99ce-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c99ce-118">Library</span></span> | <span data-ttu-id="c99ce-119">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="c99ce-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="c99ce-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c99ce-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c99ce-121">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="c99ce-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




