---
description: Méthode de constructeur.
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: CMediaType. CMediaType, constructeur (mtype. h)-cmtype et PHR, paramètres
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
ms.openlocfilehash: a40929bb6f53df7ce721e20eefba3019eb71cb0e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106545723"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a><span data-ttu-id="2feff-103">Constructeur CMediaType. CMediaType (mtype. h)</span><span class="sxs-lookup"><span data-stu-id="2feff-103">CMediaType.CMediaType constructor (Mtype.h)</span></span>

<span data-ttu-id="2feff-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="2feff-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2feff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2feff-105">Syntax</span></span>


```C++
CMediaType(
  [ref] const CMediaType &cmtype,
              HRESULT    *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="2feff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2feff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2feff-107">*cmtype* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="2feff-107">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="2feff-108">Référence à un `CMediaType` objet.</span><span class="sxs-lookup"><span data-stu-id="2feff-108">Reference to a `CMediaType` object.</span></span> <span data-ttu-id="2feff-109">Le constructeur copie le type de média vers le nouvel objet, y compris le bloc de format, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="2feff-109">The constructor copies the media type to the new object, including the format block, if any.</span></span>

</dd> <dt>

<span data-ttu-id="2feff-110">*phr*</span><span class="sxs-lookup"><span data-stu-id="2feff-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="2feff-111">Pointeur vers une variable qui reçoit une valeur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="2feff-111">Pointer to a variable that receives an HRESULT value.</span></span> <span data-ttu-id="2feff-112">Ce paramètre peut être un pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="2feff-112">This parameter can be a **NULL** pointer.</span></span> <span data-ttu-id="2feff-113">Dans le cas contraire, l’appelant doit définir la valeur sur S \_ OK avant d’appeler le constructeur.</span><span class="sxs-lookup"><span data-stu-id="2feff-113">Otherwise, the caller must set the value to S\_OK before calling the constructor.</span></span> <span data-ttu-id="2feff-114">Si le constructeur échoue, il définit la valeur sur un code d’échec.</span><span class="sxs-lookup"><span data-stu-id="2feff-114">If the constructor fails, it sets the value to a failure code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2feff-115">Notes</span><span class="sxs-lookup"><span data-stu-id="2feff-115">Remarks</span></span>

<span data-ttu-id="2feff-116">Le constructeur appelle la méthode [**CMediaType :: InitMediaType**](cmediatype-initmediatype.md) pour initialiser le type de média.</span><span class="sxs-lookup"><span data-stu-id="2feff-116">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="2feff-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2feff-117">Requirements</span></span>



| <span data-ttu-id="2feff-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2feff-118">Requirement</span></span> | <span data-ttu-id="2feff-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2feff-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2feff-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="2feff-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2feff-121"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2feff-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="2feff-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2feff-122">Library</span></span><br/> | <dl> <span data-ttu-id="2feff-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2feff-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2feff-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2feff-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2feff-125">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="2feff-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




