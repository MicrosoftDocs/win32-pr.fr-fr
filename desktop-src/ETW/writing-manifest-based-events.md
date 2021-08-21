---
description: En savoir plus sur l’écriture d’événements basés sur un manifeste dans une session de suivi. Commencez par inscrire votre fournisseur, afin qu’il soit prêt à écrire des événements dans une session de trace.
ms.assetid: 76e7202e-74ce-40a3-a04b-9af5117fe20e
title: Écriture d’événements basés sur un manifeste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6963051f65beb652eda04e3d0be6db99925e4eed81032c5687850915a0f1c173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151078"
---
# <a name="writing-manifest-based-events"></a>Écriture d’événements basés sur un manifeste

Avant de pouvoir écrire des événements dans une session de trace, vous devez inscrire votre fournisseur. L’inscription d’un fournisseur indique à ETW que votre fournisseur est prêt à écrire des événements dans une session de suivi. Un processus peut inscrire jusqu’à 1 024 GUID de fournisseur ; Toutefois, vous devez limiter le nombre de fournisseurs que votre processus inscrit à un ou deux.

**avant Windows Vista :** Il n’existe aucune limite au nombre de fournisseurs qu’un processus peut inscrire.

Pour inscrire un fournisseur basé sur un manifeste, appelez la fonction [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) . La fonction enregistre le GUID du fournisseur et identifie un rappel facultatif que ETW appelle lorsqu’un contrôleur active ou désactive le fournisseur.

Avant de quitter le fournisseur, appelez la fonction [**EventUnregister**](/windows/desktop/api/Evntprov/nf-evntprov-eventunregister) pour supprimer l’inscription du fournisseur dans ETW. La fonction [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) retourne le handle d’inscription que vous transmettez à la fonction **EventUnregister** .

Les fournisseurs [basés sur un manifeste](about-event-tracing.md) n’ont pas besoin d’implémenter une fonction [**EnableCallback**](/windows/desktop/api/Evntprov/nc-evntprov-penablecallback) pour recevoir des notifications lorsqu’une session active ou désactive le fournisseur. Le rappel est facultatif et utilisé à des fins d’information ; vous n’avez pas besoin de spécifier ou d’implémenter le rappel lors de l’inscription du fournisseur. Un fournisseur basé sur un manifeste peut simplement écrire des événements et ETW décidera si l’événement est enregistré dans une session de trace. Si un événement exige que vous effectuiez un travail extensif pour générer les données de l’événement, vous pouvez appeler la fonction [**EventEnabled**](/windows/desktop/api/Evntprov/nf-evntprov-eventenabled) ou [**EventProviderEnabled**](/windows/desktop/api/Evntprov/nf-evntprov-eventproviderenabled) pour vérifier que l’événement est écrit dans une session avant d’effectuer le travail.

En général, vous implémentez le rappel si votre fournisseur exige que les données de filtre définies par le fournisseur passent (voir le paramètre *FilterData* de [**EnableCallback**](/windows/desktop/api/Evntprov/nc-evntprov-penablecallback)) au fournisseur, ou que le fournisseur utilise les informations de contexte qu’il a spécifiées quand il s’est inscrit lui-même (voir le paramètre *CallbackContext* de [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister)).

Les fournisseurs [basés sur un manifeste](about-event-tracing.md) appellent la fonction [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) ou [**EventWriteString**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritestring) pour écrire des événements dans une session. Si vos données d’événement sont une chaîne, ou si vous ne définissez pas de manifeste pour votre fournisseur et que vos données d’événement sont une chaîne unique, appelez la fonction [**EventWriteString**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritestring) pour écrire l’événement. Pour les données d’événement qui contiennent des types de données numériques ou complexes, appelez la fonction [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) pour enregistrer l’événement.

L’exemple suivant montre comment préparer les données d’événement à écrire à l’aide de la fonction [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) . L’exemple fait référence aux événements définis dans la [publication de votre schéma d’événement pour un fournisseur basé sur un manifeste](publishing-your-event-schema-for-a-manifest-base-provider.md).


