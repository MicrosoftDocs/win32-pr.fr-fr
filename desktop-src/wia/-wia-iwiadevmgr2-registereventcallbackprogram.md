---
description: 'La méthode IWiaDevMgr2 :: RegisterEventCallbackProgram inscrit une application pour recevoir des événements d’appareil. Il est principalement fourni pour la compatibilité descendante avec les applications qui n’ont pas été écrites pour l’acquisition d’images Windows (WIA) 2,0.'
ms.assetid: 6b427f19-719b-44ce-8e2c-3c44672345c8
title: 'IWiaDevMgr2 :: RegisterEventCallbackProgram, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackProgram
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b18b5833b7616493c24f0128caa7c910b685e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545798"
---
# <a name="iwiadevmgr2registereventcallbackprogram-method"></a><span data-ttu-id="bb45d-104">IWiaDevMgr2 :: RegisterEventCallbackProgram, méthode</span><span class="sxs-lookup"><span data-stu-id="bb45d-104">IWiaDevMgr2::RegisterEventCallbackProgram method</span></span>

<span data-ttu-id="bb45d-105">La méthode **IWiaDevMgr2 :: RegisterEventCallbackProgram** inscrit une application pour recevoir des événements d’appareil.</span><span class="sxs-lookup"><span data-stu-id="bb45d-105">The **IWiaDevMgr2::RegisterEventCallbackProgram** method registers an application to receive device events.</span></span> <span data-ttu-id="bb45d-106">Il est principalement fourni pour la compatibilité descendante avec les applications qui n’ont pas été écrites pour l’acquisition d’images Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="bb45d-106">It is primarily provided for backward compatibility with applications that were not written for Windows Image Acquisition (WIA) 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb45d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb45d-107">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackProgram(
  [in]       LONG lFlags,
  [in]       BSTR bstrDeviceID,
  [in] const GUID *pEventGUID,
  [in]       BSTR bstrFullAppName,
  [in]       BSTR bstrCommandlineArg,
  [in]       BSTR bstrName,
  [in]       BSTR bstrDescription,
  [in]       BSTR bstrIcon
);
```



## <a name="parameters"></a><span data-ttu-id="bb45d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb45d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb45d-109">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb45d-109">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb45d-110">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="bb45d-110">Type: **LONG**</span></span>

<span data-ttu-id="bb45d-111">Indicateurs d’inscription.</span><span class="sxs-lookup"><span data-stu-id="bb45d-111">The registration flags.</span></span> <span data-ttu-id="bb45d-112">Peut être défini avec les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="bb45d-112">Can be set to the following values.</span></span>



| <span data-ttu-id="bb45d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb45d-113">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="bb45d-114">Signification</span><span class="sxs-lookup"><span data-stu-id="bb45d-114">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="WIA_REGISTER_EVENT_CALLBACK"></span><span id="wia_register_event_callback"></span><dl> <span data-ttu-id="bb45d-115"><dt>**\_rappel d' \_ événement de Registre WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bb45d-115"><dt>**WIA\_REGISTER\_EVENT\_CALLBACK**</dt></span></span> </dl>       | <span data-ttu-id="bb45d-116">Inscrivez-vous à l’événement.</span><span class="sxs-lookup"><span data-stu-id="bb45d-116">Register for the event.</span></span><br/>                           |
| <span id="WIA_UNREGISTER_EVENT_CALLBACK"></span><span id="wia_unregister_event_callback"></span><dl> <span data-ttu-id="bb45d-117"><dt>**\_rappel d’événement d’annulation d’inscription WIA \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bb45d-117"><dt>**WIA\_UNREGISTER\_EVENT\_CALLBACK**</dt></span></span> </dl> | <span data-ttu-id="bb45d-118">Supprimez l’inscription de l’événement.</span><span class="sxs-lookup"><span data-stu-id="bb45d-118">Delete the registration for the event.</span></span><br/>            |
| <span id="WIA_SET_DEFAULT_HANDLER"></span><span id="wia_set_default_handler"></span><dl> <span data-ttu-id="bb45d-119"><dt>**\_Gestionnaire WIA \_ par défaut \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bb45d-119"><dt>**WIA\_SET\_DEFAULT\_HANDLER**</dt></span></span> </dl>                   | <span data-ttu-id="bb45d-120">Définissez l’application en tant que gestionnaire d’événements par défaut.</span><span class="sxs-lookup"><span data-stu-id="bb45d-120">Set the application as the default event handler.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bb45d-121">*bstrDeviceID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb45d-121">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb45d-122">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bb45d-122">Type: **BSTR**</span></span>

<span data-ttu-id="bb45d-123">Identificateur d’appareil.</span><span class="sxs-lookup"><span data-stu-id="bb45d-123">A device identifier.</span></span> <span data-ttu-id="bb45d-124">Transmettez la **valeur null** pour l’inscription de l’événement sur tous les appareils WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="bb45d-124">Pass **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="bb45d-125">*pEventGUID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb45d-125">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb45d-126">Type : \* #*const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="bb45d-126">Type: \**const GUID\** _</span></span>

<span data-ttu-id="bb45d-127">Événement pour lequel l’application est inscrite.</span><span class="sxs-lookup"><span data-stu-id="bb45d-127">The event that the application is registering for.</span></span> <span data-ttu-id="bb45d-128">Pour obtenir la liste des GUID d’événements valides, consultez la page [identificateurs d’événements WIA](-wia-wia-event-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="bb45d-128">For a list of valid event GUIDs, see [WIA Event Identifiers](-wia-wia-event-identifiers.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb45d-129">_bstrFullAppName \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb45d-129">_bstrFullAppName\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb45d-130">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bb45d-130">Type: **BSTR**</span></span>

<span data-ttu-id="bb45d-131">Nom de chemin d’accès complet de l’application.</span><span class="sxs-lookup"><span data-stu-id="bb45d-131">The full path name of the application.</span></span>

</dd> <dt>

<span data-ttu-id="bb45d-132">*bstrCommandlineArg* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb45d-132">*bstrCommandlineArg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb45d-133">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bb45d-133">Type: **BSTR**</span></span>

<span data-ttu-id="bb45d-134">Arguments de ligne de commande appropriés pour l’application.</span><span class="sxs-lookup"><span data-stu-id="bb45d-134">The appropriate command-line arguments for the application.</span></span>

</dd> <dt>

<span data-ttu-id="bb45d-135">*bstrName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb45d-135">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb45d-136">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bb45d-136">Type: **BSTR**</span></span>

<span data-ttu-id="bb45d-137">Le nom de l’application.</span><span class="sxs-lookup"><span data-stu-id="bb45d-137">The name of the application.</span></span> <span data-ttu-id="bb45d-138">Le nom est affiché à l’utilisateur lorsque plusieurs applications s’inscrivent pour le même événement.</span><span class="sxs-lookup"><span data-stu-id="bb45d-138">The name is displayed to the user when multiple applications register for the same event.</span></span>

</dd> <dt>

<span data-ttu-id="bb45d-139">*bstrDescription* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb45d-139">*bstrDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb45d-140">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bb45d-140">Type: **BSTR**</span></span>

<span data-ttu-id="bb45d-141">Description de l’application.</span><span class="sxs-lookup"><span data-stu-id="bb45d-141">The description of the application.</span></span> <span data-ttu-id="bb45d-142">La description est présentée à l’utilisateur lorsque plusieurs applications s’inscrivent pour le même événement.</span><span class="sxs-lookup"><span data-stu-id="bb45d-142">The description is displayed to the user when multiple applications register for the same event.</span></span>

</dd> <dt>

<span data-ttu-id="bb45d-143">*bstrIcon* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb45d-143">*bstrIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb45d-144">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bb45d-144">Type: **BSTR**</span></span>

<span data-ttu-id="bb45d-145">Icône qui représente l’application.</span><span class="sxs-lookup"><span data-stu-id="bb45d-145">The icon that represents the application.</span></span> <span data-ttu-id="bb45d-146">L’icône s’affiche pour l’utilisateur lorsque plusieurs applications s’inscrivent pour le même événement.</span><span class="sxs-lookup"><span data-stu-id="bb45d-146">The icon is displayed to the user when multiple applications register for the same event.</span></span> <span data-ttu-id="bb45d-147">La chaîne contient le nom de l’application et l’index de base zéro de l’icône, séparés par une virgule, par exemple « MyApp, 0 ».</span><span class="sxs-lookup"><span data-stu-id="bb45d-147">The string contains the name of the application and the zero-based index of the icon separated by a comma, for example, "MyApp, 0".</span></span> <span data-ttu-id="bb45d-148">Il peut y avoir plus d’une icône qui représente une application.</span><span class="sxs-lookup"><span data-stu-id="bb45d-148">There might be more than one icon that represents an application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb45d-149">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bb45d-149">Return value</span></span>

<span data-ttu-id="bb45d-150">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bb45d-150">Type: **HRESULT**</span></span>

<span data-ttu-id="bb45d-151">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bb45d-151">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bb45d-152">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bb45d-152">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb45d-153">Notes</span><span class="sxs-lookup"><span data-stu-id="bb45d-153">Remarks</span></span>

<span data-ttu-id="bb45d-154">Utilisez **IWiaDevMgr2 :: RegisterEventCallbackProgram** pour vous inscrire pour les événements de périphérique matériel.</span><span class="sxs-lookup"><span data-stu-id="bb45d-154">Use **IWiaDevMgr2::RegisterEventCallbackProgram** to register for hardware device events.</span></span> <span data-ttu-id="bb45d-155">Lorsqu’un événement se produit lorsqu’une application est inscrite, l’application est lancée et les informations sur l’événement sont transmises à l’application.</span><span class="sxs-lookup"><span data-stu-id="bb45d-155">When an event occurs that an application is registered for, the application is launched, and the event information is transmitted to the application.</span></span>

<span data-ttu-id="bb45d-156">Utilisez la méthode [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) pour récupérer un pointeur vers un objet énumérateur pour les propriétés d’inscription des événements.</span><span class="sxs-lookup"><span data-stu-id="bb45d-156">Use the [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) method to retrieve a pointer to an enumerator object for event registration properties.</span></span>

<span data-ttu-id="bb45d-157">Utilisez la méthode **IWiaDevMgr2 :: RegisterEventCallbackProgram** uniquement pour la compatibilité descendante avec les applications non écrites pour l’architecture WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="bb45d-157">Only use the **IWiaDevMgr2::RegisterEventCallbackProgram** method for backward compatibility with applications not written for the WIA 2.0 architecture.</span></span> <span data-ttu-id="bb45d-158">Utilisez les interfaces COM (Component Object Model) fournies par l’architecture WIA 2,0 pour les nouvelles applications.</span><span class="sxs-lookup"><span data-stu-id="bb45d-158">Use the Component Object Model (COM) interfaces provided by the WIA 2.0 architecture for new applications.</span></span> <span data-ttu-id="bb45d-159">En particulier, appelez [**IWiaDevMgr2 :: RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) ou [**IWiaDevMgr2 :: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) pour inscrire une nouvelle application pour les événements d’appareil.</span><span class="sxs-lookup"><span data-stu-id="bb45d-159">Specifically, call [**IWiaDevMgr2::RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) or [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) to register a new application for device events.</span></span>

<span data-ttu-id="bb45d-160">En règle générale, cette méthode est appelée par un programme d’installation ou un script.</span><span class="sxs-lookup"><span data-stu-id="bb45d-160">Typically, this method is called by an install program or a script.</span></span> <span data-ttu-id="bb45d-161">Le programme ou le script d’installation inscrit l’application pour recevoir des événements d’appareil WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="bb45d-161">The install program or script registers the application to receive WIA 2.0 device events.</span></span> <span data-ttu-id="bb45d-162">Lorsque l’événement se produit, l’application est démarrée par le système d’exécution WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="bb45d-162">When the event occurs, the application is started by the WIA 2.0 run-time system.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb45d-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb45d-163">Requirements</span></span>



| <span data-ttu-id="bb45d-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb45d-164">Requirement</span></span> | <span data-ttu-id="bb45d-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb45d-165">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bb45d-166">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb45d-166">Minimum supported client</span></span><br/> | <span data-ttu-id="bb45d-167">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb45d-167">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bb45d-168">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb45d-168">Minimum supported server</span></span><br/> | <span data-ttu-id="bb45d-169">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb45d-169">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bb45d-170">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb45d-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb45d-171"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb45d-171"><dt>Wia.h</dt></span></span> </dl> |



 

 




