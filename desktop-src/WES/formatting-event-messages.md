---
title: Mise en forme des messages d’événement
description: Un événement peut contenir des chaînes de message localisées que vous pouvez mettre en forme pour l’affichage.
ms.assetid: 31dd8276-1925-4a0e-9e2a-6966e8086238
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314742838e5a756787385930e5122117b3a012c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509588"
---
# <a name="formatting-event-messages"></a><span data-ttu-id="4d0b3-103">Mise en forme des messages d’événement</span><span class="sxs-lookup"><span data-stu-id="4d0b3-103">Formatting Event Messages</span></span>

<span data-ttu-id="4d0b3-104">Un événement peut contenir des chaînes de message localisées que vous pouvez mettre en forme pour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="4d0b3-104">An event can contain localized message strings that you can format for display.</span></span> <span data-ttu-id="4d0b3-105">Pour obtenir une chaîne de message de l’événement, appelez la fonction [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) .</span><span class="sxs-lookup"><span data-stu-id="4d0b3-105">To get a message string from the event, call the [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) function.</span></span> <span data-ttu-id="4d0b3-106">Un événement peut contenir les chaînes de message suivantes :</span><span class="sxs-lookup"><span data-stu-id="4d0b3-106">An event can contain the following message strings:</span></span>

-   <span data-ttu-id="4d0b3-107">Chaîne de message pour l’événement lui-même.</span><span class="sxs-lookup"><span data-stu-id="4d0b3-107">A message string for the event itself.</span></span>
-   <span data-ttu-id="4d0b3-108">Chaîne de message qui décrit la valeur de niveau assignée à l’événement.</span><span class="sxs-lookup"><span data-stu-id="4d0b3-108">A message string that describes the level value assigned to the event.</span></span>
-   <span data-ttu-id="4d0b3-109">Chaîne de message qui décrit la valeur de tâche assignée à l’événement.</span><span class="sxs-lookup"><span data-stu-id="4d0b3-109">A message string that describes the task value assigned to the event.</span></span>
-   <span data-ttu-id="4d0b3-110">Chaîne de message qui décrit la valeur de l’opcode assignée à l’événement.</span><span class="sxs-lookup"><span data-stu-id="4d0b3-110">A message string that describes the opcode value assigned to the event.</span></span>
-   <span data-ttu-id="4d0b3-111">Chaîne de message qui décrit les valeurs de mot clé assignées à l’événement.</span><span class="sxs-lookup"><span data-stu-id="4d0b3-111">A message string that describes the keyword values assigned to the event.</span></span>
-   <span data-ttu-id="4d0b3-112">Chaîne de message qui décrit la valeur de canal assignée à l’événement.</span><span class="sxs-lookup"><span data-stu-id="4d0b3-112">A message string that describes the channel value assigned to the event.</span></span>

<span data-ttu-id="4d0b3-113">Vous pouvez également utiliser [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) pour obtenir la chaîne de message pour le fournisseur ou une chaîne XML qui contient l’événement et toutes les chaînes de message.</span><span class="sxs-lookup"><span data-stu-id="4d0b3-113">You can also use [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) to get the message string for the provider or an XML string that contains the event and all the message strings.</span></span>

<span data-ttu-id="4d0b3-114">Outre l’obtention des chaînes de message à partir des événements que vous interrogez, vous pouvez également obtenir les chaînes de message à partir des métadonnées du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4d0b3-114">In addition to getting the message strings from the events that you query, you can also get the message strings from the provider's metadata.</span></span> <span data-ttu-id="4d0b3-115">Pour plus d’informations sur la mise en forme d’un message basé sur un identificateur de message que vous obtenez à partir des métadonnées du fournisseur, consultez [obtention des métadonnées d’un fournisseur](getting-a-provider-s-metadata-.md).</span><span class="sxs-lookup"><span data-stu-id="4d0b3-115">For details on formatting a message based on a message identifier that you get from the provider's metadata, see [Getting a Provider's Metadata](getting-a-provider-s-metadata-.md).</span></span>

<span data-ttu-id="4d0b3-116">L’exemple suivant montre comment récupérer les chaînes de message d’un événement.</span><span class="sxs-lookup"><span data-stu-id="4d0b3-116">The following example shows how to get the message strings from an event.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <sddl.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

LPWSTR GetMessageString(EVT_HANDLE hMetadata, EVT_HANDLE hEvent, EVT_FORMAT_MESSAGE_FLAGS FormatId);

