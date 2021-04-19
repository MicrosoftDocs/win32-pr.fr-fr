---
description: Pointeur vers l’allocateur qui a créé cet exemple.
ms.assetid: b4faccec-9124-4ae6-8662-ac5eb017328a
title: 'Membre CMediaSample :: m_pAllocator (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac2943c08b881badd8e15ea0633952ccc973a534
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541266"
---
# <a name="cmediasamplem_pallocator-member"></a><span data-ttu-id="f714c-103">CMediaSample :: m \_ pAllocator, membre</span><span class="sxs-lookup"><span data-stu-id="f714c-103">CMediaSample::m\_pAllocator member</span></span>

<span data-ttu-id="f714c-104">Pointeur vers l’allocateur qui a créé cet exemple.</span><span class="sxs-lookup"><span data-stu-id="f714c-104">Pointer to the allocator that created this sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="f714c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f714c-105">Syntax</span></span>


```C++
CBaseAllocator *m_pAllocator;
```



## <a name="remarks"></a><span data-ttu-id="f714c-106">Notes</span><span class="sxs-lookup"><span data-stu-id="f714c-106">Remarks</span></span>

<span data-ttu-id="f714c-107">Bien que l’exemple conserve un pointeur vers l’allocateur, il ne contient pas de décompte de références.</span><span class="sxs-lookup"><span data-stu-id="f714c-107">Although the sample keeps a pointer to the allocator, it does not hold a reference count.</span></span> <span data-ttu-id="f714c-108">Au lieu de cela, l’allocateur incrémente son propre nombre de références dans la méthode [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) et se libère dans la méthode [**IMemAllocator :: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) .</span><span class="sxs-lookup"><span data-stu-id="f714c-108">Instead, the allocator increments its own reference count in the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method, and releases itself in the [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method.</span></span> <span data-ttu-id="f714c-109">Cela garantit que l’allocateur sera disponible tant qu’un autre objet utilise l’exemple.</span><span class="sxs-lookup"><span data-stu-id="f714c-109">This guarantees that the allocator will be available as long as another object is using the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="f714c-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f714c-110">Requirements</span></span>



| <span data-ttu-id="f714c-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f714c-111">Requirement</span></span> | <span data-ttu-id="f714c-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="f714c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f714c-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="f714c-113">Header</span></span><br/>  | <dl> <span data-ttu-id="f714c-114"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f714c-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f714c-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f714c-115">Library</span></span><br/> | <dl> <span data-ttu-id="f714c-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f714c-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f714c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f714c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f714c-118">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="f714c-118">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




