---
description: La méthode SetFormat Initialise le bloc de format.
ms.assetid: 71f1c3d4-9c45-4124-8560-378c8f66e710
title: Méthode CMediaType. SetFormat (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08dd05faf514581a3325f4922076ba2053cd0c95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540531"
---
# <a name="cmediatypesetformat-method"></a><span data-ttu-id="a8b9b-103">Méthode CMediaType. SetFormat</span><span class="sxs-lookup"><span data-stu-id="a8b9b-103">CMediaType.SetFormat method</span></span>

<span data-ttu-id="a8b9b-104">La `SetFormat` méthode initialise le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="a8b9b-104">The `SetFormat` method initializes the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b9b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8b9b-105">Syntax</span></span>


```C++
BOOL SetFormat(
   BYTE  *pFormat,
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="a8b9b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8b9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8b9b-107">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="a8b9b-107">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="a8b9b-108">Pointeur vers un bloc de mémoire qui contient le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="a8b9b-108">Pointer to a block of memory that contains the format block.</span></span>

</dd> <dt>

<span data-ttu-id="a8b9b-109">*length*</span><span class="sxs-lookup"><span data-stu-id="a8b9b-109">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="a8b9b-110">Longueur du bloc de format, en octets.</span><span class="sxs-lookup"><span data-stu-id="a8b9b-110">Length of the format block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8b9b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a8b9b-111">Return value</span></span>

<span data-ttu-id="a8b9b-112">Retourne la **valeur true** en cas de réussite, ou **false** si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a8b9b-112">Returns **TRUE** if successful, or **FALSE** if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8b9b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a8b9b-113">Remarks</span></span>

<span data-ttu-id="a8b9b-114">Cette méthode alloue de la mémoire pour le bloc de format et copie la mémoire tampon spécifiée par *pFormat* dans le nouveau bloc de format.</span><span class="sxs-lookup"><span data-stu-id="a8b9b-114">This method allocates memory for the format block and copies the buffer specified by *pFormat* into the new format block.</span></span> <span data-ttu-id="a8b9b-115">Si le type de média contient déjà un bloc de format, l’ancien est libéré.</span><span class="sxs-lookup"><span data-stu-id="a8b9b-115">If the media type already contains a format block, the old one is released.</span></span> <span data-ttu-id="a8b9b-116">La méthode définit également le membre **cbFormat** de la structure du **\_ \_ type de média am** .</span><span class="sxs-lookup"><span data-stu-id="a8b9b-116">The method also sets the **cbFormat** member of the **AM\_MEDIA\_TYPE** structure.</span></span>

<span data-ttu-id="a8b9b-117">Pour définir le type de format, appelez la méthode [**CMediaType :: SetFormatType**](cmediatype-setformattype.md) .</span><span class="sxs-lookup"><span data-stu-id="a8b9b-117">To set the format type, call the [**CMediaType::SetFormatType**](cmediatype-setformattype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b9b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8b9b-118">Requirements</span></span>



| <span data-ttu-id="a8b9b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8b9b-119">Requirement</span></span> | <span data-ttu-id="a8b9b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8b9b-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b9b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8b9b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a8b9b-122"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8b9b-122"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="a8b9b-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a8b9b-123">Library</span></span><br/> | <dl> <span data-ttu-id="a8b9b-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a8b9b-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8b9b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8b9b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b9b-126">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="a8b9b-126">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




