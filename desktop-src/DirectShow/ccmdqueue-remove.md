---
description: La méthode Remove supprime l’objet CDeferredCommand de la file d’attente.
ms.assetid: b3cff57d-9625-40db-b815-9529ac706f45
title: CCmdQueue. Remove, méthode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef9f45c8176645c5937b5ad74045130ff8cd8c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545657"
---
# <a name="ccmdqueueremove-method"></a><span data-ttu-id="8a2bb-103">CCmdQueue. Remove, méthode</span><span class="sxs-lookup"><span data-stu-id="8a2bb-103">CCmdQueue.Remove method</span></span>

<span data-ttu-id="8a2bb-104">La `Remove` méthode supprime l’objet [**CDeferredCommand**](cdeferredcommand.md) de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="8a2bb-104">The `Remove` method removes the [**CDeferredCommand**](cdeferredcommand.md) object from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a2bb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a2bb-105">Syntax</span></span>


```C++
virtual HRESULT Remove(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a><span data-ttu-id="8a2bb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a2bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a2bb-107">*pCmd*</span><span class="sxs-lookup"><span data-stu-id="8a2bb-107">*pCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="8a2bb-108">Pointeur vers l’objet **CDeferredCommand** à supprimer de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="8a2bb-108">Pointer to the **CDeferredCommand** object to remove from the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a2bb-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8a2bb-109">Return value</span></span>

<span data-ttu-id="8a2bb-110">Retourne VFW \_ E \_ \_ introuvable si l’objet est introuvable dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="8a2bb-110">Returns VFW\_E\_NOT\_FOUND if the object is not found in the queue.</span></span> <span data-ttu-id="8a2bb-111">Sinon, retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8a2bb-111">Otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a2bb-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a2bb-112">Requirements</span></span>



| <span data-ttu-id="8a2bb-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a2bb-113">Requirement</span></span> | <span data-ttu-id="8a2bb-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a2bb-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a2bb-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="8a2bb-115">Header</span></span><br/>  | <dl> <span data-ttu-id="8a2bb-116"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a2bb-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8a2bb-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8a2bb-117">Library</span></span><br/> | <dl> <span data-ttu-id="8a2bb-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8a2bb-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a2bb-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a2bb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a2bb-120">**CCmdQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="8a2bb-120">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




