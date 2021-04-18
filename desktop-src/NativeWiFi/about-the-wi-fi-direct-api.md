---
description: L’API WiFi Native contient un ensemble de fonctions qui prennent en charge l’utilisation de Wi-Fi directe pour les applications de bureau.
ms.assetid: A649EBBA-1076-4426-9C4D-85AB8C415C66
title: À propos de la fonctionnalité Wi-Fi directe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e503cb2bf86f81904b1c85c2bdf96b66c0762e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519549"
---
# <a name="about-the-wi-fi-direct-feature"></a>À propos de la fonctionnalité Wi-Fi directe

L’API WiFi Native contient un ensemble de fonctions qui prennent en charge l’utilisation de Wi-Fi directe pour les applications de bureau. À compter de Windows 8 et de Windows Server 2012, Wi-Fi fonctions directes ont été ajoutées à l’API WiFi native.

La fonctionnalité de Wi-Fi directe est basée sur le développement de la Wi-Fi spécifications techniques d’égal à égal v 1.1 par le Wi-Fi Alliance (voir [spécifications de Wi-Fi Alliance publiées](https://www.wi-fi.org/)). L’objectif de la spécification technique d’égal à égal Wi-Fi consiste à fournir une solution pour Wi-Fi la connectivité appareil-appareil sans avoir besoin d’un point d’accès sans fil (AP sans fil) pour configurer la connexion ou l’utilisation du mécanisme existant Wi-Fi ad hoc (IBSS).

> [!Note]  
> Le mode ad hoc n’est peut-être pas disponible dans les futures versions de Windows. À partir de Windows 8.1 et de Windows Server 2012 R2, utilisez Wi-Fi direct à la place.

 

Pour une application de bureau, la fonctionnalité de Wi-Fi directe requiert que les appareils Wi-FI direct soient déjà associés par l’utilisateur à l’interface utilisateur expérience de couplage Windows. Une fois cette association terminée, un profil est stocké, ce qui permet au Wi-Fi fonctions directes d’être utilisées pour démarrer une session Wi-Fi directe afin d’établir une connexion entre les Wi-Fi les appareils directs.

Les fonctions suivantes prennent en charge la fonctionnalité Wi-Fi directe.

-   [**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) : indique que l’application souhaite annuler une fonction [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) en attente qui n’est pas terminée.
-   [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) : ferme un handle vers le service Wi-Fi direct.
-   [**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) : ferme une session après un appel précédemment réussi à la fonction [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) .
-   [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) : ouvre un handle vers le service Wi-Fi direct et négocie une version de l’API Wi-Fi direct à utiliser.
-   [**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) : récupère et applique un profil stocké pour une Wi-Fi appareil hérité direct.
-   [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) : démarre une connexion à la demande à un appareil spécifique Wi-Fi direct, qui a été précédemment associé à l’expérience de couplage Windows.
-   [**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) : met à jour la visibilité de l’appareil pour le Wi-Fi adresse directe de l’appareil pour un nœud d’appareil Wi-Fi installé spécifique installé.
-   [**WFD \_ OUVERTURE d’une \_ session \_ complète \_ callback**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) : définit la fonction de rappel qui est appelée par la fonction [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) lorsque l’opération **WFDStartOpenSession** est terminée.

Pour plus d’informations sur l’utilisation de Wi-Fi direct dans une application de bureau, consultez [utilisation des fonctions directes Wi-Fi](using-the-wi-fi-direct-api.md).

Pour plus d’informations sur Wi-Fi directe pour une utilisation dans les applications du Windows Store, consultez [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) et les classes associées dans l’espace de noms [**Windows. Networking. proximite**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Autres ressources**
</dt> <dt>

[À propos de la WiFi Native](about-native-wifi.md)
</dt> <dt>

[À propos de l’API WiFi Native](about-the-native-wifi-api.md)
</dt> <dt>

[À propos de l’API ad hoc sans fil](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[Utilisation des fonctions Wi-Fi direct](using-the-wi-fi-direct-api.md)
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

 

 
