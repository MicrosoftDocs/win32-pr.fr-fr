---
description: Bloque jusqu’à ce que le thread se termine.
ms.assetid: 1ee547b5-cd73-4ce8-8e66-c2062714d0f0
title: Méthode CMsgThread. WaitForThreadExit (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.WaitForThreadExit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b48573c4297a2d5d5d008eba88fd8ea437333c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528896"
---
# <a name="cmsgthreadwaitforthreadexit-method"></a><span data-ttu-id="f7f74-103">Méthode CMsgThread. WaitForThreadExit</span><span class="sxs-lookup"><span data-stu-id="f7f74-103">CMsgThread.WaitForThreadExit method</span></span>

<span data-ttu-id="f7f74-104">Bloque jusqu’à ce que le thread se termine.</span><span class="sxs-lookup"><span data-stu-id="f7f74-104">Blocks until the thread exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7f74-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7f74-105">Syntax</span></span>


```C++
BOOL WaitForThreadExit(
   LPDWORD lpdwExitCode
);
```



## <a name="parameters"></a><span data-ttu-id="f7f74-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7f74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7f74-107">*lpdwExitCode*</span><span class="sxs-lookup"><span data-stu-id="f7f74-107">*lpdwExitCode*</span></span> 
</dt> <dd>

<span data-ttu-id="f7f74-108">Pointeur désignant le code de sortie retourné par le thread.</span><span class="sxs-lookup"><span data-stu-id="f7f74-108">Pointer to the exit code returned by the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7f74-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7f74-109">Return value</span></span>

<span data-ttu-id="f7f74-110">Retourne la **valeur true** ou **false**, dont la signification est déterminée par la classe qui fournit la fonction membre [**CMsgThread :: ThreadMessageProc**](cmsgthread-threadmessageproc.md) substituée et la fonction membre d’appel.</span><span class="sxs-lookup"><span data-stu-id="f7f74-110">Returns either **TRUE** or **FALSE**, the meaning of which is determined by the class supplying the overridden [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function and the calling member function.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7f74-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f7f74-111">Remarks</span></span>

<span data-ttu-id="f7f74-112">Assurez-vous que le thread de travail s’est terminé complètement avant de terminer la destruction de votre classe dérivée. dans le cas contraire, le thread peut encore s’exécuter après que votre bibliothèque de liens dynamiques (DLL) a été déchargée de l’espace d’adressage du processus.</span><span class="sxs-lookup"><span data-stu-id="f7f74-112">Ensure that the worker thread has exited completely before completing the destruction of your derived class; otherwise, the thread might still execute after your dynamic-link library (DLL) has been unloaded from the address space of the process.</span></span> <span data-ttu-id="f7f74-113">Même si la seule instruction restante à Exit est une instruction à retour unique, cela provoquerait une exception.</span><span class="sxs-lookup"><span data-stu-id="f7f74-113">Even if the only instruction left to exit is a single-return instruction, this would cause an exception.</span></span> <span data-ttu-id="f7f74-114">La seule méthode fiable pour s’assurer que le thread s’est arrêté est de signaler au thread de quitter (à l’aide d’un objet [**CMsg**](cmsg.md) négocié en privé envoyé à la fonction membre [**CMsgThread ::P utthreadmsg**](cmsgthread-putthreadmsg.md) ), puis d’appeler cette fonction membre.</span><span class="sxs-lookup"><span data-stu-id="f7f74-114">The only reliable way to ensure that the thread has exited is to signal the thread to exit (using a privately negotiated [**CMsg**](cmsg.md) object sent to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function) and then call this member function.</span></span> <span data-ttu-id="f7f74-115">Vous devez le faire dans le destructeur de votre classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="f7f74-115">You should do this in the destructor for your derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7f74-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7f74-116">Requirements</span></span>



| <span data-ttu-id="f7f74-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7f74-117">Requirement</span></span> | <span data-ttu-id="f7f74-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7f74-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7f74-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7f74-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f7f74-120"><dt>Msgthrd. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7f74-120"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f7f74-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f7f74-121">Library</span></span><br/> | <dl> <span data-ttu-id="f7f74-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f7f74-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7f74-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7f74-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7f74-124">**CMsgThread, classe**</span><span class="sxs-lookup"><span data-stu-id="f7f74-124">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




