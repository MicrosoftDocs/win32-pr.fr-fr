---
description: La méthode PeriodicUpdatePicture est appelée par une application pour configurer un minuteur dans le flux qui demandera régulièrement des mises à jour d’images. Les mises à jour d’image entraînent une utilisation élevée de la bande passante. cette méthode est donc normalement utilisée à la place de UpdatePicture.
ms.assetid: 6ae3b5e9-bc11-4f3f-972b-21c9ac299987
title: IKeyFrameControl ::P méthode eriodicUpdatePicture (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bbfb18b0be96d611f0fe385cc825602dc316ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539192"
---
# <a name="ikeyframecontrolperiodicupdatepicture-method"></a><span data-ttu-id="4362c-104">IKeyFrameControl ::P méthode eriodicUpdatePicture</span><span class="sxs-lookup"><span data-stu-id="4362c-104">IKeyFrameControl::PeriodicUpdatePicture method</span></span>

<span data-ttu-id="4362c-105">\[**PeriodicUpdatePicture** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4362c-105">\[**PeriodicUpdatePicture** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4362c-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="4362c-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4362c-107">La méthode **PeriodicUpdatePicture** est appelée par une application pour configurer un minuteur dans le flux qui demandera régulièrement des mises à jour d’images.</span><span class="sxs-lookup"><span data-stu-id="4362c-107">The **PeriodicUpdatePicture** method is called by an application to configure a timer in the stream that will ask for picture updates periodically.</span></span> <span data-ttu-id="4362c-108">Les mises à jour d’image entraînent une utilisation élevée de la bande passante. cette méthode est donc normalement utilisée à la place de [**UpdatePicture**](ikeyframecontrol-updatepicture.md).</span><span class="sxs-lookup"><span data-stu-id="4362c-108">Picture updates cause high bandwidth usage, so this method will normally be used instead of [**UpdatePicture**](ikeyframecontrol-updatepicture.md).</span></span>

<span data-ttu-id="4362c-109">Si la méthode est appelée lorsque le flux est actif, le minuteur démarre immédiatement.</span><span class="sxs-lookup"><span data-stu-id="4362c-109">If the method is called when the stream is active, the timer will start immediately.</span></span> <span data-ttu-id="4362c-110">Si le flux n’est pas actif, le minuteur est démarré lorsque le flux passe à l’état actif.</span><span class="sxs-lookup"><span data-stu-id="4362c-110">If the stream is not active, the timer will be started when the stream enters the active state.</span></span>

## <a name="syntax"></a><span data-ttu-id="4362c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4362c-111">Syntax</span></span>


```C++
HRESULT PeriodicUpdatePicture(
  [in] BOOL  fEnable,
  [in] DWORD dwInterval
);
```



## <a name="parameters"></a><span data-ttu-id="4362c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4362c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4362c-113">*fEnable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4362c-113">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4362c-114">**True** active la minuterie.</span><span class="sxs-lookup"><span data-stu-id="4362c-114">**TRUE** enables the timer.</span></span> <span data-ttu-id="4362c-115">**False** le désactive.</span><span class="sxs-lookup"><span data-stu-id="4362c-115">**FALSE** disables it.</span></span>

</dd> <dt>

<span data-ttu-id="4362c-116">*dwInterval* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4362c-116">*dwInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4362c-117">Intervalle, en secondes, de la minuterie.</span><span class="sxs-lookup"><span data-stu-id="4362c-117">The interval for the timer, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4362c-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4362c-118">Return value</span></span>

<span data-ttu-id="4362c-119">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="4362c-119">This method can return one of these values.</span></span>



| <span data-ttu-id="4362c-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4362c-120">Return code</span></span>                                                                            | <span data-ttu-id="4362c-121">Description</span><span class="sxs-lookup"><span data-stu-id="4362c-121">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="4362c-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4362c-122"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="4362c-123">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="4362c-123">Method succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="4362c-124"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="4362c-124"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="4362c-125">A échoué pour des raisons inattendues.</span><span class="sxs-lookup"><span data-stu-id="4362c-125">Failed for unexpected reasons.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4362c-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4362c-126">Requirements</span></span>



| <span data-ttu-id="4362c-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4362c-127">Requirement</span></span> | <span data-ttu-id="4362c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="4362c-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4362c-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="4362c-129">TAPI version</span></span><br/> | <span data-ttu-id="4362c-130">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="4362c-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4362c-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="4362c-131">Header</span></span><br/>       | <dl> <span data-ttu-id="4362c-132"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="4362c-132"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="4362c-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4362c-133">Library</span></span><br/>      | <dl> <span data-ttu-id="4362c-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4362c-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4362c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4362c-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="4362c-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4362c-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4362c-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4362c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4362c-138">MSP H323</span><span class="sxs-lookup"><span data-stu-id="4362c-138">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

 