void main(void)
{
    EVT_HANDLE hProviderMetadata = NULL;
    EVT_HANDLE hResults = NULL;
    EVT_HANDLE hEvent = NULL;
    DWORD status = ERROR_SUCCESS;
    DWORD dwReturned = 0;
    LPWSTR pwsMessage = NULL;
    LPWSTR pwsPath = L"<name of the channel goes here>";
    LPWSTR pwsQuery = L"<xpath query goes here>";
    LPWSTR pwszPublisherName = L"<name of the publisher goes here>";

    // Get the handle to the provider's metadata that contains the message strings.
    hProviderMetadata = EvtOpenPublisherMetadata(NULL, pwszPublisherName, NULL, 0, 0);
    if (NULL == hProviderMetadata)
    {
        wprintf(L"EvtOpenPublisherMetadata failed with %d\n", GetLastError());
        goto cleanup;
    }

    // Query for an event.
    hResults = EvtQuery(NULL, pwsPath, pwsQuery, EvtQueryChannelPath);
    if (NULL == hResults)
    {
        status = GetLastError();

        if (ERROR_EVT_CHANNEL_NOT_FOUND == status)
            wprintf(L"Channel %s was not found.\n", pwsPath);
        else
            wprintf(L"EvtQuery failed with %lu.\n", status);

        goto cleanup;
    }

    // Get a single event from the result set.
    if (!EvtNext(hResults, 1, &hEvent, INFINITE, 0, &dwReturned))
    {
        wprintf(L"EvtNext failed with %lu\n", status);
        goto cleanup;
    }

    // Get the various message strings from the event.
    pwsMessage = GetMessageString(hProviderMetadata, hEvent, EvtFormatMessageEvent);
    if (pwsMessage)
    {
        wprintf(L"Event message string: %s\n\n", pwsMessage);
        free(pwsMessage);
        pwsMessage = NULL;
    }

    pwsMessage = GetMessageString(hProviderMetadata, hEvent, EvtFormatMessageLevel);
    if (pwsMessage)
    {
        wprintf(L"Level message string: %s\n\n", pwsMessage);
        free(pwsMessage);
        pwsMessage = NULL;
    }

    pwsMessage = GetMessageString(hProviderMetadata, hEvent, EvtFormatMessageTask);
    if (pwsMessage)
    {
        wprintf(L"Task message string: %s\n\n", pwsMessage);
        free(pwsMessage);
        pwsMessage = NULL;
    }

    pwsMessage = GetMessageString(hProviderMetadata, hEvent, EvtFormatMessageOpcode);
    if (pwsMessage)
    {
        wprintf(L"Opcode message string: %s\n\n", pwsMessage);
        free(pwsMessage);
        pwsMessage = NULL;
    }

    pwsMessage = GetMessageString(hProviderMetadata, hEvent, EvtFormatMessageKeyword);
    if (pwsMessage)
    {
        LPWSTR ptemp = pwsMessage;

        wprintf(L"Keyword message string: %s", ptemp);

        while (*(ptemp += wcslen(ptemp)+1))
            wprintf(L", %s", ptemp);

        wprintf(L"\n\n");
        free(pwsMessage);
        pwsMessage = NULL;
    }

    pwsMessage = GetMessageString(hProviderMetadata, hEvent, EvtFormatMessageChannel);
    if (pwsMessage)
    {
        wprintf(L"Channel message string: %s\n\n", pwsMessage);
        free(pwsMessage);
        pwsMessage = NULL;
    }

    pwsMessage = GetMessageString(hProviderMetadata, hEvent, EvtFormatMessageProvider);
    if (pwsMessage)
    {
        wprintf(L"Provider message string: %s\n\n", pwsMessage);
        free(pwsMessage);
        pwsMessage = NULL;
    }

    pwsMessage = GetMessageString(hProviderMetadata, hEvent, EvtFormatMessageXml);
    if (pwsMessage)
    {
        wprintf(L"XML message string: %s\n\n", pwsMessage);
        free(pwsMessage);
        pwsMessage = NULL;
    }

cleanup:

    if (hEvent)
        EvtClose(hEvent);

    if (hResults)
        EvtClose(hResults);
    
    if (hProviderMetadata)
        EvtClose(hProviderMetadata);
}


// Gets the specified message string from the event. If the event does not
// contain the specified message, the function returns NULL.
LPWSTR GetMessageString(EVT_HANDLE hMetadata, EVT_HANDLE hEvent, EVT_FORMAT_MESSAGE_FLAGS FormatId)
{
    LPWSTR pBuffer = NULL;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD status = 0;

    if (!EvtFormatMessage(hMetadata, hEvent, 0, 0, NULL, FormatId, dwBufferSize, pBuffer, &dwBufferUsed))
    {
        status = GetLastError();
        if (ERROR_INSUFFICIENT_BUFFER == status)
        {
            // An event can contain one or more keywords. The function returns keywords
            // as a list of keyword strings. To process the list, you need to know the
            // size of the buffer, so you know when you have read the last string, or you
            // can terminate the list of strings with a second null terminator character 
            // as this example does.
            if ((EvtFormatMessageKeyword == FormatId))
                pBuffer[dwBufferSize-1] = L'\0';
            else
                dwBufferSize = dwBufferUsed;

            pBuffer = (LPWSTR)malloc(dwBufferSize * sizeof(WCHAR));

            if (pBuffer)
            {
                EvtFormatMessage(hMetadata, hEvent, 0, 0, NULL, FormatId, dwBufferSize, pBuffer, &dwBufferUsed);

                // Add the second null terminator character.
                if ((EvtFormatMessageKeyword == FormatId))
                    pBuffer[dwBufferUsed-1] = L'\0';
            }
            else
            {
                wprintf(L"malloc failed\n");
            }
        }
        else if (ERROR_EVT_MESSAGE_NOT_FOUND == status || ERROR_EVT_MESSAGE_ID_NOT_FOUND == status)
            ;
        else
        {
            wprintf(L"EvtFormatMessage failed with %u\n", status);
        }
    }

    return pBuffer;
}
```



 

 




