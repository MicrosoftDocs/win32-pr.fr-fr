---
description: Utilisation des API de journalisation pour les contrôles parentaux
ms.assetid: 6c38a634-53ba-4e76-83bf-1a3f36efb0bc
title: Utilisation des API de journalisation pour les contrôles parentaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 571a24f8bdbf687f8c1975cfc29057035ac56747edc0459682512531194c55a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869061"
---
# <a name="using-logging-apis-for-parental-controls"></a>Utilisation des API de journalisation pour les contrôles parentaux

### <a name="activity-reporting-logging"></a>Rapport d’activité (journalisation)

Le fichier d’en-tête WpcEvent. h contient les définitions des champs pour chaque type d’événement d’activité prédéfini et le type personnalisé. Cet exemple de code illustre les étapes de journalisation d’un événement d’invitation à une conversation de messagerie instantanée à l’aide de l’API de publication ETW :


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



### <a name="custom-logging"></a>Journalisation personnalisée

Pour qu’une application étende les événements journalisés en dehors de l’ensemble des événements prédéfinis ou du type personnalisé, vous devez définir un fournisseur pour celui-ci dans le manifeste de l’application. Le canal par défaut WPC peut ensuite être importé et les événements définis par l’application peuvent ensuite être journalisés.

### <a name="logging-rights"></a>Droits de journalisation

Le canal de journalisation WPC est contrôlé par la [*liste de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL) pour fournir un accès complet uniquement aux administrateurs. Les comptes non-administrateurs peuvent écrire dans le canal mais n’ont pas d’accès en lecture ou en suppression. L’accès au canal consiste à utiliser l’API ETW.

### <a name="parental-controls-logging-provider-details"></a>Détails du fournisseur de journalisation des contrôles parentaux

le fournisseur WPC est nommé Microsoft.com/Windows/ParentalControls avec le GUID {01090065-B467-4503-9B28-533766761087}. le canal de journalisation local par défaut est Microsoft.com/Windows/ParentalControls/LocalEvents.

les fichiers journaux sont stockés dans le \\ dossier Windows System32 \\ Wpc \\ Logs.

### <a name="notification-of-impending-time-limits-logout"></a>Notification de déconnexion de limites de temps imminentes

Le système de contrôle parental déclenche un événement d’avertissement à 15 minutes, puis à une minute avant la déconnexion d’un utilisateur contrôlé en fonction de restrictions de temps. les Applications peuvent s’abonner à ces événements, en particulier lorsqu’elles s’exécutent en mode plein écran DirectX, où les notifications de Windows standard ne sont pas affichées. Un exemple de code qui montre comment s’abonner aux événements, inscrire une fonction de rappel et recevoir les événements est fourni.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble des fonctionnalités d’extensibilité des contrôles parentaux](parental-controls-extensibility-features-overview.md)
</dt> <dt>

[**descripteur des données d’événement \_ \_**](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor)
</dt> <dt>

[**EventDataDescCreate**](/windows/desktop/api/evntprov/nf-evntprov-eventdatadesccreate)
</dt> <dt>

[**WPC \_ args \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 
