---
description: Montre comment utiliser Wi-Fi fonctions directes dans les applications de bureau.
ms.assetid: 50B95B7D-B860-44DF-8E78-1E7D2DC5A9B6
title: Utilisation des fonctions Wi-Fi direct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa9a00a5474632ed54a84a7dc8cc5c64774e7cfe7547e6994acee599df2461ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684729"
---
# <a name="using-the-wi-fi-direct-functions"></a>Utilisation des fonctions Wi-Fi direct

Cette rubrique montre comment utiliser Wi-Fi fonctions directes dans les applications de bureau. à partir de Windows 8 et Windows Server 2012, Wi-Fi fonctions directes ont été ajoutées à l’API Wifi Native.

La fonctionnalité de Wi-Fi directe est basée sur le développement de la Wi-Fi spécifications techniques d’égal à égal v 1.1 par le Wi-Fi Alliance (voir [spécifications de Wi-Fi Alliance publiées](https://www.wi-fi.org/)). L’objectif de la spécification technique d’égal à égal Wi-Fi consiste à fournir une solution pour Wi-Fi la connectivité appareil-appareil sans avoir besoin d’un point d’accès sans fil (AP sans fil) pour configurer la connexion ou l’utilisation du mécanisme existant Wi-Fi ad hoc (IBSS).

> [!Note]  
> Le mode ad hoc n’est peut-être pas disponible dans les versions ultérieures de Windows. à partir de Windows 8.1 et Windows Server 2012 R2, utilisez Wi-Fi Direct à la place.

 

Les fonctions suivantes prennent en charge la fonctionnalité Wi-Fi directe.

-   [**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) : indique que l’application souhaite annuler une fonction [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) en attente qui n’est pas terminée.
-   [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) : ferme un handle vers le service Wi-Fi direct.
-   [**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) : ferme une session après un appel précédemment réussi à la fonction [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) .
-   [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) : ouvre un handle vers le service Wi-Fi direct et négocie une version de l’API Wi-Fi direct à utiliser.
-   [**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) : récupère et applique un profil stocké pour une Wi-Fi appareil hérité direct.
-   [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) : démarre une connexion à la demande à un appareil spécifique Wi-Fi Direct, qui a été précédemment associé à l’expérience de couplage Windows.
-   [**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) : met à jour la visibilité de l’appareil pour le Wi-Fi adresse directe de l’appareil pour un nœud d’appareil Wi-Fi installé spécifique installé.
-   [**WFD \_ OUVERTURE d’une \_ session \_ complète \_ callback**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) : définit la fonction de rappel qui est appelée par la fonction [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) lorsque l’opération **WFDStartOpenSession** est terminée.

pour une application de bureau, la fonctionnalité de Wi-Fi directe requiert que les appareils Wi-FI directs soient déjà associés par l’utilisateur à l’interface utilisateur expérience de couplage Windows. Une fois cette association terminée, un profil est stocké, ce qui permet au Wi-Fi fonctions directes d’être utilisées pour démarrer une session Wi-Fi directe afin d’établir une connexion entre les Wi-Fi les appareils directs.

Pour utiliser Wi-Fi directe, une application doit d’abord obtenir un handle pour le service Wi-Fi direct en appelant la fonction [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) . Le handle Wi-Fi direct (WFD) retourné par la fonction **WFDOpenHandle** est utilisé pour les appels de fonction directe Wi-Fis directs passés au service Wi-Fi direct.

La fonction [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) démarre une opération asynchrone pour démarrer une connexion à la demande à un appareil spécifique Wi-Fi direct. l’appareil Wi-Fi cible doit avoir été associé à l’expérience de couplage Windows. Lorsque l’opération asynchrone se termine, la fonction de rappel spécifiée dans le paramètre *pfnCallback* est appelée.

Une fois qu’une application a été effectuée à l’aide du service Wi-Fi direct, l’application doit appeler la fonction [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) pour signaler au service direct Wi-Fi que l’application est effectuée à l’aide du service. Cela permet au service Wi-Fi direct de libérer les ressources utilisées par l’application.

pour plus d’informations sur Wi-Fi Direct pour une utilisation Windows dans les applications du windows Store, consultez [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) et les classes connexes dans le [**Windows. Espace de noms Networking. proximite**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Autres ressources**
</dt> <dt>

[À propos de la WiFi Native](about-native-wifi.md)
</dt> <dt>

[À propos de l’API WiFi Native](about-the-native-wifi-api.md)
</dt> <dt>

[À propos de la fonctionnalité Wi-Fi directe](about-the-wi-fi-direct-api.md)
</dt> <dt>

**Référence**
</dt> <dt>

[**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[**\_rappel d’ouverture de session WFD \_ \_ terminé \_**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 
