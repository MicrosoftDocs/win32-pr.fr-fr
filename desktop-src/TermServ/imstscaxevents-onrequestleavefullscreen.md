---
title: Méthode IMsTscAxEvents OnRequestLeaveFullScreen
description: Appelée lorsque le client demande à conserver le mode plein écran et que la propriété IMsTscAdvancedSettings put \_ ContainerHandledFullScreen a été définie sur une valeur différente de zéro.
ms.assetid: db6ee012-8288-4360-98b2-12858ea65baa
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnRequestLeaveFullScreen
- Méthode OnRequestLeaveFullScreen Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnRequestLeaveFullScreen
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestLeaveFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e814d6153e32fdf4fa498a6630fc9ca2908510e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742093"
---
# <a name="imstscaxeventsonrequestleavefullscreen-method"></a><span data-ttu-id="21418-106">IMsTscAxEvents :: OnRequestLeaveFullScreen, méthode</span><span class="sxs-lookup"><span data-stu-id="21418-106">IMsTscAxEvents::OnRequestLeaveFullScreen method</span></span>

<span data-ttu-id="21418-107">Appelée lorsque le client demande à conserver le mode plein écran et que la propriété [**IMsTscAdvancedSettings ::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) a été définie sur une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="21418-107">Called when the client requests to leave full-screen mode and the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) property has been set to a nonzero value.</span></span>

## <a name="syntax"></a><span data-ttu-id="21418-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21418-108">Syntax</span></span>


```C++
void OnRequestLeaveFullScreen();
```



## <a name="parameters"></a><span data-ttu-id="21418-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21418-109">Parameters</span></span>

<span data-ttu-id="21418-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="21418-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21418-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="21418-111">Return value</span></span>

<span data-ttu-id="21418-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="21418-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="21418-113">Notes</span><span class="sxs-lookup"><span data-stu-id="21418-113">Remarks</span></span>

<span data-ttu-id="21418-114">En mode plein écran géré par un conteneur, le conteneur doit conserver le mode plein écran standard en réponse à cet événement.</span><span class="sxs-lookup"><span data-stu-id="21418-114">In container-handled full-screen mode, the container should leave standard full-screen mode in response to this event.</span></span>

<span data-ttu-id="21418-115">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="21418-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="21418-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21418-116">Requirements</span></span>



| <span data-ttu-id="21418-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21418-117">Requirement</span></span> | <span data-ttu-id="21418-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="21418-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21418-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21418-119">Minimum supported client</span></span><br/> | <span data-ttu-id="21418-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21418-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="21418-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21418-121">Minimum supported server</span></span><br/> | <span data-ttu-id="21418-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21418-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="21418-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="21418-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="21418-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21418-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="21418-125">DLL</span><span class="sxs-lookup"><span data-stu-id="21418-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21418-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21418-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="21418-127">IID</span><span class="sxs-lookup"><span data-stu-id="21418-127">IID</span></span><br/>                      | <span data-ttu-id="21418-128">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="21418-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="21418-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21418-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21418-130">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="21418-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





