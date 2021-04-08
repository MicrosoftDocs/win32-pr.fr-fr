---
title: Méthode IWMPEvents4 SyncEstimationComplete
description: L’événement SyncEstimationComplete se produit lorsqu’une estimation de la taille, précédemment lancée par IWMPSyncDevice3 estimateSyncSize, est terminée.
ms.assetid: 2fb45a13-d82b-48b6-b9bb-46409f33a33f
keywords:
- Méthode SyncEstimationComplete lecteur Windows Media
- Méthode SyncEstimationComplete lecteur Windows Media, interface IWMPEvents4
- Interface IWMPEvents4 lecteur Windows Media, méthode SyncEstimationComplete
topic_type:
- apiref
api_name:
- IWMPEvents4.SyncEstimationComplete
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 209ed2f2bd0f075dbaa8d442a276c994d50ce2e5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723386"
---
# <a name="iwmpevents4syncestimationcomplete-method"></a><span data-ttu-id="43f26-106">IWMPEvents4 :: SyncEstimationComplete, méthode</span><span class="sxs-lookup"><span data-stu-id="43f26-106">IWMPEvents4::SyncEstimationComplete method</span></span>

<span data-ttu-id="43f26-107">L’événement **SyncEstimationComplete** se produit lorsqu’une estimation de la taille, précédemment lancée par [**IWMPSyncDevice3 :: estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize), est terminée.</span><span class="sxs-lookup"><span data-stu-id="43f26-107">The **SyncEstimationComplete** event occurs when a size estimation, previously initiated by [**IWMPSyncDevice3::estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize), is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="43f26-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43f26-108">Syntax</span></span>


```C++
void SyncEstimationComplete(
  [in] IWMPSyncDevice *pDevice,
  [in] long           hrResult,
  [in] long           lEstimatedUsedSpace,
  [in] long           lEstimatedSize
);
```



## <a name="parameters"></a><span data-ttu-id="43f26-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43f26-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43f26-110">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="43f26-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f26-111">Pointeur vers l’interface [**IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) qui représente l’appareil pour lequel l’estimation de la taille a été initiée.</span><span class="sxs-lookup"><span data-stu-id="43f26-111">Pointer to the [**IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) interface that represents the device for which the size estimation was initiated.</span></span>

</dd> <dt>

<span data-ttu-id="43f26-112">*hrResult* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="43f26-112">*hrResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f26-113">Valeur qui indique la réussite ou l’échec de l’estimation.</span><span class="sxs-lookup"><span data-stu-id="43f26-113">A value that indicates the success or failure of the estimation.</span></span>



| <span data-ttu-id="43f26-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="43f26-114">Value</span></span>                                                                                                                                       | <span data-ttu-id="43f26-115">Signification</span><span class="sxs-lookup"><span data-stu-id="43f26-115">Meaning</span></span>                                |
|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="43f26-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="43f26-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="43f26-117">Estimation réussie.</span><span class="sxs-lookup"><span data-stu-id="43f26-117">The estimation succeeded.</span></span><br/>   |
| <span id="E_ABORT"></span><span id="e_abort"></span><dl> <span data-ttu-id="43f26-118"><dt>**E \_ Abort**</dt></span><span class="sxs-lookup"><span data-stu-id="43f26-118"><dt>**E\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="43f26-119">L’estimation a été abandonnée.</span><span class="sxs-lookup"><span data-stu-id="43f26-119">The estimation was aborted.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="43f26-120">*lEstimatedUsedSpace* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="43f26-120">*lEstimatedUsedSpace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f26-121">Espace estimé (en octets) qui doit être utilisé sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="43f26-121">The estimated space (in bytes) that would be used on the device.</span></span>

</dd> <dt>

<span data-ttu-id="43f26-122">*lEstimatedSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="43f26-122">*lEstimatedSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f26-123">Taille estimée (en octets) des données à synchroniser.</span><span class="sxs-lookup"><span data-stu-id="43f26-123">The estimated size (in bytes) of the data to be synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43f26-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43f26-124">Return value</span></span>

<span data-ttu-id="43f26-125">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="43f26-125">This method does not return a value.</span></span>

## <a name="see-also"></a><span data-ttu-id="43f26-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43f26-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43f26-127">**Interface IWMPEvents4**</span><span class="sxs-lookup"><span data-stu-id="43f26-127">**IWMPEvents4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
</dt> <dt>

[<span data-ttu-id="43f26-128">**IWMPSyncDevice3::estimateSyncSize**</span><span class="sxs-lookup"><span data-stu-id="43f26-128">**IWMPSyncDevice3::estimateSyncSize**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)
</dt> </dl>

 

 





