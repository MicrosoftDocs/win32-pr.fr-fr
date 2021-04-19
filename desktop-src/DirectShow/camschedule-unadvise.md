---
description: La méthode Unadvise supprime une demande de notification.
ms.assetid: b3dfda82-577e-4499-a114-1c8721e4af9e
title: CAMSchedule. Unadvise, méthode (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25dd70a46fcc2b6572500b3164b64fd0facbcbe0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532681"
---
# <a name="camscheduleunadvise-method"></a><span data-ttu-id="232e0-103">CAMSchedule. Unadvise, méthode</span><span class="sxs-lookup"><span data-stu-id="232e0-103">CAMSchedule.Unadvise method</span></span>

<span data-ttu-id="232e0-104">La `Unadvise` méthode supprime une demande de notification.</span><span class="sxs-lookup"><span data-stu-id="232e0-104">The `Unadvise` method removes an advise request.</span></span>

## <a name="syntax"></a><span data-ttu-id="232e0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="232e0-105">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="232e0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="232e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="232e0-107">*dwAdviseCookie*</span><span class="sxs-lookup"><span data-stu-id="232e0-107">*dwAdviseCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="232e0-108">Identificateur de la demande de notification, retourné par la méthode [**CAMSchedule :: AddAdvisePacket**](camschedule-addadvisepacket.md) .</span><span class="sxs-lookup"><span data-stu-id="232e0-108">Identifier of the advise request, returned by the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="232e0-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="232e0-109">Return value</span></span>

<span data-ttu-id="232e0-110">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="232e0-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="232e0-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="232e0-111">Return code</span></span>                                                                             | <span data-ttu-id="232e0-112">Description</span><span class="sxs-lookup"><span data-stu-id="232e0-112">Description</span></span>          |
|-----------------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="232e0-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="232e0-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="232e0-114">Introuvable</span><span class="sxs-lookup"><span data-stu-id="232e0-114">Not found</span></span><br/> |
| <dl> <span data-ttu-id="232e0-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="232e0-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="232e0-116">Succès</span><span class="sxs-lookup"><span data-stu-id="232e0-116">Success</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="232e0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="232e0-117">Requirements</span></span>



| <span data-ttu-id="232e0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="232e0-118">Requirement</span></span> | <span data-ttu-id="232e0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="232e0-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="232e0-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="232e0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="232e0-121"><dt>Dsschedule. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="232e0-121"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="232e0-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="232e0-122">Library</span></span><br/> | <dl> <span data-ttu-id="232e0-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="232e0-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="232e0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="232e0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="232e0-125">**CAMSchedule, classe**</span><span class="sxs-lookup"><span data-stu-id="232e0-125">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




