---
description: Utilisation des API de journalisation pour les contrôles parentaux
ms.assetid: 6c38a634-53ba-4e76-83bf-1a3f36efb0bc
title: Utilisation des API de journalisation pour les contrôles parentaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d1cedb9ff02856be6ea1ae2069d8635b980681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865569"
---
# <a name="using-logging-apis-for-parental-controls"></a><span data-ttu-id="793f0-103">Utilisation des API de journalisation pour les contrôles parentaux</span><span class="sxs-lookup"><span data-stu-id="793f0-103">Using Logging APIs for Parental Controls</span></span>

### <a name="activity-reporting-logging"></a><span data-ttu-id="793f0-104">Rapport d’activité (journalisation)</span><span class="sxs-lookup"><span data-stu-id="793f0-104">Activity Reporting (Logging)</span></span>

<span data-ttu-id="793f0-105">Le fichier d’en-tête WpcEvent. h contient les définitions des champs pour chaque type d’événement d’activité prédéfini et le type personnalisé.</span><span class="sxs-lookup"><span data-stu-id="793f0-105">The WpcEvent.h header file contains definitions of the fields for each predefined activity event type and the custom type.</span></span> <span data-ttu-id="793f0-106">Cet exemple de code illustre les étapes de journalisation d’un événement d’invitation à une conversation de messagerie instantanée à l’aide de l’API de publication ETW :</span><span class="sxs-lookup"><span data-stu-id="793f0-106">This sample code shows the steps for logging an instant messaging conversation invitation event using the ETW publishing API:</span></span>


```C++
#include <windows.h>
#include <evntprov.h>
#include <wpcevent.h>

#pragma comment(lib, "advapi32.lib")

#define BYTELEN(x) ((wcslen(x) + 1) * sizeof(WCHAR))

void main()
{
    REGHANDLE hWpc = 0;

    // Register
    ULONG res = EventRegister(&WPCPROV, NULL, NULL, &hWpc);

    // Log an event
    PCWSTR pcszAppName = L"SuperIM";
    PCWSTR pcszAppVersion = L"7.0";
    PCWSTR pcszAccountName = L"Kate";
    PCWSTR pcszConvID = L"102";
    PCWSTR pcszRequestingIP = L"192.168.2.100";
    PCWSTR pcszSender = L"imperson@isp.com";
    const DWORD dwReason = WPCFLAG_ISBLOCKED_NOTBLOCKED;
    const DWORD dwRecipCount = 1;
    PCWSTR pcszRecipient = L"otherim@isp.com";

    EVENT_DATA_DESCRIPTOR eventData[WPC_ARGS_CONVERSATIONINITEVENT_CARGS];

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_APPNAME],
        (const PVOID)pcszAppName, (ULONG)BYTELEN(pcszAppName));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_APPVERSION],
        (const PVOID)pcszAppVersion,(ULONG)BYTELEN(pcszAppVersion));

    EventDataDescCreate(
        &eventData[WPC_ARGS_CONVERSATIONINITEVENT_ACCOUNTNAME], 
        (const PVOID)pcszAccountName, (ULONG)BYTELEN(pcszAccountName));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_CONVID], 
        (const PVOID)pcszConvID, (ULONG)BYTELEN(pcszConvID));

    EventDataDescCreate(
        &eventData[WPC_ARGS_CONVERSATIONINITEVENT_REQUESTINGIP], 
        (const PVOID)pcszRequestingIP, (ULONG)BYTELEN(pcszRequestingIP));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_SENDER],
        (const PVOID)pcszSender, (ULONG)BYTELEN(pcszSender));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_REASON],
        (const PVOID)&dwReason, sizeof(dwReason));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_RECIPCOUNT],
        (const PVOID)&dwRecipCount, sizeof(dwRecipCount));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_RECIPIENT],
        (const PVOID)pcszRecipient, (ULONG)BYTELEN(pcszRecipient));


    ULONG lRet = EventWrite(hWpc, &WPCEVENT_IM_INVITATION, ARRAYSIZE(eventData), eventData);

    // Unregister
    EventUnregister(hWpc);
}
```



### <a name="custom-logging"></a><span data-ttu-id="793f0-107">Journalisation personnalisée</span><span class="sxs-lookup"><span data-stu-id="793f0-107">Custom Logging</span></span>

<span data-ttu-id="793f0-108">Pour qu’une application étende les événements journalisés en dehors de l’ensemble des événements prédéfinis ou du type personnalisé, vous devez définir un fournisseur pour celui-ci dans le manifeste de l’application.</span><span class="sxs-lookup"><span data-stu-id="793f0-108">For an application to extend the events logged outside the set of predefined events or the one custom type, you will need to define a provider for that in the application manifest.</span></span> <span data-ttu-id="793f0-109">Le canal par défaut WPC peut ensuite être importé et les événements définis par l’application peuvent ensuite être journalisés.</span><span class="sxs-lookup"><span data-stu-id="793f0-109">The WPC default channel can then be imported and application-defined events can then be logged.</span></span>

