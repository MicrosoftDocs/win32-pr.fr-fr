---
description: Active les optimisations statiques dans le pipeline vidéo.
ms.assetid: 62fb3f0f-ab1f-4c61-8e7f-62908b947788
title: Attribut MF_TOPOLOGY_STATIC_PLAYBACK_OPTIMIZATIONS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f9f7d884c49078ca02571f8ba141f9a1e13589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521964"
---
# <a name="mf_topology_static_playback_optimizations-attribute"></a><span data-ttu-id="5b90d-103">Attribut d’optimisation de \_ \_ lecture statique de \_ la topologie MF \_</span><span class="sxs-lookup"><span data-stu-id="5b90d-103">MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS attribute</span></span>

<span data-ttu-id="5b90d-104">Active les optimisations statiques dans le pipeline vidéo.</span><span class="sxs-lookup"><span data-stu-id="5b90d-104">Enables static optimizations in the video pipeline.</span></span>

## <a name="data-type"></a><span data-ttu-id="5b90d-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5b90d-105">Data type</span></span>

<span data-ttu-id="5b90d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5b90d-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="5b90d-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="5b90d-107">Get/set</span></span>

<span data-ttu-id="5b90d-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="5b90d-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="5b90d-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="5b90d-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="5b90d-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="5b90d-110">Applies to</span></span>

[<span data-ttu-id="5b90d-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="5b90d-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="5b90d-112">Notes</span><span class="sxs-lookup"><span data-stu-id="5b90d-112">Remarks</span></span>

<span data-ttu-id="5b90d-113">Définissez cet attribut avant de charger une topologie.</span><span class="sxs-lookup"><span data-stu-id="5b90d-113">Set this attribute before loading a topology.</span></span> <span data-ttu-id="5b90d-114">Si l’attribut a la **valeur true**, le chargeur de topologie tente d’optimiser le pipeline avant le démarrage de la lecture.</span><span class="sxs-lookup"><span data-stu-id="5b90d-114">If the attribute is **TRUE**, the topology loader attempts to optimize the pipeline before playback starts.</span></span>

<span data-ttu-id="5b90d-115">Si vous définissez cet attribut, vous devez également définir les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="5b90d-115">If you set this attribute, you should also set the following attributes:</span></span>

-   [<span data-ttu-id="5b90d-116">\_fréquence de lecture de \_ la topologie MF \_</span><span class="sxs-lookup"><span data-stu-id="5b90d-116">MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE</span></span>](mf-topology-playback-framerate.md)
-   [<span data-ttu-id="5b90d-117">\_ \_ nombre maximal de lectures de la topologie \_ MF \_</span><span class="sxs-lookup"><span data-stu-id="5b90d-117">MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS</span></span>](mf-topology-playback-max-dims.md)

<span data-ttu-id="5b90d-118">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5b90d-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="5b90d-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="5b90d-119">Examples</span></span>


```C++
HRESULT SetPlaybackOptimizations(IMFTopology *pTopology, HWND hwnd)
{
    HRESULT hr = pTopology->SetUINT32(
        MF_TOPOLOGY_STATIC_PLAYBACK_OPTIMIZATIONS, TRUE);

    if (FAILED(hr))
    {
        return hr;
    }

    HMONITOR hCurrentMon = MonitorFromWindow(hwnd, MONITOR_DEFAULTTOPRIMARY);

    if (hCurrentMon)
    {
        MONITORINFO MonitorInfo = {0};
        MonitorInfo.cbSize = sizeof(MONITORINFO);

        BOOL fSucceeded = GetMonitorInfo(hCurrentMon, &MonitorInfo);

        if (fSucceeded )
        {
            const RECT& rcMonitor = MonitorInfo.rcMonitor;

            LONG width = rcMonitor.right - rcMonitor.left;
            LONG height = rcMonitor.bottom - rcMonitor.top;

            hr = MFSetAttributeSize(
                pTopology, 
                MF_TOPOLOGY_PLAYBACK_MAX_DIMS, 
                (UINT32)width, (UINT32)height
                );

            if (FAILED(hr))
            {
                goto done;
            }

            HDC hdc = GetDC(hwnd);

            hr = MFSetAttributeRatio(
                pTopology,
                MF_TOPOLOGY_PLAYBACK_FRAMERATE,
                GetDeviceCaps(hdc, VREFRESH), 1
                );

            ReleaseDC(hwnd, hdc);
        }
    }
done:
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="5b90d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b90d-120">Requirements</span></span>



| <span data-ttu-id="5b90d-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b90d-121">Requirement</span></span> | <span data-ttu-id="5b90d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b90d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5b90d-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b90d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5b90d-124">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b90d-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5b90d-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b90d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5b90d-126">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b90d-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5b90d-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b90d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b90d-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b90d-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b90d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b90d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b90d-130">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5b90d-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5b90d-131">Attributs de topologie</span><span class="sxs-lookup"><span data-stu-id="5b90d-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="5b90d-132">Gestion de la qualité vidéo</span><span class="sxs-lookup"><span data-stu-id="5b90d-132">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




