---
description: Fonction de rappel utilisée pour informer l’hôte des frames dont les rapports d’analyse hors connexion sont disponibles.
MS-HAID: vspixengine.IOfflineAnalysisCacheCallback\_OfflineAnalaysisReportAvailabilityCallback\_DWORD\_DWORD\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IOfflineAnalysisCacheCallback :: OfflineAnalaysisReportAvailabilityCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2061EB62-4CBD-4668-BFCD-6E43014BB406
api_name:
- IOfflineAnalysisCacheCallback.OfflineAnalaysisReportAvailabilityCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: adbffbeb79aaf648c3319cf572dcbc905e9fd307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514732"
---
# <a name="span-idvspixengineiofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arrspaniofflineanalysiscachecallbackofflineanalaysisreportavailabilitycallback-method"></a><span data-ttu-id="02b3d-103"><span id="vspixengine.iofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arr"></span>IOfflineAnalysisCacheCallback :: OfflineAnalaysisReportAvailabilityCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="02b3d-103"><span id="vspixengine.iofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arr"></span>IOfflineAnalysisCacheCallback::OfflineAnalaysisReportAvailabilityCallback method</span></span>

<span data-ttu-id="02b3d-104">Fonction de rappel utilisée pour informer l’hôte des frames dont les rapports d’analyse hors connexion sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="02b3d-104">A callback function used to notify the host about which frames have offline analysis reports available.</span></span>

## <a name="syntax"></a><span data-ttu-id="02b3d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02b3d-105">Syntax</span></span>


```C++
HRESULT OfflineAnalaysisReportAvailabilityCallback(
   DWORD    numFramesWithReports,
   DWORD [] count0_framesWithReports
);
```

## <a name="parameters"></a><span data-ttu-id="02b3d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02b3d-106">Parameters</span></span>

<span data-ttu-id="02b3d-107">*numFramesWithReports* </span><span class="sxs-lookup"><span data-stu-id="02b3d-107">*numFramesWithReports* </span></span>  
<span data-ttu-id="02b3d-108">Nombre de frames dans count0 \_ framesWithReports.</span><span class="sxs-lookup"><span data-stu-id="02b3d-108">The number of frames in count0\_framesWithReports.</span></span>

<span data-ttu-id="02b3d-109">*count0 \_ framesWithReports* </span><span class="sxs-lookup"><span data-stu-id="02b3d-109">*count0\_framesWithReports* </span></span>  
<span data-ttu-id="02b3d-110">Tableau contenant les numéros de frame des frames dont les rapports d’analyse hors connexion sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="02b3d-110">An array containing the frame numbers of the frames that have offline analysis reports available.</span></span>

## <a name="return-value"></a><span data-ttu-id="02b3d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02b3d-111">Return value</span></span>

<span data-ttu-id="02b3d-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="02b3d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="02b3d-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="02b3d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="02b3d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02b3d-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="02b3d-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="02b3d-115">Header</span></span></p></td><td><span data-ttu-id="02b3d-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="02b3d-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="02b3d-117"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02b3d-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="02b3d-118">**IOfflineAnalysisCacheCallback**</span><span class="sxs-lookup"><span data-stu-id="02b3d-118">**IOfflineAnalysisCacheCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscachecallback)

 

 
