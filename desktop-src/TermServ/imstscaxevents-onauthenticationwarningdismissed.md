---
title: Méthode IMsTscAxEvents OnAuthenticationWarningDismissed
description: Appelé après qu’un contrôle ActiveX affiche une boîte de dialogue d’authentification (par exemple, la boîte de dialogue erreur de certificat).
ms.assetid: bf5dbe4a-9129-47b3-9808-ed09d9010099
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnAuthenticationWarningDismissed
- Méthode OnAuthenticationWarningDismissed Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnAuthenticationWarningDismissed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDismissed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86bdadfdbc8e0a1387a1f3aaf712188689d0f808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384580"
---
# <a name="imstscaxeventsonauthenticationwarningdismissed-method"></a><span data-ttu-id="341a8-106">IMsTscAxEvents :: OnAuthenticationWarningDismissed, méthode</span><span class="sxs-lookup"><span data-stu-id="341a8-106">IMsTscAxEvents::OnAuthenticationWarningDismissed method</span></span>

<span data-ttu-id="341a8-107">Appelé après qu’un contrôle ActiveX affiche une boîte de dialogue d’authentification (par exemple, la boîte de dialogue erreur de certificat).</span><span class="sxs-lookup"><span data-stu-id="341a8-107">Called after an ActiveX control displays an authentication dialog box (for example, the certificate error dialog box).</span></span>

## <a name="syntax"></a><span data-ttu-id="341a8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="341a8-108">Syntax</span></span>


```C++
void OnAuthenticationWarningDismissed();
```



## <a name="parameters"></a><span data-ttu-id="341a8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="341a8-109">Parameters</span></span>

<span data-ttu-id="341a8-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="341a8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="341a8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="341a8-111">Return value</span></span>

<span data-ttu-id="341a8-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="341a8-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="341a8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="341a8-113">Remarks</span></span>

<span data-ttu-id="341a8-114">Si nécessaire, la propriété [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) de l’interface [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) peut être utilisée pour rétablir tout parent éventuellement effectué dans la méthode [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) .</span><span class="sxs-lookup"><span data-stu-id="341a8-114">If needed, the [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) property of the [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) interface can be used to revert any parenting that may have been done in the [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) method.</span></span>

<span data-ttu-id="341a8-115">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="341a8-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="341a8-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="341a8-116">Requirements</span></span>



| <span data-ttu-id="341a8-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="341a8-117">Requirement</span></span> | <span data-ttu-id="341a8-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="341a8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="341a8-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="341a8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="341a8-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="341a8-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="341a8-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="341a8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="341a8-122">Windows Server 2008, Windows Server 2008 avec SP1</span><span class="sxs-lookup"><span data-stu-id="341a8-122">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="341a8-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="341a8-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="341a8-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="341a8-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="341a8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="341a8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="341a8-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="341a8-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="341a8-127">IID</span><span class="sxs-lookup"><span data-stu-id="341a8-127">IID</span></span><br/>                      | <span data-ttu-id="341a8-128">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="341a8-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="341a8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="341a8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="341a8-130">**OnAuthenticationWarningDisplayed**</span><span class="sxs-lookup"><span data-stu-id="341a8-130">**OnAuthenticationWarningDisplayed**</span></span>](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[<span data-ttu-id="341a8-131">**UIParentWindowHandle**</span><span class="sxs-lookup"><span data-stu-id="341a8-131">**UIParentWindowHandle**</span></span>](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[<span data-ttu-id="341a8-132">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="341a8-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





