---
description: 'La méthode GetInfo récupère des informations sur les paramètres de contrôle de flux actuels, y compris les heures de démarrage et d’arrêt. Cette méthode implémente la méthode IAMStreamControl :: GetInfo.'
ms.assetid: 3bc9bb32-eb33-4752-b22c-9033c28b41f7
title: CBaseStreamControl. GetInfo, méthode (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.GetInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab0ba31fa5692a6bc92372860ec1a28ab776206f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544479"
---
# <a name="cbasestreamcontrolgetinfo-method"></a><span data-ttu-id="8be1e-104">CBaseStreamControl. GetInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="8be1e-104">CBaseStreamControl.GetInfo method</span></span>

<span data-ttu-id="8be1e-105">La `GetInfo` méthode récupère des informations sur les paramètres de contrôle de flux actuels, y compris les heures de démarrage et d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="8be1e-105">The `GetInfo` method retrieves information about the current stream-control settings, including the start and stop times.</span></span> <span data-ttu-id="8be1e-106">Cette méthode implémente la méthode [**IAMStreamControl :: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) .</span><span class="sxs-lookup"><span data-stu-id="8be1e-106">This method implements the [**IAMStreamControl::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8be1e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8be1e-107">Syntax</span></span>


```C++
HRESULT GetInfo(
   AM_STREAM_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="8be1e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8be1e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8be1e-109">*pInfo*</span><span class="sxs-lookup"><span data-stu-id="8be1e-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="8be1e-110">Pointeur vers une structure d' [**\_ \_ informations de flux am**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) , allouée par l’appelant, qui reçoit les paramètres de contrôle de flux actuels.</span><span class="sxs-lookup"><span data-stu-id="8be1e-110">Pointer to an [**AM\_STREAM\_INFO**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) structure, allocated by the caller, that receives the current stream-control settings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8be1e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8be1e-111">Return value</span></span>

<span data-ttu-id="8be1e-112">Retourne le \_ pointeur S ou OK \_ .</span><span class="sxs-lookup"><span data-stu-id="8be1e-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="8be1e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8be1e-113">Requirements</span></span>



| <span data-ttu-id="8be1e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8be1e-114">Requirement</span></span> | <span data-ttu-id="8be1e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="8be1e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8be1e-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="8be1e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8be1e-117"><dt>Strmctl. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8be1e-117"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8be1e-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8be1e-118">Library</span></span><br/> | <dl> <span data-ttu-id="8be1e-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8be1e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8be1e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8be1e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8be1e-121">**CBaseStreamControl, classe**</span><span class="sxs-lookup"><span data-stu-id="8be1e-121">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




