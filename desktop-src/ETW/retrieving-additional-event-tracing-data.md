---
description: Une fois que vous avez commencé une session de suivi d’événements, vous pouvez utiliser TraceSetInformation pour indiquer au système de retourner des données de suivi d’événements supplémentaires.
ms.assetid: 65CCD658-869E-40C4-83AE-34CC2720B7CB
title: Récupération de données de suivi d’événements supplémentaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbae65e516a63154fb76d3d558e02e9533e58e119e977f851c2404f0a218ec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393897"
---
# <a name="retrieving-additional-event-tracing-data"></a>Récupération de données de suivi d’événements supplémentaires

Une fois que vous avez commencé une session de suivi d’événements, vous pouvez utiliser [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) pour indiquer au système de retourner des données de suivi d’événements supplémentaires. Les informations supplémentaires seront placées dans la section données étendues du suivi d’événements approprié.

La procédure suivante décrit comment utiliser la fonction [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) pour récupérer des données supplémentaires à partir d’une session de suivi d’événements.

**Pour récupérer des données de suivi d’événements supplémentaires**

1.  Démarrez votre session avec un appel à [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea).

    Pour plus d’informations, consultez [configuration et démarrage d’une session de suivi d’événements](configuring-and-starting-an-event-tracing-session.md).

2.  Appelez [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) pour définir des données de suivi d’événements supplémentaires.

    Utilisez l’énumération de [**\_ \_ classe d’informations d’événement**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) dans le paramètre *ClassInformation* pour décrire les informations supplémentaires que vous souhaitez récupérer. L’exemple suivant décrit comment appeler [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), à l’aide du handle de session retourné à partir de l’appel à [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), et la valeur **TraceProviderBinaryTracking** de la **classe d' \_ informations \_ d’événement**.

    ```C++
    BOOLEAN enabled = TRUE;
    Win32Error error = TraceSetInformation(
        m_sessionHandle,
        TraceProviderBinaryTracking,
        &enabled,
        sizeof(enabled));
    ```

    

3.  Vous pouvez également utiliser [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) pour récupérer des informations sur les paramètres actuels de la session de suivi d’événements.

    Comme [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) utilise l’énumération de [**\_ \_ classe d’informations d’événement**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) pour décrire les informations à récupérer à partir du système.

 

 