### <a name="logging-rights"></a><span data-ttu-id="793f0-110">Droits de journalisation</span><span class="sxs-lookup"><span data-stu-id="793f0-110">Logging Rights</span></span>

<span data-ttu-id="793f0-111">Le canal de journalisation WPC est contrôlé par la [*liste de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL) pour fournir un accès complet uniquement aux administrateurs.</span><span class="sxs-lookup"><span data-stu-id="793f0-111">The WPC logging channel is controlled by [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) to provide full access for administrators only.</span></span> <span data-ttu-id="793f0-112">Les comptes non-administrateurs peuvent écrire dans le canal mais n’ont pas d’accès en lecture ou en suppression.</span><span class="sxs-lookup"><span data-stu-id="793f0-112">Non-administrator accounts may write to the channel but have no read or delete access.</span></span> <span data-ttu-id="793f0-113">L’accès au canal consiste à utiliser l’API ETW.</span><span class="sxs-lookup"><span data-stu-id="793f0-113">Access to the channel is by using the ETW API.</span></span>

### <a name="parental-controls-logging-provider-details"></a><span data-ttu-id="793f0-114">Détails du fournisseur de journalisation des contrôles parentaux</span><span class="sxs-lookup"><span data-stu-id="793f0-114">Parental Controls Logging Provider Details</span></span>

<span data-ttu-id="793f0-115">Le fournisseur WPC est nommé Microsoft.com/Windows/ParentalControls avec le GUID {01090065-B467-4503-9B28-533766761087}.</span><span class="sxs-lookup"><span data-stu-id="793f0-115">The WPC provider is named Microsoft.com/Windows/ParentalControls with GUID {01090065-B467-4503-9B28-533766761087}.</span></span> <span data-ttu-id="793f0-116">Le canal de journalisation local par défaut est Microsoft.com/Windows/ParentalControls/LocalEvents.</span><span class="sxs-lookup"><span data-stu-id="793f0-116">The default local logging channel is Microsoft.com/Windows/ParentalControls/LocalEvents.</span></span>

<span data-ttu-id="793f0-117">Les fichiers journaux sont stockés dans le \\ dossier Windows system32 \\ WPC \\ logs.</span><span class="sxs-lookup"><span data-stu-id="793f0-117">Log files are stored in the Windows\\System32\\Wpc\\Logs folder.</span></span>

### <a name="notification-of-impending-time-limits-logout"></a><span data-ttu-id="793f0-118">Notification de déconnexion de limites de temps imminentes</span><span class="sxs-lookup"><span data-stu-id="793f0-118">Notification of Impending Time Limits Logout</span></span>

<span data-ttu-id="793f0-119">Le système de contrôle parental déclenche un événement d’avertissement à 15 minutes, puis à une minute avant la déconnexion d’un utilisateur contrôlé en fonction de restrictions de temps.</span><span class="sxs-lookup"><span data-stu-id="793f0-119">The Parental Controls system will fire a warning event at 15 minutes and again at 1 minute before logout of a controlled user based on time restrictions.</span></span> <span data-ttu-id="793f0-120">Les applications peuvent s’abonner à ces événements, en particulier lorsqu’elles s’exécutent en mode plein écran DirectX dans lequel les notifications Windows standard ne sont pas affichées.</span><span class="sxs-lookup"><span data-stu-id="793f0-120">Applications can subscribe to these events, especially when they are running in DirectX full-screen mode where standard Windows notifications are not displayed.</span></span> <span data-ttu-id="793f0-121">Un exemple de code qui montre comment s’abonner aux événements, inscrire une fonction de rappel et recevoir les événements est fourni.</span><span class="sxs-lookup"><span data-stu-id="793f0-121">Sample code is provided that shows how to subscribe to the events, register a callback function, and receive the events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="793f0-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="793f0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="793f0-123">Vue d’ensemble des fonctionnalités d’extensibilité des contrôles parentaux</span><span class="sxs-lookup"><span data-stu-id="793f0-123">Parental Controls Extensibility Features Overview</span></span>](parental-controls-extensibility-features-overview.md)
</dt> <dt>

[<span data-ttu-id="793f0-124">**descripteur des données d’événement \_ \_**</span><span class="sxs-lookup"><span data-stu-id="793f0-124">**EVENT\_DATA\_DESCRIPTOR**</span></span>](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor)
</dt> <dt>

[<span data-ttu-id="793f0-125">**EventDataDescCreate**</span><span class="sxs-lookup"><span data-stu-id="793f0-125">**EventDataDescCreate**</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventdatadesccreate)
</dt> <dt>

[<span data-ttu-id="793f0-126">**WPC \_ args \_ CONVERSATIONINITEVENT**</span><span class="sxs-lookup"><span data-stu-id="793f0-126">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 