```C++
#include <windows.h>
#include <stdio.h>
#include <evntprov.h>
#include "provider.h"  // Generated from manifest

#define SUNDAY     0X1
#define MONDAY     0X2
#define TUESDAY    0X4
#define WEDNESDAY  0X8
#define THURSDAY   0X10
#define FRIDAY     0X20
#define SATURDAY   0X40

enum TRANSFER_TYPE {
  Download = 1,
  Upload,
  UploadReply
};

#define MAX_NAMEDVALUES          5  // Maximum array size
#define MAX_PAYLOAD_DESCRIPTORS  9 + (2 * MAX_NAMEDVALUES)

typedef struct _namedvalue {
  LPWSTR name;
  USHORT value;
} NAMEDVALUE, *PNAMEDVALUE;

void wmain(void)
{
    DWORD status = ERROR_SUCCESS;
    REGHANDLE RegistrationHandle = NULL; 
    EVENT_DATA_DESCRIPTOR Descriptors[MAX_PAYLOAD_DESCRIPTORS]; 
    DWORD i = 0;

    // Data to load into event descriptors

    USHORT Scores[3] = {45, 63, 21};
    ULONG pImage = (ULONG)&Scores;
    DWORD TransferType = Upload;
    DWORD Day = MONDAY | TUESDAY;
    LPWSTR Path = L"c:\\path\\folder\\file.ext";
    BYTE Cert[11] = {0x2, 0x4, 0x8, 0x10, 0x20, 0x30, 0x40, 0x50, 0x60, 0x0, 0x1};
    PBYTE Guid = (PBYTE) &ProviderGuid;
    USHORT ArraySize = MAX_NAMEDVALUES;
    BOOL IsLocal = TRUE;
    NAMEDVALUE NamedValues[MAX_NAMEDVALUES] = { 
        {L"Bill", 1},
        {L"Bob", 2},
        {L"William", 3},
        {L"Robert", 4},
        {L"", 5}
        };

    status = EventRegister(
        &ProviderGuid,      // GUID that identifies the provider
        NULL,               // Callback not used
        NULL,               // Context noot used
        &RegistrationHandle // Used when calling EventWrite and EventUnregister
        );

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"EventRegister failed with %lu\n", status);
        goto cleanup;
    }
  
    // Load the array of data descriptors for the TransferEvent event. 
    // Add the data to the array in the order of the <data> elements
    // defined in the event's template. 
   
    EventDataDescCreate(&Descriptors[i++], &pImage, sizeof(ULONG));
    EventDataDescCreate(&Descriptors[i++], Scores, sizeof(Scores));
    EventDataDescCreate(&Descriptors[i++], Guid, sizeof(GUID));
    EventDataDescCreate(&Descriptors[i++], Cert, sizeof(Cert));
    EventDataDescCreate(&Descriptors[i++], &IsLocal, sizeof(BOOL));
    EventDataDescCreate(&Descriptors[i++], Path, (ULONG)(wcslen(Path) + 1) * sizeof(WCHAR));
    EventDataDescCreate(&Descriptors[i++], &ArraySize, sizeof(USHORT));

    // If your event contains a structure, you should write each member
    // of the structure separately. If the structure contained integral data types
    // such as DWORDs and the data types were aligned on an 8-byte boundary, you 
    // could use the following call to write the structure, however, you are 
    // encouraged to write the members separately.
    //
    // EventDataDescCreate(&EvtData, struct, sizeof(struct));
    //
    // Because the array of structures in this example contains both strings 
    // and numbers, you must write each member of the structure separately.

    for (int j = 0; j < MAX_NAMEDVALUES; j++)
    {
        EventDataDescCreate(&Descriptors[i++], NamedValues[j].name, (ULONG)(wcslen(NamedValues[j].name)+1) * sizeof(WCHAR) );
        EventDataDescCreate(&Descriptors[i++], &(NamedValues[j].value), sizeof(USHORT) );
    }

    EventDataDescCreate(&Descriptors[i++], &Day, sizeof(DWORD));
    EventDataDescCreate(&Descriptors[i++], &TransferType, sizeof(DWORD));

    // Write the event. You do not have to verify if your provider is enabled before
    // writing the event. ETW will write the event to any session that enabled
    // the provider. If no session enabled the provider, the event is not 
    // written. If you need to perform extra work to write an event that you
    // would not otherwise do, you may want to call the EventEnabled function
    // before performing the extra work. The EventEnabled function tells you if a
    // session has enabled your provider, so you know if you need to perform the 
    // extra work or not.

    status = EventWrite(
        RegistrationHandle,              // From EventRegister
        &TransferEvent,                  // EVENT_DESCRIPTOR generated from the manifest
        (ULONG)MAX_PAYLOAD_DESCRIPTORS,  // Size of the array of EVENT_DATA_DESCRIPTORs
        &Descriptors[0]                  // Array of descriptors that contain the event data
        );

    if (status != ERROR_SUCCESS) 
    {
        wprintf(L"EventWrite failed with 0x%x", status);
    }

cleanup:

    EventUnregister(RegistrationHandle);
}
```



Quand vous compilez le manifeste (voir [compilation d’un manifeste d’instrumentation](../wes/compiling-an-instrumentation-manifest.md)) utilisé par l’exemple ci-dessus, il crée le fichier d’en-tête suivant (référencé dans l’exemple ci-dessus).


```C++
//**********************************************************************`
//* This is an include file generated by Message Compiler.             *`
//*                                                                    *`
//* Copyright (c) Microsoft Corporation. All Rights Reserved.          *`
//**********************************************************************`
#pragma once
//+
// Provider Microsoft-Windows-ETWProvider Event Count 1
//+
EXTERN_C __declspec(selectany) const GUID ProviderGuid = {0xd8909c24, 0x5be9, 0x4502, {0x98, 0xca, 0xab, 0x7b, 0xdc, 0x24, 0x89, 0x9d}};
//
// Keyword
//
#define READ_KEYWORD 0x1
#define WRITE_KEYWORD 0x2
#define LOCAL_KEYWORD 0x4
#define REMOTE_KEYWORD 0x8

//
// Event Descriptors
//
EXTERN_C __declspec(selectany) const EVENT_DESCRIPTOR TransferEvent = {0x1, 0x0, 0x0, 0x4, 0x0, 0x0, 0x5};
#define TransferEvent_value 0x1
#define MSG_Provider_Name                    0x90000001L
#define MSG_Event_WhenToTransfer             0xB0000001L
#define MSG_Map_Download                     0xD0000001L
#define MSG_Map_Upload                       0xD0000002L
#define MSG_Map_UploadReply                  0xD0000003L
#define MSG_Map_Sunday                       0xF0000001L
#define MSG_Map_Monday                       0xF0000002L
#define MSG_Map_Tuesday                      0xF0000003L
#define MSG_Map_Wednesday                    0xF0000004L
#define MSG_Map_Thursday                     0xF0000005L
#define MSG_Map_Friday                       0xF0000006L
#define MSG_Map_Saturday                     0xF0000007L
```



 

 
