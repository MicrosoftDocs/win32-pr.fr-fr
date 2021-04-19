---
description: S’abonne aux notifications de modification de l’état du service à l’aide d’une fonction de rappel.
ms.assetid: d67113eb-2141-444c-9f09-eaa772bcad8a
title: SubscribeServiceChangeNotifications, fonction (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: e327a44d613b514123862b1ddcb1bf302fea63ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527234"
---
# <a name="subscribeservicechangenotifications-function"></a><span data-ttu-id="8e40f-103">SubscribeServiceChangeNotifications fonction)</span><span class="sxs-lookup"><span data-stu-id="8e40f-103">SubscribeServiceChangeNotifications function</span></span>

<span data-ttu-id="8e40f-104">S’abonne aux notifications de modification de l’état du service à l’aide d’une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="8e40f-104">Subscribes for service status change notifications using a callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e40f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e40f-105">Syntax</span></span>


```C++
DWORD WINAPI SubscribeServiceChangeNotifications(
  _In_     SC_HANDLE                     hService,
  _In_     SC_EVENT_TYPE                 eEventType,
  _In_     PSC_NOTIFICATION_CALLBACK     pCallback,
  _In_opt_ PVOID                         pCallbackContext,
  _Out_    PSC_NOTIFICATION_REGISTRATION *pSubscription
);
```



## <a name="parameters"></a><span data-ttu-id="8e40f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e40f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e40f-107">*hService* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e40f-107">*hService* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e40f-108">Un handle vers le service ou un handle vers le gestionnaire de contrôle des services (SCM) pour surveiller les modifications.</span><span class="sxs-lookup"><span data-stu-id="8e40f-108">A handle to the service or a handle to the service control manager (SCM) to monitor for changes.</span></span>

<span data-ttu-id="8e40f-109">Les handles vers les services sont retournés par les fonctions [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) et [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) et doivent disposer du droit d’accès **\_ \_ État** de la requête de service.</span><span class="sxs-lookup"><span data-stu-id="8e40f-109">Handles to services are returned by the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) and [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function and must have the **SERVICE\_QUERY\_STATUS** access right.</span></span> <span data-ttu-id="8e40f-110">Les handles du gestionnaire de contrôle des services sont retournés par la fonction [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) et doivent disposer du droit d' **\_ \_ énumérer \_** l’accès au service du gestionnaire SC.</span><span class="sxs-lookup"><span data-stu-id="8e40f-110">Handles to the service control manager are returned by the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function and must have the **SC\_MANAGER\_ENUMERATE\_SERVICE** access right.</span></span>

</dd> <dt>

<span data-ttu-id="8e40f-111">*eEventType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e40f-111">*eEventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e40f-112">Spécifie le type de modification d’État qui doit être signalé.</span><span class="sxs-lookup"><span data-stu-id="8e40f-112">Specifies the type of status changes that should be reported.</span></span> <span data-ttu-id="8e40f-113">Ce paramètre est défini sur l’une des valeurs spécifiées dans le [**\_ \_ type d’événement SC**](sc-event-type.md).</span><span class="sxs-lookup"><span data-stu-id="8e40f-113">This parameter is set to one of the values specified in [**SC\_EVENT\_TYPE**](sc-event-type.md).</span></span> <span data-ttu-id="8e40f-114">Le comportement de cette fonction est différent selon le type d’événement, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="8e40f-114">The behavior for this function is different depending on the event type as follows.</span></span>



| <span data-ttu-id="8e40f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e40f-115">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="8e40f-116">Signification</span><span class="sxs-lookup"><span data-stu-id="8e40f-116">Meaning</span></span>                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span><dl> <span data-ttu-id="8e40f-117"><dt>**SC \_ \_ \_ Modification de la base de données d’événements**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8e40f-117"><dt>**SC\_EVENT\_DATABASE\_CHANGE**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="8e40f-118">Un service a été ajouté ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="8e40f-118">A service has been added or deleted.</span></span> <span data-ttu-id="8e40f-119">Le paramètre *hService* doit être un handle vers le SCM.</span><span class="sxs-lookup"><span data-stu-id="8e40f-119">The *hService* parameter must be a handle to the SCM.</span></span><br/>                  |
| <span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span><dl> <span data-ttu-id="8e40f-120"><dt>**SC \_ \_ \_ Modification**</dt> de la propriété d’événement <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8e40f-120"><dt>**SC\_EVENT\_PROPERTY\_CHANGE**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="8e40f-121">Une ou plusieurs propriétés de service ont été mises à jour.</span><span class="sxs-lookup"><span data-stu-id="8e40f-121">One or more service properties have been updated.</span></span> <span data-ttu-id="8e40f-122">Le paramètre *hService* doit être un handle vers le service.</span><span class="sxs-lookup"><span data-stu-id="8e40f-122">The *hService* parameter must be a handle to the service.</span></span><br/> |
| <span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span><dl> <span data-ttu-id="8e40f-123"><dt>**SC \_ \_ \_ Modification**</dt> de l’état de l’événement <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8e40f-123"><dt>**SC\_EVENT\_STATUS\_CHANGE**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="8e40f-124">L’état d’un service a changé.</span><span class="sxs-lookup"><span data-stu-id="8e40f-124">The status of a service has changed.</span></span> <span data-ttu-id="8e40f-125">Le paramètre *hService* doit être un handle vers le service.</span><span class="sxs-lookup"><span data-stu-id="8e40f-125">The *hService* parameter must be a handle to the service.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="8e40f-126">*pCallback* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e40f-126">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e40f-127">Spécifie la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="8e40f-127">Specifies the callback function.</span></span> <span data-ttu-id="8e40f-128">Le rappel doit être défini comme ayant un type de **\_ \_ rappel de notification SC**.</span><span class="sxs-lookup"><span data-stu-id="8e40f-128">The callback must be defined as having a type of **SC\_NOTIFICATION\_CALLBACK**.</span></span> <span data-ttu-id="8e40f-129">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="8e40f-129">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8e40f-130">*pCallbackContext* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="8e40f-130">*pCallbackContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8e40f-131">Pointeur représentant le contexte de ce rappel de notification.</span><span class="sxs-lookup"><span data-stu-id="8e40f-131">A pointer representing the context for this notification callback.</span></span>

</dd> <dt>

<span data-ttu-id="8e40f-132">*pSubscription* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8e40f-132">*pSubscription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e40f-133">Retourne un pointeur vers l’abonnement résultant de l’inscription du rappel de notification.</span><span class="sxs-lookup"><span data-stu-id="8e40f-133">Returns a pointer to the subscription resulting from the notification callback registration.</span></span> <span data-ttu-id="8e40f-134">L’appelant est chargé d’appeler [**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) pour cesser de recevoir des notifications.</span><span class="sxs-lookup"><span data-stu-id="8e40f-134">The caller is responsible for calling [**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) to stop receiving notifications.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e40f-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8e40f-135">Return value</span></span>

<span data-ttu-id="8e40f-136">Si la fonction réussit, la valeur de retour est une **erreur de \_ réussite**.</span><span class="sxs-lookup"><span data-stu-id="8e40f-136">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="8e40f-137">Si la fonction échoue, la valeur de retour est l’un des [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8e40f-137">If the function fails, the return value is one of the [system error codes](/windows/desktop/Debug/system-error-codes).</span></span>

## <a name="remarks"></a><span data-ttu-id="8e40f-138">Notes</span><span class="sxs-lookup"><span data-stu-id="8e40f-138">Remarks</span></span>

<span data-ttu-id="8e40f-139">La fonction de rappel est déclarée comme suit :</span><span class="sxs-lookup"><span data-stu-id="8e40f-139">The callback function is declared as follows:</span></span>


```C++
typedef VOID CALLBACK SC_NOTIFICATION_CALLBACK(
    _In_    DWORD                   dwNotify,
    _In_    PVOID                   pCallbackContext
);
typedef SC_NOTIFICATION_CALLBACK* PSC_NOTIFICATION_CALLBACK;
```



<span data-ttu-id="8e40f-140">La fonction de rappel reçoit un pointeur vers le contexte fourni par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="8e40f-140">The callback function receives a pointer to the context provided by the caller.</span></span> <span data-ttu-id="8e40f-141">Le rappel est appelé à la suite de l’événement de modification de l’état du service.</span><span class="sxs-lookup"><span data-stu-id="8e40f-141">The callback is invoked as a result of the service status change event.</span></span> <span data-ttu-id="8e40f-142">Lorsque le rappel est appelé, il est fourni avec un masque de révocation de **service \_ notification \_ \* xxx**\* qui indique le type de modification de l’état du service.</span><span class="sxs-lookup"><span data-stu-id="8e40f-142">When the callback is invoked, it is provided with a bitmask of **SERVICE\_NOTIFY\_\*XXX**\* values that indicating the type of service status change.</span></span> <span data-ttu-id="8e40f-143">Lorsque le rappel est fourni avec zéro au lieu d’une valeur de **service \_ Notify \_ \* xxx**\* valide, l’application doit vérifier ce qui a été modifié.</span><span class="sxs-lookup"><span data-stu-id="8e40f-143">When the callback is provided with zero instead of a valid **SERVICE\_NOTIFY\_\*XXX**\* value, the application must verify what was changed.</span></span>

<span data-ttu-id="8e40f-144">La fonction de rappel ne doit pas bloquer l’exécution.</span><span class="sxs-lookup"><span data-stu-id="8e40f-144">The callback function must not block execution.</span></span> <span data-ttu-id="8e40f-145">Si vous vous attendez à ce que l’exécution de la fonction de rappel prenne du temps, déchargez le travail que vous effectuez dans la fonction de rappel vers un thread distinct en mettant en file d’attente un élément de travail vers un thread dans un pool de threads.</span><span class="sxs-lookup"><span data-stu-id="8e40f-145">If you expect the execution of the callback function to take time, offload the work that you perform in the callback function to a separate thread by queuing a work item to a thread in a thread pool.</span></span> <span data-ttu-id="8e40f-146">Certains types de travail qui peuvent rendre la fonction de rappel prend du temps incluent l’exécution d’e/s de fichier, l’attente d’un événement et l’exécution d’appels de procédure distante externes.</span><span class="sxs-lookup"><span data-stu-id="8e40f-146">Some types of work that can make the callback function take time include performing file I/O, waiting on an event, and making external remote procedure calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e40f-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e40f-147">Requirements</span></span>



| <span data-ttu-id="8e40f-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e40f-148">Requirement</span></span> | <span data-ttu-id="8e40f-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e40f-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e40f-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e40f-150">Minimum supported client</span></span><br/> | <span data-ttu-id="8e40f-151">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e40f-151">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8e40f-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e40f-152">Minimum supported server</span></span><br/> | <span data-ttu-id="8e40f-153">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e40f-153">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8e40f-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e40f-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e40f-155"><dt>Winsvcp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e40f-155"><dt>Winsvcp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8e40f-156">DLL</span><span class="sxs-lookup"><span data-stu-id="8e40f-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e40f-157"><dt>SecHost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e40f-157"><dt>SecHost.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e40f-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e40f-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e40f-159">**CreateService**</span><span class="sxs-lookup"><span data-stu-id="8e40f-159">**CreateService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[<span data-ttu-id="8e40f-160">**OpenService**</span><span class="sxs-lookup"><span data-stu-id="8e40f-160">**OpenService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[<span data-ttu-id="8e40f-161">**OpenSCManager**</span><span class="sxs-lookup"><span data-stu-id="8e40f-161">**OpenSCManager**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[<span data-ttu-id="8e40f-162">**UnsubscribeServiceChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="8e40f-162">**UnsubscribeServiceChangeNotifications**</span></span>](unsubscribeservicechangenotifications.md)
</dt> <dt>

[<span data-ttu-id="8e40f-163">**QueryServiceDynamicInformation**</span><span class="sxs-lookup"><span data-stu-id="8e40f-163">**QueryServiceDynamicInformation**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

