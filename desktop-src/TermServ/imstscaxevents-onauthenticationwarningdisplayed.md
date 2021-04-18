---
title: Méthode IMsTscAxEvents OnAuthenticationWarningDisplayed
description: Appelé avant qu’un contrôle ActiveX affiche une boîte de dialogue d’authentification (par exemple, la boîte de dialogue erreur de certificat).
ms.assetid: ce307e5f-5e26-4041-bbd5-6871c0678da4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnAuthenticationWarningDisplayed
- Méthode OnAuthenticationWarningDisplayed Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnAuthenticationWarningDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33307adf103536cce5841effe2843a7c48fda357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103528"
---
# <a name="imstscaxeventsonauthenticationwarningdisplayed-method"></a><span data-ttu-id="28560-106">IMsTscAxEvents :: OnAuthenticationWarningDisplayed, méthode</span><span class="sxs-lookup"><span data-stu-id="28560-106">IMsTscAxEvents::OnAuthenticationWarningDisplayed method</span></span>

<span data-ttu-id="28560-107">Appelé avant qu’un contrôle ActiveX affiche une boîte de dialogue d’authentification (par exemple, la boîte de dialogue erreur de certificat).</span><span class="sxs-lookup"><span data-stu-id="28560-107">Called before an ActiveX control displays an authentication dialog box (for example, the certificate error dialog box).</span></span>

## <a name="syntax"></a><span data-ttu-id="28560-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28560-108">Syntax</span></span>


```C++
void OnAuthenticationWarningDisplayed();
```



## <a name="parameters"></a><span data-ttu-id="28560-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28560-109">Parameters</span></span>

<span data-ttu-id="28560-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="28560-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28560-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28560-111">Return value</span></span>

<span data-ttu-id="28560-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="28560-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="28560-113">Notes</span><span class="sxs-lookup"><span data-stu-id="28560-113">Remarks</span></span>

<span data-ttu-id="28560-114">Si nécessaire, la propriété [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) de l’interface [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) peut être utilisée pour s’assurer que la boîte de dialogue d’authentification modale à afficher est apparentée par une fenêtre spécifiée (cela peut être nécessaire pour empêcher les utilisateurs d’utiliser d’autres boîtes de dialogue pendant que la boîte de dialogue d’authentification est affichée).</span><span class="sxs-lookup"><span data-stu-id="28560-114">If needed, the [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) property of the [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) interface can be used to ensure that the modal authentication dialog to be displayed will be parented by a specified window (this may be necessary to prevent users from using other dialog boxes while the authentication dialog box is displayed).</span></span> <span data-ttu-id="28560-115">Par défaut, le parent est la fenêtre contrôle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="28560-115">By default, the parent is the ActiveX control window.</span></span>

<span data-ttu-id="28560-116">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="28560-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="28560-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28560-117">Requirements</span></span>



| <span data-ttu-id="28560-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28560-118">Requirement</span></span> | <span data-ttu-id="28560-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="28560-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28560-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28560-120">Minimum supported client</span></span><br/> | <span data-ttu-id="28560-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28560-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="28560-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28560-122">Minimum supported server</span></span><br/> | <span data-ttu-id="28560-123">Windows Server 2008, Windows Server 2008 avec SP1</span><span class="sxs-lookup"><span data-stu-id="28560-123">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="28560-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="28560-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="28560-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28560-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="28560-126">DLL</span><span class="sxs-lookup"><span data-stu-id="28560-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28560-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28560-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="28560-128">IID</span><span class="sxs-lookup"><span data-stu-id="28560-128">IID</span></span><br/>                      | <span data-ttu-id="28560-129">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="28560-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="28560-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28560-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28560-131">**OnAuthenticationWarningDismissed**</span><span class="sxs-lookup"><span data-stu-id="28560-131">**OnAuthenticationWarningDismissed**</span></span>](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[<span data-ttu-id="28560-132">**UIParentWindowHandle**</span><span class="sxs-lookup"><span data-stu-id="28560-132">**UIParentWindowHandle**</span></span>](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[<span data-ttu-id="28560-133">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="28560-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





