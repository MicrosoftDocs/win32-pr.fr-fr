---
description: Demandes d’exécution d’une expérience (capture) sur le processus spécifié.
MS-HAID: vspixengine.IRunExperimentCallback\_ResultCallback\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IRunExperimentCallback :: ResultCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C00034DF-5F51-49A2-B49A-62F98EA48F46
api_name:
- IRunExperimentCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ac6838e7103970d588814bdc5a39e9e26fd4a33
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516739"
---
# <a name="span-idvspixengineirunexperimentcallback_resultcallback_dwordspanirunexperimentcallbackresultcallback-method"></a><span data-ttu-id="245f2-103"><span id="vspixengine.irunexperimentcallback_resultcallback_dword"></span>IRunExperimentCallback :: ResultCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="245f2-103"><span id="vspixengine.irunexperimentcallback_resultcallback_dword"></span>IRunExperimentCallback::ResultCallback method</span></span>

<span data-ttu-id="245f2-104">Demandes d’exécution d’une expérience (capture) sur le processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="245f2-104">Requests to run an experiment (capture) on the specified process.</span></span>

## <a name="syntax"></a><span data-ttu-id="245f2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="245f2-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD processId
);
```

## <a name="parameters"></a><span data-ttu-id="245f2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="245f2-106">Parameters</span></span>

<span data-ttu-id="245f2-107">*processId* </span><span class="sxs-lookup"><span data-stu-id="245f2-107">*processId* </span></span>  
<span data-ttu-id="245f2-108">Processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="245f2-108">The specified process.</span></span>

## <a name="return-value"></a><span data-ttu-id="245f2-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="245f2-109">Return value</span></span>

<span data-ttu-id="245f2-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="245f2-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="245f2-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="245f2-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="245f2-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="245f2-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="245f2-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="245f2-113">Header</span></span></p></td><td><span data-ttu-id="245f2-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="245f2-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="245f2-115"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="245f2-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="245f2-116">**IRunExperimentCallback**</span><span class="sxs-lookup"><span data-stu-id="245f2-116">**IRunExperimentCallback**</span></span>](/windows/desktop/direct3dtools/irunexperimentcallback)

 

 
