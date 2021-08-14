---
title: Ajout d’une source d’événement à un abonnement initié par le collecteur
description: Pour recevoir un événement transféré d’un abonnement aux événements, vous pouvez créer un abonnement initié par le collecteur sur l’ordinateur local.
ms.assetid: f0100938-1702-4ef7-b20e-a0e8df224d18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905dd9b5a250f9ab12397f851f79a8374c6847235acb34013972dea445f3622b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344210"
---
# <a name="adding-an-event-source-to-a-collector-initiated-subscription"></a>Ajout d’une source d’événement à un abonnement initié par le collecteur

Pour recevoir un événement transféré d’un abonnement aux événements, vous pouvez créer un abonnement initié par le collecteur sur l’ordinateur local. Pour plus d’informations sur la création d’un abonnement initié par le collecteur, consultez l’exemple de code C++ présenté dans [création d’un abonnement à un collecteur d’événements](creating-an-event-collector-subscription.md).

Après avoir créé un abonnement initié par le collecteur, vous pouvez ajouter des sources d’événements à l’abonnement. Vous devez ajouter au moins une source d’événement à un abonnement pour collecter des événements.

> [!Note]
>
> Vous pouvez utiliser cet exemple de code pour ajouter une source d’événement à un abonnement, ou vous pouvez taper la commande suivante à l’invite de commandes :
>
> **wecutil SS** *SubscriptionName* **/ESA :**_EventSourceAddress_ **/AES/ESE**
>
> *EventSourceAddress* peut être localhost pour l’ordinateur local ou un nom de domaine complet pour un ordinateur distant.

 

Pour plus d’informations sur l’ajout de sources d’événements à un abonnement initié par la source, consultez [configuration d’un abonnement initié par la source](setting-up-a-source-initiated-subscription.md).

Cet exemple suit une série d’étapes pour ajouter une source d’événement à un abonnement initié par le collecteur.

**Pour ajouter une source d’événement à un abonnement initié par le collecteur**

1.  Ouvrez l’abonnement existant en fournissant le nom de l’abonnement et les droits d’accès en tant que paramètres à la fonction [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) . pour plus d’informations sur les droits d’accès, consultez [**Windows des constantes du collecteur d’événements**](windows-event-collector-constants.md).
2.  Récupérez le tableau des sources d’événements de l’abonnement en appelant la fonction [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) . Pour plus d’informations sur les propriétés d’abonnement qui peuvent être récupérées, consultez l’énumération de l' [**\_ ID de \_ propriété \_ d’abonnement EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) .
3.  Ajoutez une nouvelle source d’événement au tableau des sources d’événements de l’abonnement en appelant la fonction [**EcInsertObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement) .
4.  Définissez les propriétés de la source d’événements en appelant la fonction [**EcSetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty) . La propriété **EcSubscriptionEventSourceAddress** est définie sur une adresse pour l’ordinateur local (localhost) ou sur un nom de domaine complet pour un ordinateur distant. Pour plus d’informations sur les propriétés de la source d’événements qui peuvent être définies, consultez l’énumération de l' **\_ ID de \_ propriété \_ d’abonnement EC** .
5.  Enregistrez l’abonnement en appelant la fonction [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) .
6.  Fermez l’abonnement en appelant la fonction [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) .

L’exemple de code C++ suivant montre comment ajouter une source d’événement à un abonnement initié par le collecteur :


