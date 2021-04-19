---
description: Construit un objet CMsg.
ms.assetid: b7ee0643-73e4-450d-bff4-ca5006fdcc14
title: Constructeur CMsg. CMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg.CMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b26a9572b51d4a476b70c3dd7ddae8c896a4d648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545506"
---
# <a name="cmsgcmsg-constructor"></a><span data-ttu-id="ffa2f-103">Constructeur CMsg. CMsg</span><span class="sxs-lookup"><span data-stu-id="ffa2f-103">CMsg.CMsg constructor</span></span>

<span data-ttu-id="ffa2f-104">Construit un objet [**CMsg**](cmsg.md) .</span><span class="sxs-lookup"><span data-stu-id="ffa2f-104">Constructs a [**CMsg**](cmsg.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffa2f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffa2f-105">Syntax</span></span>


```C++
CMsg(
   UINT     u,
   DWORD    dw,
   LPVOID   lp,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a><span data-ttu-id="ffa2f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ffa2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffa2f-107">*u*</span><span class="sxs-lookup"><span data-stu-id="ffa2f-107">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="ffa2f-108">Code de requête, défini par le client de la classe de thread et compris par la fonction de thread de travail remplacée.</span><span class="sxs-lookup"><span data-stu-id="ffa2f-108">Request code, defined by the client of the thread class and understood by the overridden worker thread function.</span></span>

</dd> <dt>

<span data-ttu-id="ffa2f-109">*dw*</span><span class="sxs-lookup"><span data-stu-id="ffa2f-109">*dw*</span></span> 
</dt> <dd>

<span data-ttu-id="ffa2f-110">Paramètre d’indicateur pour le code de la requête.</span><span class="sxs-lookup"><span data-stu-id="ffa2f-110">Flag parameter to the request code.</span></span>

</dd> <dt>

<span data-ttu-id="ffa2f-111">*Aid*</span><span class="sxs-lookup"><span data-stu-id="ffa2f-111">*lp*</span></span> 
</dt> <dd>

<span data-ttu-id="ffa2f-112">Pointeur vers les données requises par le thread de travail comme valeurs de paramètre ou de retour.</span><span class="sxs-lookup"><span data-stu-id="ffa2f-112">Pointer to data required by the worker thread as parameter or return values.</span></span> <span data-ttu-id="ffa2f-113">Ces données ne doivent pas être basées sur la pile, car elles seront référencées un peu plus tard après la fin de l’opération de mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="ffa2f-113">This data should not be stack-based, as it will be referenced some time after completing the queuing operation.</span></span>

</dd> <dt>

<span data-ttu-id="ffa2f-114">*pEvent*</span><span class="sxs-lookup"><span data-stu-id="ffa2f-114">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="ffa2f-115">Pointeur vers l’objet d’événement qu’un thread de travail peut signaler pour indiquer l’achèvement de l’opération.</span><span class="sxs-lookup"><span data-stu-id="ffa2f-115">Pointer to the event object that a worker thread can signal to indicate the completion of the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ffa2f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ffa2f-116">Remarks</span></span>

<span data-ttu-id="ffa2f-117">Cette fonction membre contient une demande pour un thread de travail [**CMsgThread**](cmsgthread.md) sur lequel agir.</span><span class="sxs-lookup"><span data-stu-id="ffa2f-117">This member function contains a request for a [**CMsgThread**](cmsgthread.md) worker thread to act on.</span></span> <span data-ttu-id="ffa2f-118">Tous les paramètres sont passés à la fonction de thread de travail en tant que paramètres lorsque ce message est traité.</span><span class="sxs-lookup"><span data-stu-id="ffa2f-118">All the parameters are passed to the worker thread function as parameters when this message gets processed.</span></span> <span data-ttu-id="ffa2f-119">La signification des paramètres est définie par la fonction cliente qui appelle le thread de travail et la classe dérivée qui fournit la fonction d’exécution du thread de travail.</span><span class="sxs-lookup"><span data-stu-id="ffa2f-119">The meanings of the parameters are defined by the client function that calls the worker thread and the derived class that supplies the worker thread's execution function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffa2f-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffa2f-120">Requirements</span></span>



| <span data-ttu-id="ffa2f-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffa2f-121">Requirement</span></span> | <span data-ttu-id="ffa2f-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffa2f-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffa2f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ffa2f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ffa2f-124"><dt>Msgthrd. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ffa2f-124"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ffa2f-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ffa2f-125">Library</span></span><br/> | <dl> <span data-ttu-id="ffa2f-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ffa2f-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




