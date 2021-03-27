---
description: Une fois que vous avez commencé une session de suivi d’événements, vous pouvez utiliser TraceSetInformation pour indiquer au système de retourner des données de suivi d’événements supplémentaires.
ms.assetid: 65CCD658-869E-40C4-83AE-34CC2720B7CB
title: Récupération de données de suivi d’événements supplémentaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef864de40b924e0210603646d5ba5430d5d9b643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951369"
---
# <a name="retrieving-additional-event-tracing-data"></a><span data-ttu-id="3e154-103">Récupération de données de suivi d’événements supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3e154-103">Retrieving Additional Event Tracing Data</span></span>

<span data-ttu-id="3e154-104">Une fois que vous avez commencé une session de suivi d’événements, vous pouvez utiliser [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) pour indiquer au système de retourner des données de suivi d’événements supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="3e154-104">Once you have begun an event tracing session, you can use [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) to instruct the system to return additional event tracing data.</span></span> <span data-ttu-id="3e154-105">Les informations supplémentaires seront placées dans la section données étendues du suivi d’événements approprié.</span><span class="sxs-lookup"><span data-stu-id="3e154-105">The additional information will be placed in the extended data section of the relevant event trace.</span></span>

<span data-ttu-id="3e154-106">La procédure suivante décrit comment utiliser la fonction [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) pour récupérer des données supplémentaires à partir d’une session de suivi d’événements.</span><span class="sxs-lookup"><span data-stu-id="3e154-106">The following procedure describes how to use the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function to retrieve additional data from an event tracing session.</span></span>

<span data-ttu-id="3e154-107">**Pour récupérer des données de suivi d’événements supplémentaires**</span><span class="sxs-lookup"><span data-stu-id="3e154-107">**To retrieve additional event tracing data**</span></span>

1.  <span data-ttu-id="3e154-108">Démarrez votre session avec un appel à [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea).</span><span class="sxs-lookup"><span data-stu-id="3e154-108">Start your session with a call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea).</span></span>

    <span data-ttu-id="3e154-109">Pour plus d’informations, consultez [configuration et démarrage d’une session de suivi d’événements](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="3e154-109">For more information, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

2.  <span data-ttu-id="3e154-110">Appelez [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) pour définir des données de suivi d’événements supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="3e154-110">Call [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) to set additional event tracing data.</span></span>

    <span data-ttu-id="3e154-111">Utilisez l’énumération de [**\_ \_ classe d’informations d’événement**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) dans le paramètre *ClassInformation* pour décrire les informations supplémentaires que vous souhaitez récupérer.</span><span class="sxs-lookup"><span data-stu-id="3e154-111">use the [**EVENT\_INFO\_CLASS**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) enumeration in the *ClassInformation* parameter to describe the additional information you wish to retrieve.</span></span> <span data-ttu-id="3e154-112">L’exemple suivant décrit comment appeler [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), à l’aide du handle de session retourné à partir de l’appel à [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), et la valeur **TraceProviderBinaryTracking** de la **classe d' \_ informations \_ d’événement**.</span><span class="sxs-lookup"><span data-stu-id="3e154-112">The following example describes how to call [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), using the session handle returned from the call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), and the **TraceProviderBinaryTracking** value from **EVENT\_INFO\_CLASS**.</span></span>

    ```C++
    BOOLEAN enabled = TRUE;
    Win32Error error = TraceSetInformation(
        m_sessionHandle,
        TraceProviderBinaryTracking,
        &enabled,
        sizeof(enabled));
    ```

    

3.  <span data-ttu-id="3e154-113">Vous pouvez également utiliser [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) pour récupérer des informations sur les paramètres actuels de la session de suivi d’événements.</span><span class="sxs-lookup"><span data-stu-id="3e154-113">Alternately, you can use [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) to retrieve information about the current event tracing session settings.</span></span>

    <span data-ttu-id="3e154-114">Comme [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) utilise l’énumération de [**\_ \_ classe d’informations d’événement**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) pour décrire les informations à récupérer à partir du système.</span><span class="sxs-lookup"><span data-stu-id="3e154-114">Like [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) uses the [**EVENT\_INFO\_CLASS**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) enumeration to describe what information to retrieve from the system.</span></span>

 

 
