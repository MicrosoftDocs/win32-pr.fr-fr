---
description: Préfixe de chaque mémoire tampon, en octets.
ms.assetid: 471b73bf-f959-41aa-84ba-324a2738dd0e
title: 'Membre CBaseAllocator :: m_lPrefix (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lPrefix
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc52db44dcdfa050cf8bc7faf57cb7094d8cac91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541037"
---
# <a name="cbaseallocatorm_lprefix-member"></a><span data-ttu-id="67ad1-103">CBaseAllocator :: m \_ lPrefix, membre</span><span class="sxs-lookup"><span data-stu-id="67ad1-103">CBaseAllocator::m\_lPrefix member</span></span>

<span data-ttu-id="67ad1-104">Préfixe de chaque mémoire tampon, en octets.</span><span class="sxs-lookup"><span data-stu-id="67ad1-104">Prefix of each buffer, in bytes.</span></span> <span data-ttu-id="67ad1-105">Si la valeur est différente de zéro, chaque pointeur de mémoire tampon retourné par la méthode [**CBaseAllocator :: GetBuffer**](cbaseallocator-getbuffer.md) est précédé d’un bloc d’octets de taille *m \_ lPrefix*.</span><span class="sxs-lookup"><span data-stu-id="67ad1-105">If the value is non-zero, each buffer pointer returned by the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method is preceded by a block of bytes of size *m\_lPrefix*.</span></span> <span data-ttu-id="67ad1-106">Ce bloc de mémoire est appelé le *préfixe*.</span><span class="sxs-lookup"><span data-stu-id="67ad1-106">This memory block is called the *prefix*.</span></span> <span data-ttu-id="67ad1-107">La variable membre [**CBaseAllocator :: m \_ lSize**](cbaseallocator-m-lsize.md) n’inclut pas la valeur de préfixe.</span><span class="sxs-lookup"><span data-stu-id="67ad1-107">The [**CBaseAllocator::m\_lSize**](cbaseallocator-m-lsize.md) member variable does not include the prefix value.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ad1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67ad1-108">Syntax</span></span>


```C++
long m_lPrefix;
```



## <a name="requirements"></a><span data-ttu-id="67ad1-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67ad1-109">Requirements</span></span>



| <span data-ttu-id="67ad1-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67ad1-110">Requirement</span></span> | <span data-ttu-id="67ad1-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="67ad1-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67ad1-112">En-tête</span><span class="sxs-lookup"><span data-stu-id="67ad1-112">Header</span></span><br/>  | <dl> <span data-ttu-id="67ad1-113"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67ad1-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="67ad1-114">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="67ad1-114">Library</span></span><br/> | <dl> <span data-ttu-id="67ad1-115"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="67ad1-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67ad1-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67ad1-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ad1-117">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="67ad1-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




