---
description: 'La méthode STOPAT indique au code PIN quand arrêter la transmission de données. Cette méthode implémente la méthode IAMStreamControl :: STOPAT.'
ms.assetid: cc9f0fdc-253b-4feb-95ce-56ebc575a49b
title: CBaseStreamControl. STOPAT, méthode (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StopAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e6b794f5f05721f403d943252c2aabd48614519
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537309"
---
# <a name="cbasestreamcontrolstopat-method"></a><span data-ttu-id="9107a-104">CBaseStreamControl. STOPAT, méthode</span><span class="sxs-lookup"><span data-stu-id="9107a-104">CBaseStreamControl.StopAt method</span></span>

<span data-ttu-id="9107a-105">La `StopAt` méthode informe le code confidentiel quand il faut arrêter la transmission des données.</span><span class="sxs-lookup"><span data-stu-id="9107a-105">The `StopAt` method informs the pin when to stop delivering data.</span></span> <span data-ttu-id="9107a-106">Cette méthode implémente la méthode [**IAMStreamControl :: STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .</span><span class="sxs-lookup"><span data-stu-id="9107a-106">This method implements the [**IAMStreamControl::StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9107a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9107a-107">Syntax</span></span>


```C++
HRESULT StopAt(
   const REFERENCE_TIME *ptStop = NULL,
         BOOL           bSendExtra = FALSE,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a><span data-ttu-id="9107a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9107a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9107a-109">*ptStop*</span><span class="sxs-lookup"><span data-stu-id="9107a-109">*ptStop*</span></span> 
</dt> <dd>

<span data-ttu-id="9107a-110">Pointeur vers une valeur de [**\_ temps de référence**](reference-time.md) qui spécifie quand le code confidentiel doit cesser de transmettre des données.</span><span class="sxs-lookup"><span data-stu-id="9107a-110">Pointer to a [**REFERENCE\_TIME**](reference-time.md) value that specifies when the pin should stop delivering data.</span></span>

</dd> <dt>

<span data-ttu-id="9107a-111">*bSendExtra*</span><span class="sxs-lookup"><span data-stu-id="9107a-111">*bSendExtra*</span></span> 
</dt> <dd>

<span data-ttu-id="9107a-112">Spécifie une valeur booléenne qui indique s’il faut envoyer un échantillon supplémentaire après l’heure d’arrêt planifiée.</span><span class="sxs-lookup"><span data-stu-id="9107a-112">Specifies a Boolean value that indicates whether to send an extra sample after the scheduled stop time.</span></span> <span data-ttu-id="9107a-113">Si la **valeur est true**, le code PIN envoie un échantillon supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="9107a-113">If **TRUE**, the pin sends one extra sample.</span></span>

</dd> <dt>

<span data-ttu-id="9107a-114">*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="9107a-114">*dwCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="9107a-115">Spécifie une valeur à envoyer avec la notification de démarrage.</span><span class="sxs-lookup"><span data-stu-id="9107a-115">Specifies a value to send along with the start notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9107a-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9107a-116">Return value</span></span>

<span data-ttu-id="9107a-117">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9107a-117">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="9107a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9107a-118">Requirements</span></span>



| <span data-ttu-id="9107a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9107a-119">Requirement</span></span> | <span data-ttu-id="9107a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9107a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9107a-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="9107a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9107a-122"><dt>Strmctl. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9107a-122"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9107a-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9107a-123">Library</span></span><br/> | <dl> <span data-ttu-id="9107a-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9107a-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9107a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9107a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9107a-126">**CBaseStreamControl, classe**</span><span class="sxs-lookup"><span data-stu-id="9107a-126">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