```C++
#include <windows.h>
#include <iostream>
using namespace std;
#include <EvColl.h>
#include <vector>
#include <string>
#include <strsafe.h>

#pragma comment(lib, "wecapi.lib")

DWORD GetProperty(EC_HANDLE hSubscription,  
                  EC_SUBSCRIPTION_PROPERTY_ID propID, 
                  DWORD flags, 
                  std::vector<BYTE>& buffer, 
                  PEC_VARIANT& vProperty);

void __cdecl wmain()
{
    EC_HANDLE hSubscription;
    std::wstring eventSource = L"localhost"; 
    BOOL status = true;
    std::wstring eventSourceUserName;
    std::wstring eventSourcePassword;
    LPCWSTR lpSubname = L"TestSubscription-CollectorInitiated";
    DWORD dwEventSourceCount;
    DWORD dwRetVal = ERROR_SUCCESS;
    PEC_VARIANT vEventSource = NULL;
    std::vector<BYTE> buffer;
    LPVOID lpwszBuffer;
    EC_VARIANT vProperty;

    // Create a handle to access the event sources array.
    EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray = NULL;

    // Step 1: Open an existing subscription.
    hSubscription = EcOpenSubscription( lpSubname,
        EC_READ_ACCESS | EC_WRITE_ACCESS, 
        EC_OPEN_EXISTING);
    if (!hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 2: Get the event sources array to add a new event 
    // source to the subscription.
    dwRetVal = GetProperty(hSubscription, 
        EcSubscriptionEventSources,
        0,
        buffer,
        vEventSource);
    if (ERROR_SUCCESS != dwRetVal)
    {
        goto Cleanup;
    }

    // Ensure that a handle to the event sources array has been obtained. 
    if (vEventSource->Type != EcVarTypeNull  && 
        vEventSource->Type != EcVarObjectArrayPropertyHandle)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    hArray = (vEventSource->Type == EcVarTypeNull)? NULL: 
        vEventSource->PropertyHandleVal;
    if(!hArray)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }
    if (!EcGetObjectArraySize(hArray, &dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 3: Add a new event source to the event source array.
    if (!EcInsertObjectArrayElement(hArray,
        dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 4: Set the properties of the event source
    // Set the EventSourceAddress property that specifies the address
    // of the event forwarding computer, this property can be localhost 
    // or a fully-qualified domain name.
    vProperty.Type = EcVarTypeString;
    vProperty.StringVal = eventSource.c_str();
    if (!EcSetObjectArrayProperty( hArray,
        EcSubscriptionEventSourceAddress,
        dwEventSourceCount,
        0,
        &vProperty))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Get the credentials.
    wcout << "Enter credentials used to connect to the event source " <<
        eventSource << ". " << endl <<
        "Enter user name: " << endl;
    wcin >> eventSourceUserName;
    cout << "Enter password: " << endl;

    wchar_t c;
    while( (c = _getwch()) && c != '\n' && c != '\r' && eventSourcePassword.length() < 512)
    {eventSourcePassword.append(1, c);}

    // Set the EventSourceUserName property that specifies the user
    // that can retrieve events from the event source.
    if (eventSourceUserName.length() > 0)
    {
        vProperty.Type = EcVarTypeString;
        vProperty.StringVal = eventSourceUserName.c_str();
        if (!EcSetObjectArrayProperty(hArray,
            EcSubscriptionEventSourceUserName,
            dwEventSourceCount,
            0,
            &vProperty))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the EventSourcePassword property that defines the password
        // for the previously-defined user.
        vProperty.StringVal = (eventSourcePassword.length() > 0) ? 
            eventSourcePassword.c_str() : L"";
        if (!EcSetObjectArrayProperty(hArray,
            EcSubscriptionEventSourcePassword, 
            dwEventSourceCount,
            0,
            &vProperty))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }
    }

    // When you have finished using the credentials,
    // erase them.
    eventSourceUserName.erase();
    eventSourcePassword.erase();


    // Set the EventSourceEnabled property that enables the event source
    // to forward events.
    vProperty.Type = EcVarTypeBoolean;
    vProperty.BooleanVal = status;
    if (!EcSetObjectArrayProperty(hArray,
        EcSubscriptionEventSourceEnabled,
        dwEventSourceCount,
        0,
        &vProperty))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 5: Save the subscription to enable the event source.
    if (!EcSaveSubscription(hSubscription, NULL))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 6: Close the subscription.
Cleanup:
    if (hArray)
        EcClose(hArray);
    if (hSubscription)
        EcClose(hSubscription);

    if (dwRetVal != ERROR_SUCCESS)
    {
        FormatMessageW( FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_SYSTEM,
            NULL,
            dwRetVal,
            0,
            (LPWSTR) &lpwszBuffer,
            0,
            NULL);
        if (!lpwszBuffer)
        {
            wprintf(L"Failed to FormatMessage.  Operation Error Code: %u\n  Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
            return;
        }
        wprintf(L"\nFailed to Perform Operation. Error Code: %u\n Error Message: %s\n", dwRetVal, lpwszBuffer);
        LocalFree(lpwszBuffer);
    }
}

DWORD GetProperty(EC_HANDLE hSubscription,
                  EC_SUBSCRIPTION_PROPERTY_ID propID,
                  DWORD flags,
                  std::vector<BYTE>& buffer,
                  PEC_VARIANT& vProperty)
{
    DWORD  dwBufferSize, dwRetVal = ERROR_SUCCESS;
    buffer.resize(sizeof(EC_VARIANT));

    if (!hSubscription)
        return ERROR_INVALID_PARAMETER;

    // Get the value for the specified property. 
    if (!EcGetSubscriptionProperty(hSubscription,
        propID,
        flags,
        (DWORD) buffer.size(), 
        (PEC_VARIANT)&buffer[0],
        &dwBufferSize))
    {
        dwRetVal = GetLastError();
        if (ERROR_INSUFFICIENT_BUFFER == dwRetVal)
        {
            dwRetVal = ERROR_SUCCESS;
            buffer.resize(dwBufferSize);

            if (!EcGetSubscriptionProperty(hSubscription,
                propID,
                flags,
                (DWORD) buffer.size(),
                (PEC_VARIANT)&buffer[0],
                &dwBufferSize) )
            {
                dwRetVal = GetLastError();
            }
        }
    }

    if (dwRetVal == ERROR_SUCCESS)
    {
        vProperty = (PEC_VARIANT) &buffer[0];
    }
    else
    {
        vProperty = NULL;
    }

    return dwRetVal;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configurer des ordinateurs pour transférer et collecter des événements](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))
</dt> <dt>

[Création d’un abonnement à un collecteur d’événements](creating-an-event-collector-subscription.md)
</dt> <dt>

[Windows Référence du collecteur d’événements](windows-event-collector-reference.md)
</dt> </dl>

 

 