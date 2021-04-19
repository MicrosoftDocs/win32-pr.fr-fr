---
description: Méthode de constructeur.
ms.assetid: 48143a61-5ba7-4bf9-bffa-244f2769144d
title: Constructeur CPersistStream. CPersistStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.CPersistStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cdb736a191f64099b8c0310a5b3ac3dad3cbe0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545512"
---
# <a name="cpersiststreamcpersiststream-constructor"></a><span data-ttu-id="01408-103">Constructeur CPersistStream. CPersistStream</span><span class="sxs-lookup"><span data-stu-id="01408-103">CPersistStream.CPersistStream constructor</span></span>

<span data-ttu-id="01408-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="01408-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="01408-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01408-105">Syntax</span></span>


```C++
CPersistStream(
   IUnknown *pUnk,
   HRESULT  *phr
);
```



## <a name="parameters"></a><span data-ttu-id="01408-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01408-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01408-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="01408-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="01408-108">Pointeur vers l’interface **IUnknown** de l’objet qui délègue.</span><span class="sxs-lookup"><span data-stu-id="01408-108">Pointer to the **IUnknown** interface of the delegating object.</span></span>

</dd> <dt>

<span data-ttu-id="01408-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="01408-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="01408-110">Pointeur vers la valeur de retour COM générale.</span><span class="sxs-lookup"><span data-stu-id="01408-110">Pointer to the general COM return value.</span></span> <span data-ttu-id="01408-111">Cette valeur est modifiée uniquement si cette fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="01408-111">This value is changed only if this function fails.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01408-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01408-112">Requirements</span></span>



| <span data-ttu-id="01408-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01408-113">Requirement</span></span> | <span data-ttu-id="01408-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="01408-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01408-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="01408-115">Header</span></span><br/>  | <dl> <span data-ttu-id="01408-116"><dt>PStream. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01408-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="01408-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="01408-117">Library</span></span><br/> | <dl> <span data-ttu-id="01408-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="01408-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01408-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01408-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01408-120">**CPersistStream, classe**</span><span class="sxs-lookup"><span data-stu-id="01408-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




