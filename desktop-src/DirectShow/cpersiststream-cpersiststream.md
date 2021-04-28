---
description: Méthode constructeur CPersistStream. CPersistStream.
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
ms.openlocfilehash: 9e3be9233d76929ebfcb79121c60ef6c1af35b56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085607"
---
# <a name="cpersiststreamcpersiststream-constructor"></a><span data-ttu-id="4f673-103">Constructeur CPersistStream. CPersistStream</span><span class="sxs-lookup"><span data-stu-id="4f673-103">CPersistStream.CPersistStream constructor</span></span>

<span data-ttu-id="4f673-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="4f673-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f673-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f673-105">Syntax</span></span>


```C++
CPersistStream(
   IUnknown *pUnk,
   HRESULT  *phr
);
```



## <a name="parameters"></a><span data-ttu-id="4f673-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f673-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f673-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="4f673-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="4f673-108">Pointeur vers l’interface **IUnknown** de l’objet qui délègue.</span><span class="sxs-lookup"><span data-stu-id="4f673-108">Pointer to the **IUnknown** interface of the delegating object.</span></span>

</dd> <dt>

<span data-ttu-id="4f673-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="4f673-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="4f673-110">Pointeur vers la valeur de retour COM générale.</span><span class="sxs-lookup"><span data-stu-id="4f673-110">Pointer to the general COM return value.</span></span> <span data-ttu-id="4f673-111">Cette valeur est modifiée uniquement si cette fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="4f673-111">This value is changed only if this function fails.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f673-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f673-112">Requirements</span></span>



| <span data-ttu-id="4f673-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f673-113">Requirement</span></span> | <span data-ttu-id="4f673-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f673-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f673-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f673-115">Header</span></span><br/>  | <dl> <span data-ttu-id="4f673-116"><dt>PStream. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f673-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4f673-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4f673-117">Library</span></span><br/> | <dl> <span data-ttu-id="4f673-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4f673-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f673-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f673-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f673-120">**CPersistStream, classe**</span><span class="sxs-lookup"><span data-stu-id="4f673-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




