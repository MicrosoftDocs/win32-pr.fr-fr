---
description: Inscrit une application en cours d’exécution pour la notification d’événements WIA (Windows Image Acquisition) 2,0.
ms.assetid: 978dcd41-d63b-421d-b7e1-8e9368b36180
title: 'IWiaDevMgr2 :: RegisterEventCallbackInterface, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackInterface
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7cd3a7e00cff56bc5d91bfc843ab79fe71aa1123
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202887"
---
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a><span data-ttu-id="f98bc-103">IWiaDevMgr2 :: RegisterEventCallbackInterface, méthode</span><span class="sxs-lookup"><span data-stu-id="f98bc-103">IWiaDevMgr2::RegisterEventCallbackInterface method</span></span>

<span data-ttu-id="f98bc-104">Inscrit une application en cours d’exécution pour la notification d’événements WIA (Windows Image Acquisition) 2,0.</span><span class="sxs-lookup"><span data-stu-id="f98bc-104">Registers a running application for Windows Image Acquisition (WIA) 2.0 event notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="f98bc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f98bc-105">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackInterface(
  [in]        LONG              lFlags,
  [in]        BSTR              bstrDeviceID,
  [in]  const GUID              *pEventGUID,
  [in]        IWiaEventCallback *pIWiaEventCallback,
  [out]       IUnknown          **pEventObject
);
```



## <a name="parameters"></a><span data-ttu-id="f98bc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f98bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f98bc-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f98bc-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f98bc-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="f98bc-108">Type: **LONG**</span></span>

<span data-ttu-id="f98bc-109">Actuellement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="f98bc-109">Currently unused.</span></span> <span data-ttu-id="f98bc-110">Doit être défini sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="f98bc-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="f98bc-111">*bstrDeviceID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f98bc-111">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f98bc-112">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f98bc-112">Type: **BSTR**</span></span>

<span data-ttu-id="f98bc-113">Spécifie l’identificateur unique d’un appareil WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="f98bc-113">Specifies the unique identifier of a WIA 2.0 device.</span></span> <span data-ttu-id="f98bc-114">Affectez la valeur **null** à ce paramètre pour vous inscrire à l’événement sur tous les appareils WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="f98bc-114">Set this parameter to **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="f98bc-115">*pEventGUID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f98bc-115">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f98bc-116">Type : \* #*const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="f98bc-116">Type: \**const GUID\** _</span></span>

<span data-ttu-id="f98bc-117">Spécifie un pointeur vers l’identificateur d’événement pour lequel l’application est inscrite.</span><span class="sxs-lookup"><span data-stu-id="f98bc-117">Specifies a pointer to the event identifier that the application is registering for.</span></span> <span data-ttu-id="f98bc-118">Consultez [identificateurs d’événements WIA](-wia-wia-event-identifiers.md) pour les identificateurs d’événements standard.</span><span class="sxs-lookup"><span data-stu-id="f98bc-118">See [WIA Event Identifiers](-wia-wia-event-identifiers.md) for standard event identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="f98bc-119">_pIWiaEventCallback \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f98bc-119">_pIWiaEventCallback\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f98bc-120">Tapez : \**[**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) \** _</span><span class="sxs-lookup"><span data-stu-id="f98bc-120">Type: \**[**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback)\** _</span></span>

<span data-ttu-id="f98bc-121">Spécifie un pointeur vers l’interface [_ *IWiaEventCallback* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) que l’WIA 2,0 utilise pour envoyer une notification d’événement.</span><span class="sxs-lookup"><span data-stu-id="f98bc-121">Specifies a pointer to the [_ *IWiaEventCallback*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) interface that the WIA 2.0 uses to send event notification.</span></span>

</dd> <dt>

<span data-ttu-id="f98bc-122">*pEventObject* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f98bc-122">*pEventObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f98bc-123">Type : **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="f98bc-123">Type: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="f98bc-124">Reçoit l’adresse d’un pointeur vers l’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f98bc-124">Receives the address of a pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f98bc-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f98bc-125">Return value</span></span>

<span data-ttu-id="f98bc-126">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f98bc-126">Type: **HRESULT**</span></span>

<span data-ttu-id="f98bc-127">Retourne les codes d’erreur COM standard ou les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="f98bc-127">Returns the standard COM error codes or the following.</span></span>



| <span data-ttu-id="f98bc-128">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f98bc-128">Return code</span></span>                                                                               | <span data-ttu-id="f98bc-129">Description</span><span class="sxs-lookup"><span data-stu-id="f98bc-129">Description</span></span>                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f98bc-130"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="f98bc-130"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="f98bc-131">L’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) ne peut pas être retournée.</span><span class="sxs-lookup"><span data-stu-id="f98bc-131">The [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface cannot be returned.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="f98bc-132">Notes</span><span class="sxs-lookup"><span data-stu-id="f98bc-132">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="f98bc-133">L’utilisation des méthodes [**IWiaDevMgr :: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2 :: RegisterEventCallbackInterface** et [**devicemanager. RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) à partir du même processus après le redémarrage du service image continue peut entraîner une violation d’accès, si les fonctions ont été utilisées avant l’arrêt du service.</span><span class="sxs-lookup"><span data-stu-id="f98bc-133">Using the [**IWiaDevMgr::RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2::RegisterEventCallbackInterface**, and [**DeviceManager.RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) methods from the same process after the Still Image Service is restarted may cause an access violation, if the functions were used before the service was stopped.</span></span>

 

<span data-ttu-id="f98bc-134">Lorsque les applications WIA 2,0 commencent à s’exécuter, elles utilisent cette méthode pour s’inscrire afin de recevoir des événements de périphérique matériel.</span><span class="sxs-lookup"><span data-stu-id="f98bc-134">When WIA 2.0 applications begin executing, they use this method to register to receive hardware device events.</span></span> <span data-ttu-id="f98bc-135">Cela empêche l’application d’être redémarrée lorsqu’un autre événement pour lequel elle est inscrite se produit.</span><span class="sxs-lookup"><span data-stu-id="f98bc-135">This prevents the application from being restarted when another event for which it is registered occurs.</span></span> <span data-ttu-id="f98bc-136">Une fois qu’une application appelle **IWiaDevMgr2 :: RegisterEventCallbackInterface** pour s’inscrire pour recevoir les événements WIA 2,0 d’un appareil, les événements inscrits sont acheminés vers le programme par WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="f98bc-136">Once an application calls **IWiaDevMgr2::RegisterEventCallbackInterface** to register itself to receive WIA 2.0 events from a device, the registered events are routed to the program by WIA 2.0.</span></span>

<span data-ttu-id="f98bc-137">Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *pEventObject* .</span><span class="sxs-lookup"><span data-stu-id="f98bc-137">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *pEventObject* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="f98bc-138">Dans une application multithread, le rappel de notification d’événements peut se trouver sur un thread différent de celui qui a inscrit le rappel.</span><span class="sxs-lookup"><span data-stu-id="f98bc-138">In a multithreaded application, the event notification callback may come in on a different thread from the one that registered the callback.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f98bc-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f98bc-139">Requirements</span></span>



| <span data-ttu-id="f98bc-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f98bc-140">Requirement</span></span> | <span data-ttu-id="f98bc-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="f98bc-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f98bc-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f98bc-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f98bc-143">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f98bc-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f98bc-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f98bc-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f98bc-145">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f98bc-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f98bc-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="f98bc-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="f98bc-147"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="f98bc-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="f98bc-148">MIDL</span><span class="sxs-lookup"><span data-stu-id="f98bc-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f98bc-149"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f98bc-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 
