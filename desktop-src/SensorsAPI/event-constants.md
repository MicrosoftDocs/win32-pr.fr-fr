---
description: La plate-forme capteur et emplacement Windows définit des constantes pour les événements de pilote. Les manfuactureres de capteur peuvent également définir leurs propres constantes.
ms.assetid: ca61c912-bce5-4e41-ab48-40615d5b93ba
title: Constantes d’événement (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9fb3ced92c1fe263538f2ce27c3fc65fdd7676
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544292"
---
# <a name="event-constants-sensorsh"></a><span data-ttu-id="ab033-104">Constantes d’événement (sensors. h)</span><span class="sxs-lookup"><span data-stu-id="ab033-104">Event Constants (Sensors.h)</span></span>

<span data-ttu-id="ab033-105">La plate-forme capteur et emplacement Windows définit des constantes pour les événements de pilote.</span><span class="sxs-lookup"><span data-stu-id="ab033-105">The Windows Sensor and Location platform defines constants for driver events.</span></span> <span data-ttu-id="ab033-106">Les manfuactureres de capteur peuvent également définir leurs propres constantes.</span><span class="sxs-lookup"><span data-stu-id="ab033-106">Sensor manfuactureres can also define their own constants.</span></span>

<span data-ttu-id="ab033-107">**Types d’événements de capteur**</span><span class="sxs-lookup"><span data-stu-id="ab033-107">**Sensor Event Types**</span></span>

<span data-ttu-id="ab033-108">La plateforme définit les identificateurs de type d’événement de capteur suivants.</span><span class="sxs-lookup"><span data-stu-id="ab033-108">The platform defines the following sensor event type identifiers.</span></span>



| <span data-ttu-id="ab033-109">Type d’événement de capteur</span><span class="sxs-lookup"><span data-stu-id="ab033-109">Sensor event type</span></span>                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="ab033-110">Description</span><span class="sxs-lookup"><span data-stu-id="ab033-110">Description</span></span>                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_ACCELEROMETER_SHAKE"></span><span id="sensor_event_accelerometer_shake"></span><dl> <span data-ttu-id="ab033-111"><dt>**Capteur \_ ÉVÉNEMENT \_ accéléromètre \_ tremble**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt></span><span class="sxs-lookup"><span data-stu-id="ab033-111"><dt>**SENSOR\_EVENT\_ACCELEROMETER\_SHAKE**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt></span></span> </dl> | <span data-ttu-id="ab033-112">Indique que l’appareil a été agité.</span><span class="sxs-lookup"><span data-stu-id="ab033-112">Indicates that the device was shaken.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_DATA_UPDATED"></span><span id="sensor_event_data_updated"></span><dl> <span data-ttu-id="ab033-113"><dt>**Capteur \_ Données d’événement \_ \_ mises à jour**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt></span><span class="sxs-lookup"><span data-stu-id="ab033-113"><dt>**SENSOR\_EVENT\_DATA\_UPDATED**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt></span></span> </dl>                      | <span data-ttu-id="ab033-114">Indique que de nouvelles données sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="ab033-114">Indicates that new data is available.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_PROPERTY_CHANGED"></span><span id="sensor_event_property_changed"></span><dl> <span data-ttu-id="ab033-115"><dt>**Capteur \_ \_ \_ Modification**</dt> de la propriété d’événement <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt></span><span class="sxs-lookup"><span data-stu-id="ab033-115"><dt>**SENSOR\_EVENT\_PROPERTY\_CHANGED**</dt> <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt></span></span> </dl>          | <span data-ttu-id="ab033-116">Indique qu’une valeur de propriété a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="ab033-116">Indicates that a property value changed.</span></span> <span data-ttu-id="ab033-117">Vérifiez l’interface [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) , transmise via le paramètre *pEventData* à [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent), pour déterminer quelle propriété a changé et sa nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="ab033-117">Check the [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) interface, passed through the *pEventData* parameter to [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent), to determine which property changed and its new value.</span></span><br/> |
| <span id="SENSOR_EVENT_STATE_CHANGED"></span><span id="sensor_event_state_changed"></span><dl> <span data-ttu-id="ab033-118"><dt>**Capteur \_ État de l’événement \_ \_ modifié**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt></span><span class="sxs-lookup"><span data-stu-id="ab033-118"><dt>**SENSOR\_EVENT\_STATE\_CHANGED**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt></span></span> </dl>                   | <span data-ttu-id="ab033-119">Indique une modification de l’état opérationnel, par exemple, de \_ l’état du capteur \_ initialisé à l’état de capteur \_ \_ Ready.</span><span class="sxs-lookup"><span data-stu-id="ab033-119">Indicates a change of operational state, for example, from SENSOR\_STATE\_INITIALIZING to SENSOR\_STATE\_READY.</span></span><br/>                                                                                                                                                                                            |



<span data-ttu-id="ab033-120">**Événement de capteur PROPERTYKEYs**</span><span class="sxs-lookup"><span data-stu-id="ab033-120">**Sensor Event PROPERTYKEYs**</span></span>

<span data-ttu-id="ab033-121">Les clés de propriété définies par la plateforme pour les événements sont basées sur le GUID suivant :</span><span class="sxs-lookup"><span data-stu-id="ab033-121">Platform-defined property keys for events are based on the following GUID:</span></span>

<span data-ttu-id="ab033-122">{64346E30-8728-4B34-BDF6-4F52442C5C28}</span><span class="sxs-lookup"><span data-stu-id="ab033-122">{64346E30-8728-4B34-BDF6-4F52442C5C28}</span></span>

<span data-ttu-id="ab033-123">La plateforme de capteur définit les **PROPERTYKEY** s suivantes qui identifient les paramètres d’événement de capteur.</span><span class="sxs-lookup"><span data-stu-id="ab033-123">The sensor platform defines the following **PROPERTYKEY** s that identify sensor event parameters.</span></span>



| <span data-ttu-id="ab033-124">Événement de capteur PROPERTYKEY et PID</span><span class="sxs-lookup"><span data-stu-id="ab033-124">Sensor event PROPERTYKEY and PID</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="ab033-125">Description</span><span class="sxs-lookup"><span data-stu-id="ab033-125">Description</span></span>                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_PARAMETER_EVENT_ID"></span><span id="sensor_event_parameter_event_id"></span><dl> <span data-ttu-id="ab033-126"><dt>**Capteur \_ \_ID d' \_ événement \_ du paramètre d’événement**</dt> <dt>(PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="ab033-126"><dt>**SENSOR\_EVENT\_PARAMETER\_EVENT\_ID**</dt> <dt>(PID = 2)</dt></span></span> </dl> | <span data-ttu-id="ab033-127">Indique que la valeur **GUID** dans [IPORTABLEDEVICEVALUES](/previous-versions//ms740012(v=vs.85)) est un ID de type d’événement, comme les données d’événement de capteur \_ \_ \_ mises à jour.</span><span class="sxs-lookup"><span data-stu-id="ab033-127">Indicates that the **GUID** value in [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) is an event type ID, such as SENSOR\_EVENT\_DATA\_UPDATED.</span></span><br/> |
| <span id="SENSOR_EVENT_PARAMETER_STATE"></span><span id="sensor_event_parameter_state"></span><dl> <span data-ttu-id="ab033-128"><dt>**Capteur \_ \_ \_ État du paramètre d’événement**</dt> <dt>(PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="ab033-128"><dt>**SENSOR\_EVENT\_PARAMETER\_STATE**</dt> <dt>(PID = 3)</dt></span></span> </dl>           | <span data-ttu-id="ab033-129">Indique que la valeur de l’entier non signé dans **IPortableDeviceValues** est un état de capteur, par exemple l’état du capteur \_ \_ Ready.</span><span class="sxs-lookup"><span data-stu-id="ab033-129">Indicates that the unsigned integer value in **IPortableDeviceValues** is a sensor state, such as SENSOR\_STATE\_READY.</span></span><br/>                                                  |



<span data-ttu-id="ab033-130">**Erreur de capteur PROPERTYKEYs**</span><span class="sxs-lookup"><span data-stu-id="ab033-130">**Sensor Error PROPERTYKEYs**</span></span>

<span data-ttu-id="ab033-131">Les clés de propriété définies par la plateforme pour les erreurs seront basées sur le GUID suivant :</span><span class="sxs-lookup"><span data-stu-id="ab033-131">Platform-defined property keys for errors will be based on the following GUID:</span></span>

<span data-ttu-id="ab033-132">{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}</span><span class="sxs-lookup"><span data-stu-id="ab033-132">{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}</span></span>

<span data-ttu-id="ab033-133">La plateforme de capteur réserve ce GUID pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ab033-133">The sensor platform reserves this GUID for future use.</span></span>

<dl></dl>

## <a name="requirements"></a><span data-ttu-id="ab033-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab033-134">Requirements</span></span>



| <span data-ttu-id="ab033-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab033-135">Requirement</span></span> | <span data-ttu-id="ab033-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab033-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ab033-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab033-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ab033-138">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab033-138">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ab033-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab033-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ab033-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab033-140">None supported</span></span><br/>                                                            |
| <span data-ttu-id="ab033-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab033-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab033-142"><dt>Capteurs. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab033-142"><dt>Sensors.h</dt></span></span> </dl> |



 

