---
title: Méthode IAccessibilityDockingService GetAvailableSize
description: Obtient les dimensions disponibles pour l’ancrage d’une fenêtre d’accessibilité sur une analyse.
ms.assetid: 1C838B01-EF26-4FCC-878F-A36DEFBA3142
keywords:
- Méthode GetAvailableSize COM
- Méthode GetAvailableSize COM, interface IAccessibilityDockingService
- Interface IAccessibilityDockingService COM, méthode GetAvailableSize
topic_type:
- apiref
api_name:
- IAccessibilityDockingService.GetAvailableSize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1b9f113792b14f5fb86e0349d083ea48ffdb3fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030178"
---
# <a name="iaccessibilitydockingservicegetavailablesize-method"></a><span data-ttu-id="cfa7b-106">IAccessibilityDockingService :: GetAvailableSize, méthode</span><span class="sxs-lookup"><span data-stu-id="cfa7b-106">IAccessibilityDockingService::GetAvailableSize method</span></span>

<span data-ttu-id="cfa7b-107">Obtient les dimensions disponibles pour l’ancrage d’une fenêtre d’accessibilité sur une analyse.</span><span class="sxs-lookup"><span data-stu-id="cfa7b-107">Gets the dimensions available for docking an accessibility window on a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfa7b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfa7b-108">Syntax</span></span>


```C++
HRESULT GetAvailableSize(
  [in]  HMONITOR hMonitor,
  [out] UINT     *puMaxHeight,
  [out] UINT     *puFixedWidth
);
```



## <a name="parameters"></a><span data-ttu-id="cfa7b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cfa7b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfa7b-110">*hMonitor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cfa7b-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfa7b-111">Spécifie le moniteur pour lequel la taille d’ancrage disponible sera récupérée.</span><span class="sxs-lookup"><span data-stu-id="cfa7b-111">Specifies the monitor for which the available docking size will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="cfa7b-112">*puMaxHeight* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cfa7b-112">*puMaxHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfa7b-113">En cas de réussite, définissez la hauteur maximale disponible pour l’ancrage sur le *hMonitor* spécifié, en pixels.</span><span class="sxs-lookup"><span data-stu-id="cfa7b-113">On success, set to the maximum height available for docking on the specified *hMonitor*, in pixels.</span></span>

<span data-ttu-id="cfa7b-114">En cas d’échec, définissez sur zéro.</span><span class="sxs-lookup"><span data-stu-id="cfa7b-114">On failure, set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="cfa7b-115">*puFixedWidth* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cfa7b-115">*puFixedWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfa7b-116">En cas de réussite, définissez la largeur fixe disponible pour l’ancrage sur le *hMonitor* spécifié, en pixels.</span><span class="sxs-lookup"><span data-stu-id="cfa7b-116">On success, set to the fixed width available for docking on the specified *hMonitor*, in pixels.</span></span> <span data-ttu-id="cfa7b-117">Toute fenêtre ancrée à ce *hMonitor* sera dimensionnée à cette largeur.</span><span class="sxs-lookup"><span data-stu-id="cfa7b-117">Any window docked to this *hMonitor* will be sized to this width.</span></span>

<span data-ttu-id="cfa7b-118">En cas d’échec, définissez sur zéro.</span><span class="sxs-lookup"><span data-stu-id="cfa7b-118">On failure, set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfa7b-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cfa7b-119">Return value</span></span>



| <span data-ttu-id="cfa7b-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="cfa7b-120">Return code</span></span>                                                                                                                          | <span data-ttu-id="cfa7b-121">Description</span><span class="sxs-lookup"><span data-stu-id="cfa7b-121">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cfa7b-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cfa7b-122"><dt>**S\_OK**</dt></span></span> </dl>                                                 | <span data-ttu-id="cfa7b-123">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="cfa7b-123">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="cfa7b-124"><dt>**HRESULT \_ à partir de \_ Win32 (handle de moniteur d’erreur \_ non valide \_ \_ )**</dt></span><span class="sxs-lookup"><span data-stu-id="cfa7b-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_MONITOR\_HANDLE)**</dt></span></span> </dl> | <span data-ttu-id="cfa7b-125">L’analyse spécifiée par le descripteur du moniteur ne prend pas en charge l’ancrage.</span><span class="sxs-lookup"><span data-stu-id="cfa7b-125">The monitor specified by the monitor handle does not support docking.</span></span><br/> |



 

<span data-ttu-id="cfa7b-126">Si *puMaxHeight* ou *puFixedWidth* a la valeur null, une violation d’accès se produit.</span><span class="sxs-lookup"><span data-stu-id="cfa7b-126">If either *puMaxHeight* or *puFixedWidth* are null, an access violation will occur.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfa7b-127">Notes</span><span class="sxs-lookup"><span data-stu-id="cfa7b-127">Remarks</span></span>

<span data-ttu-id="cfa7b-128">Les fenêtres d’accessibilité peuvent uniquement être ancrées à une analyse qui a au moins 768 pixels d’écran verticaux.</span><span class="sxs-lookup"><span data-stu-id="cfa7b-128">Accessibility windows can only be docked to a monitor that has at least 768 vertical screen pixels.</span></span> <span data-ttu-id="cfa7b-129">Cette API n’autorise pas l’ancrage de ces fenêtres avec une hauteur qui amènerait les applications du Windows Store à avoir moins de 768 pixels d’écran verticaux.</span><span class="sxs-lookup"><span data-stu-id="cfa7b-129">This API will not allow such windows to be docked with a height that would cause Windows Store apps to have less than 768 vertical screen pixels.</span></span>

## <a name="examples"></a><span data-ttu-id="cfa7b-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="cfa7b-130">Examples</span></span>


```
IAccessibilityDockingService *pDockingService;
HRESULT hr = CoCreateInstance(CLSID_AccessibilityDockingService, CLSCTX_INPROV_SERVER, nullptr, IID_PPV_ARGS(&pDockingService));
if (SUCCEEDED(hr))
{
    UINT uMaxHeight;
    UINT uFixedWidth;

    HMONITOR hMonitor = MonitorFromWindow(_hwndMyApplication, MONITOR_DEFAULTTONULL);
    if (hMonitor != nullptr)
    {
        hr = pDockingService->GetAvailableSize(hMonitor, &uMaxHeight, &uFixedWidth);
    }
}
```



## <a name="see-also"></a><span data-ttu-id="cfa7b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfa7b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfa7b-132">**IAccessibilityDockingService**</span><span class="sxs-lookup"><span data-stu-id="cfa7b-132">**IAccessibilityDockingService**</span></span>](/windows/desktop/api/shobjidl/nn-shobjidl-iaccessibilitydockingservice)
</dt> </dl>

 

 





