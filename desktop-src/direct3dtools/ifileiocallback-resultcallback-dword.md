---
description: Fonction de rappel utilisée pour informer l’hôte des erreurs lors de la capture ou de la lecture.
MS-HAID: vspixengine.IFileIOCallback\_ResultCallback\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFileIOCallback :: ResultCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E4418A63-47C6-4F12-94FA-0F1B5465FE84
api_name:
- IFileIOCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 751c4d0b57165e148002218ae2151aaba69e48f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109247"
---
# <a name="span-idvspixengineifileiocallback_resultcallback_dwordspanifileiocallbackresultcallback-method"></a><span data-ttu-id="6e20d-103"><span id="vspixengine.ifileiocallback_resultcallback_dword"></span>IFileIOCallback :: ResultCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="6e20d-103"><span id="vspixengine.ifileiocallback_resultcallback_dword"></span>IFileIOCallback::ResultCallback method</span></span>

<span data-ttu-id="6e20d-104">Fonction de rappel utilisée pour informer l’hôte des erreurs lors de la capture ou de la lecture.</span><span class="sxs-lookup"><span data-stu-id="6e20d-104">A callback function used to notify the host of errors while during capture or playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e20d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e20d-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD resultState
);
```

## <a name="parameters"></a><span data-ttu-id="6e20d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e20d-106">Parameters</span></span>

<span data-ttu-id="6e20d-107">*resultState* </span><span class="sxs-lookup"><span data-stu-id="6e20d-107">*resultState* </span></span>  
<span data-ttu-id="6e20d-108">Indique le type d’erreur rencontrée.</span><span class="sxs-lookup"><span data-stu-id="6e20d-108">Indicates the kind of error encountered.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e20d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6e20d-109">Return value</span></span>

<span data-ttu-id="6e20d-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6e20d-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6e20d-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6e20d-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e20d-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e20d-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6e20d-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e20d-113">Header</span></span></p></td><td><span data-ttu-id="6e20d-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6e20d-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="6e20d-115"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e20d-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="6e20d-116">**IFileIOCallback**</span><span class="sxs-lookup"><span data-stu-id="6e20d-116">**IFileIOCallback**</span></span>](/windows/desktop/direct3dtools/ifileiocallback)

 

 
