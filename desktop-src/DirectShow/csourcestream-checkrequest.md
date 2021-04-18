---
description: La méthode CheckRequest vérifie s’il existe une demande de thread, sans blocage.
ms.assetid: b4691dde-abec-4671-bea6-0f22cc4e7c61
title: Méthode CSourceStream. CheckRequest (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3100d449d2f29b2080541c5968cad6abc5643b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533340"
---
# <a name="csourcestreamcheckrequest-method"></a><span data-ttu-id="ab6f1-103">Méthode CSourceStream. CheckRequest</span><span class="sxs-lookup"><span data-stu-id="ab6f1-103">CSourceStream.CheckRequest method</span></span>

<span data-ttu-id="ab6f1-104">La `CheckRequest` méthode vérifie s’il existe une demande de thread, sans blocage.</span><span class="sxs-lookup"><span data-stu-id="ab6f1-104">The `CheckRequest` method checks if there is a thread request, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab6f1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab6f1-105">Syntax</span></span>


```C++
BOOL CheckRequest(
   Command *pCom
);
```



## <a name="parameters"></a><span data-ttu-id="ab6f1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab6f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab6f1-107">*pCom*</span><span class="sxs-lookup"><span data-stu-id="ab6f1-107">*pCom*</span></span> 
</dt> <dd>

<span data-ttu-id="ab6f1-108">Pointeur vers une variable qui reçoit la valeur passée dans le dernier appel à la méthode [**CAMThread :: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="ab6f1-108">Pointer to a variable that receives the value passed in the last call to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab6f1-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ab6f1-109">Return value</span></span>

<span data-ttu-id="ab6f1-110">Retourne la **valeur true** s’il y a une demande en attente, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ab6f1-110">Returns **TRUE** if there is a pending request, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab6f1-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ab6f1-111">Remarks</span></span>

<span data-ttu-id="ab6f1-112">Cette méthode remplace la méthode [**CAMThread :: CheckRequest**](camthread-checkrequest.md) pour effectuer la vérification de type.</span><span class="sxs-lookup"><span data-stu-id="ab6f1-112">This method overrides the [**CAMThread::CheckRequest**](camthread-checkrequest.md) method to perform type-checking.</span></span> <span data-ttu-id="ab6f1-113">La classe **CSourceStream** définit le type énuméré suivant pour le paramètre *pCom* :</span><span class="sxs-lookup"><span data-stu-id="ab6f1-113">The **CSourceStream** class defines the following enumerated type for the *pCom* parameter:</span></span>


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a><span data-ttu-id="ab6f1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab6f1-114">Requirements</span></span>



| <span data-ttu-id="ab6f1-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab6f1-115">Requirement</span></span> | <span data-ttu-id="ab6f1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab6f1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab6f1-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab6f1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ab6f1-118"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab6f1-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ab6f1-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ab6f1-119">Library</span></span><br/> | <dl> <span data-ttu-id="ab6f1-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ab6f1-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab6f1-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab6f1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab6f1-122">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="ab6f1-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




