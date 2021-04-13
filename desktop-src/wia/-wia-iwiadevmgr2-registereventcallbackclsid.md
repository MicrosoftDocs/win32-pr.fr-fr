---
description: 'La méthode IWiaDevMgr2 :: RegisterEventCallbackCLSID inscrit une application pour recevoir des événements même si l’application n’est pas en cours d’exécution.'
ms.assetid: e0d421a7-ef49-4e27-9661-c358ac819712
title: 'IWiaDevMgr2 :: RegisterEventCallbackCLSID, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackCLSID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 63e69d12d47f90ba40f5cc785d8b864c40158774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527075"
---
# <a name="iwiadevmgr2registereventcallbackclsid-method"></a><span data-ttu-id="dced0-103">IWiaDevMgr2 :: RegisterEventCallbackCLSID, méthode</span><span class="sxs-lookup"><span data-stu-id="dced0-103">IWiaDevMgr2::RegisterEventCallbackCLSID method</span></span>

<span data-ttu-id="dced0-104">La méthode **IWiaDevMgr2 :: RegisterEventCallbackCLSID** inscrit une application pour recevoir des événements même si l’application n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="dced0-104">The **IWiaDevMgr2::RegisterEventCallbackCLSID** method registers an application to receive events even if the application is not running.</span></span>

