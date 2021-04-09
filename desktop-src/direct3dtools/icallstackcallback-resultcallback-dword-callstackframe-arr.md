---
description: Fonction de rappel utilisée pour informer l’hôte des informations de la pile des appels.
MS-HAID: vspixengine.ICallStackCallback\_ResultCallback\_DWORD\_CallStackFrame\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ICallStackCallback :: ResultCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9C083298-6FD5-4414-8E0C-625F6A144668
api_name:
- ICallStackCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4bd77ea22fd31b31081d72707b1fd7a2efbda607
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846398"
---
# <a name="span-idvspixengineicallstackcallback_resultcallback_dword_callstackframe_arrspanicallstackcallbackresultcallback-method"></a><span data-ttu-id="a4257-103"><span id="vspixengine.icallstackcallback_resultcallback_dword_callstackframe_arr"></span>ICallStackCallback :: ResultCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="a4257-103"><span id="vspixengine.icallstackcallback_resultcallback_dword_callstackframe_arr"></span>ICallStackCallback::ResultCallback method</span></span>

<span data-ttu-id="a4257-104">Fonction de rappel utilisée pour informer l’hôte des informations de la pile des appels.</span><span class="sxs-lookup"><span data-stu-id="a4257-104">A callback function used to notify the host of call stack information.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4257-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4257-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD             count,
   CallStackFrame [] count0_callStackFrameBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="a4257-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4257-106">Parameters</span></span>

<span data-ttu-id="a4257-107">*saut* </span><span class="sxs-lookup"><span data-stu-id="a4257-107">*count* </span></span>  
<span data-ttu-id="a4257-108">Nombre de framebuffers de pile des appels renvoyés.</span><span class="sxs-lookup"><span data-stu-id="a4257-108">The number of callstack framebuffers returned.</span></span>

<span data-ttu-id="a4257-109">*count0 \_ callStackFrameBuffer* </span><span class="sxs-lookup"><span data-stu-id="a4257-109">*count0\_callStackFrameBuffer* </span></span>  
<span data-ttu-id="a4257-110">Informations de la pile des appels.</span><span class="sxs-lookup"><span data-stu-id="a4257-110">The callstack information.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4257-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a4257-111">Return value</span></span>

<span data-ttu-id="a4257-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a4257-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a4257-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a4257-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4257-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4257-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a4257-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="a4257-115">Header</span></span></p></td><td><span data-ttu-id="a4257-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a4257-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a4257-117"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4257-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a4257-118">**ICallStackCallback**</span><span class="sxs-lookup"><span data-stu-id="a4257-118">**ICallStackCallback**</span></span>](/windows/desktop/direct3dtools/icallstackcallback)

 

 