## <a name="syntax"></a><span data-ttu-id="dced0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dced0-105">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackCLSID(
  [in]               LONG lFlags,
  [in]               BSTR bstrDeviceID,
  [in]         const GUID *pEventGUID,
  [in, unique] const GUID *pClsID,
  [in]               BSTR bstrName,
  [in]               BSTR bstrDescription,
  [in]               BSTR bstrIcon
);
```



## <a name="parameters"></a><span data-ttu-id="dced0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dced0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dced0-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dced0-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dced0-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="dced0-108">Type: **LONG**</span></span>

<span data-ttu-id="dced0-109">Spécifie les indicateurs d’inscription.</span><span class="sxs-lookup"><span data-stu-id="dced0-109">Specifies registration flags.</span></span> <span data-ttu-id="dced0-110">Peut être défini avec les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="dced0-110">Can be set to the following values:</span></span>



| <span data-ttu-id="dced0-111">Indicateur d’inscription</span><span class="sxs-lookup"><span data-stu-id="dced0-111">Registration Flag</span></span>                | <span data-ttu-id="dced0-112">Signification</span><span class="sxs-lookup"><span data-stu-id="dced0-112">Meaning</span></span>                                           |
|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="dced0-113">\_rappel d' \_ événement de Registre WIA \_</span><span class="sxs-lookup"><span data-stu-id="dced0-113">WIA\_REGISTER\_EVENT\_CALLBACK</span></span>   | <span data-ttu-id="dced0-114">Inscrivez-vous à l’événement.</span><span class="sxs-lookup"><span data-stu-id="dced0-114">Register for the event.</span></span>                           |
| <span data-ttu-id="dced0-115">\_rappel d’événement d’annulation d’inscription WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="dced0-115">WIA\_UNREGISTER\_EVENT\_CALLBACK</span></span> | <span data-ttu-id="dced0-116">Supprimez l’inscription de l’événement.</span><span class="sxs-lookup"><span data-stu-id="dced0-116">Delete the registration for the event.</span></span>            |
| <span data-ttu-id="dced0-117">\_Gestionnaire WIA \_ par défaut \_</span><span class="sxs-lookup"><span data-stu-id="dced0-117">WIA\_SET\_DEFAULT\_HANDLER</span></span>       | <span data-ttu-id="dced0-118">Définissez l’application en tant que gestionnaire d’événements par défaut.</span><span class="sxs-lookup"><span data-stu-id="dced0-118">Set the application as the default event handler.</span></span> |



 

</dd> <dt>

<span data-ttu-id="dced0-119">*bstrDeviceID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dced0-119">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dced0-120">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="dced0-120">Type: **BSTR**</span></span>

<span data-ttu-id="dced0-121">Spécifie un identificateur d’appareil.</span><span class="sxs-lookup"><span data-stu-id="dced0-121">Specifies a device identifier.</span></span> <span data-ttu-id="dced0-122">Transmettez la **valeur null** pour l’inscription de l’événement sur tous les appareils WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="dced0-122">Pass **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="dced0-123">*pEventGUID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dced0-123">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dced0-124">Type : \* #*const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="dced0-124">Type: \**const GUID\** _</span></span>

<span data-ttu-id="dced0-125">Spécifie l’événement pour lequel l’application est inscrite.</span><span class="sxs-lookup"><span data-stu-id="dced0-125">Specifies the event that the application is registering for.</span></span> <span data-ttu-id="dced0-126">Pour obtenir la liste des événements standard, consultez la page [identificateurs d’événements WIA](-wia-wia-event-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="dced0-126">For a list of standard events, see [WIA Event Identifiers](-wia-wia-event-identifiers.md).</span></span>

</dd> <dt>

<span data-ttu-id="dced0-127">_pClsID \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dced0-127">_pClsID\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dced0-128">Type : \* #*const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="dced0-128">Type: \**const GUID\** _</span></span>

<span data-ttu-id="dced0-129">Pointeur vers l’ID de classe d’application (_ \* CLSID \* \*).</span><span class="sxs-lookup"><span data-stu-id="dced0-129">Pointer to the application class ID (_\*CLSID\*\*).</span></span> <span data-ttu-id="dced0-130">Le système d’exécution WIA 2,0 utilise le **CLSID** de l’application pour démarrer l’application quand un événement s’est produit pour lequel il est enregistré.</span><span class="sxs-lookup"><span data-stu-id="dced0-130">The WIA 2.0 run-time system uses the application **CLSID** to start the application when an event occurs that it is registered for.</span></span>

</dd> <dt>

<span data-ttu-id="dced0-131">*bstrName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dced0-131">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dced0-132">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="dced0-132">Type: **BSTR**</span></span>

<span data-ttu-id="dced0-133">Spécifie le nom de l’application qui s’inscrit pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="dced0-133">Specifies the name of the application that registers for the event.</span></span>

</dd> <dt>

<span data-ttu-id="dced0-134">*bstrDescription* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dced0-134">*bstrDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dced0-135">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="dced0-135">Type: **BSTR**</span></span>

<span data-ttu-id="dced0-136">Spécifie une description textuelle de l’application qui s’inscrit pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="dced0-136">Specifies a text description of the application that registers for the event.</span></span>

</dd> <dt>

<span data-ttu-id="dced0-137">*bstrIcon* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dced0-137">*bstrIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dced0-138">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="dced0-138">Type: **BSTR**</span></span>

<span data-ttu-id="dced0-139">Spécifie le nom d’un fichier image à utiliser pour l’icône de l’application qui s’inscrit pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="dced0-139">Specifies the name of an image file to use for the icon for the application that registers for the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dced0-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dced0-140">Return value</span></span>

<span data-ttu-id="dced0-141">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dced0-141">Type: **HRESULT**</span></span>

<span data-ttu-id="dced0-142">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dced0-142">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dced0-143">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dced0-143">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dced0-144">Notes</span><span class="sxs-lookup"><span data-stu-id="dced0-144">Remarks</span></span>

<span data-ttu-id="dced0-145">Les applications WIA 2,0 utilisent cette méthode pour s’inscrire afin de recevoir des événements de périphérique matériel.</span><span class="sxs-lookup"><span data-stu-id="dced0-145">WIA 2.0 applications use this method to register to receive hardware device events.</span></span> <span data-ttu-id="dced0-146">Après l’appel de **IWiaDevMgr2 :: RegisterEventCallbackCLSID** , l’application est inscrite pour recevoir des événements d’appareil WIA 2,0, même s’il n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="dced0-146">After **IWiaDevMgr2::RegisterEventCallbackCLSID** is called, the application is registered to receive WIA 2.0 device events even if it is not running.</span></span>

<span data-ttu-id="dced0-147">Lorsque l’événement se produit, le système WIA 2,0 détermine quelle application est inscrite pour recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="dced0-147">When the event occurs, the WIA 2.0 system determines which application is registered to receive the event.</span></span> <span data-ttu-id="dced0-148">Elle utilise la fonction [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) et le CLSID spécifiés dans le paramètre *pClsID* pour créer une instance de l’application, puis appelle la méthode [**ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) pour transmettre les informations d’événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="dced0-148">It uses the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function and the CLSID specified in the *pClsID* parameter to create an instance of the application, and then calls the [**ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) method to transmit the event information to the application.</span></span>

<span data-ttu-id="dced0-149">Une application peut appeler la méthode [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) pour énumérer les informations d’inscription des événements.</span><span class="sxs-lookup"><span data-stu-id="dced0-149">An application can invoke the [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) method to enumerate event registration information.</span></span>

<span data-ttu-id="dced0-150">Si l’application n’est pas un composant COM (Component Object Model) inscrit et n’est pas compatible avec l’architecture WIA 2,0, utilisez la méthode [**IWiaDevMgr2 :: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) pour inscrire une application pour les événements d’appareil.</span><span class="sxs-lookup"><span data-stu-id="dced0-150">If the application is not a registered Component Object Model (COM) component and is not compatible with the WIA 2.0 architecture, use the [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) method to register an application for device events.</span></span>

> [!Note]  
> <span data-ttu-id="dced0-151">Dans une application multithread, il n’y a aucune garantie que le rappel de notification d’événement soit retourné sur le thread qui a inscrit le rappel.</span><span class="sxs-lookup"><span data-stu-id="dced0-151">In a multi-threaded application, there is no guarantee that the event notification callback is returned on the same thread that registered the callback.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dced0-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dced0-152">Requirements</span></span>



| <span data-ttu-id="dced0-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dced0-153">Requirement</span></span> | <span data-ttu-id="dced0-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="dced0-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dced0-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dced0-155">Minimum supported client</span></span><br/> | <span data-ttu-id="dced0-156">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dced0-156">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dced0-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dced0-157">Minimum supported server</span></span><br/> | <span data-ttu-id="dced0-158">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dced0-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dced0-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="dced0-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="dced0-160"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="dced0-160"><dt>Wia.h</dt></span></span> </dl> |



 

 
