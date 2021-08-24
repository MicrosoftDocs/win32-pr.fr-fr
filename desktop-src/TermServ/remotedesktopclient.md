---
title: RemoteDesktopClient, classe
description: implémente l’application Microsoft Windows Store Bureau à distance le contrôle Client-version 1.
ms.assetid: 0910883A-BD49-4908-8423-1FC280E0FE0C
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la classe RemoteDesktopClient
- Services Bureau à distance de la classe RemoteDesktopClient, Description
topic_type:
- apiref
api_name:
- RemoteDesktopClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad76c8c189854a28709765c5677d047590216ae8ab6271d44c595f7b24fdd88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865898"
---
# <a name="remotedesktopclient-class"></a>RemoteDesktopClient, classe

implémente l’application Microsoft Windows Store Bureau à distance le contrôle Client-version 1

Cette classe implémente les interfaces suivantes.

-   [**IRemoteDesktopClient**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
-   [**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)

**RemoteDesktopClient** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **RemoteDesktopClient** possède ces méthodes.



| Méthode                                                                                      | Description                                                                                                                                                        |
|:--------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attachEvent**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-attachevent)                                     | Attache un gestionnaire d’événements à un événement.<br/>                                                                                                                  |
| [**Connecter**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-connect)                                             | Établit une connexion à l’aide des propriétés actuellement définies sur le contrôle client du conteneur d’applications protocole RDP (Remote Desktop Protocol) (RDP).<br/>                         |
| [**DeleteSavedCredentials**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-deletesavedcredentials)               | Supprime les informations d’identification enregistrées pour l’ordinateur distant spécifié.<br/>                                                                                            |
| [**detachEvent**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-detachevent)                                     | Détache un gestionnaire d’événements d’un événement.<br/>                                                                                                                |
| [**Déconnecter**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-disconnect)                                       | Déconnecte la connexion active.<br/>                                                                                                                      |
| [**OnAdminMessageReceived**](iremotedesktopclientevents-onadminmessagereceived.md)         | Appelé lorsque le contrôle client reçoit un message d’administration.<br/>                                                                                      |
| [**OnAutoReconnected**](iremotedesktopclientevents-onautoreconnected.md)                   | Appelé lorsque le contrôle client se reconnecte automatiquement à une session à distance.<br/>                                                                       |
| [**OnAutoReconnecting**](iremotedesktopclientevents-onautoreconnecting.md)                 | Appelé lorsque le contrôle client tente de rétablir automatiquement une connexion à une session à distance.<br/>                                                  |
| [**OnConnected**](iremotedesktopclientevents-onconnected.md)                               | Appelé lorsque le contrôle client s’est connecté à une session à distance.<br/>                                                                                       |
| [**OnConnecting**](iremotedesktopclientevents-onconnecting.md)                             | Appelé lorsque le contrôle client tente d’établir une connexion à une session à distance.<br/>                                                                  |
| [**OnDialogDismissed**](iremotedesktopclientevents-ondialogdismissed.md)                   | Appelé après la fermeture d’une boîte de dialogue affichée par le contrôle client.<br/>                                                                                 |
| [**OnDialogDisplaying**](iremotedesktopclientevents-ondialogdisplaying.md)                 | Appelé avant que le contrôle affiche une boîte de dialogue.<br/>                                                                                                        |
| [**OnDisconnected**](iremotedesktopclientevents-ondisconnected.md)                         | Appelé lorsque le contrôle client a été déconnecté d’une session à distance.<br/>                                                                             |
| [**OnKeyCombinationPressed**](iremotedesktopclientevents-onkeycombinationpressed.md)       | Appelé lorsque des combinaisons de touches spéciales sont activées dans la session à distance.<br/>                                                                                 |
| [**OnLoginCompleted**](iremotedesktopclientevents-onlogincompleted.md)                     | Appelé lorsque le contrôle client a réussi à se connecter à une session à distance.<br/>                                                                          |
| [**OnNetworkStatusChanged**](iremotedesktopclientevents-onnetworkstatuschanged.md)         | Appelé lorsque l’état du réseau a changé.<br/>                                                                                                             |
| [**OnRemoteDesktopSizeChanged**](iremotedesktopclientevents-onremotedesktopsizechanged.md) | Appelé lorsque la taille du Bureau à distance a changé.<br/>                                                                                                        |
| [**OnStatusChanged**](iremotedesktopclientevents-onstatuschanged.md)                       | Appelé lorsque le contrôle client a mis à jour son état.<br/>                                                                                                  |
| [**OnTouchPointerCursorMoved**](iremotedesktopclientevents-ontouchpointercursormoved.md)   | Appelé lorsque le curseur tactile a été déplacé et que la propriété [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) a la valeur true.<br/> |
| [**Reconnexion**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-reconnect)                                         | Lance une reconnexion automatique du contrôle client du conteneur d’applications protocole RDP (Remote Desktop Protocol) (RDP) pour ajuster la taille de la session à la nouvelle largeur et à la hauteur.<br/>   |
| [**UpdateSessionDisplaySettings**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-updatesessiondisplaysettings)   | Met à jour les paramètres de largeur et de hauteur pour le contrôle client du conteneur d’applications protocole RDP (Remote Desktop Protocol) (RDP).<br/>                                               |



 

### <a name="properties"></a>Propriétés

La classe **RemoteDesktopClient** possède les propriétés suivantes.



| Propriété                                                             | Type d’accès          | Description                                                                                                                                                            |
|:---------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Actions**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_actions)<br/>           | Lecture seule<br/> | Récupère l’objet actions pour le client de conteneur d’application protocole RDP (Remote Desktop Protocol) (RDP).<br/>                                                                    |
| [**Paramètres**](iremotedesktopclient-settings.md)<br/>         | Lecture seule<br/> | Récupère l’objet de paramètres pour le client de conteneur d’applications protocole RDP (Remote Desktop Protocol) (RDP).<br/>                                                                   |
| [**TouchPointer**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_touchpointer)<br/> | Lecture seule<br/> | Contient l’objet [**RemoteDesktopClientTouchPointer**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer) pour le client de conteneur d’application protocole RDP (Remote Desktop Protocol) (RDP).<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                           |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| CLSID<br/>                    | Le CLSID \_ RemoteDesktopClient est défini en tant que EAB16C5D-EED1-4E95-868B-0FBA1B42C092<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Bureau à distance ActiveX les classes de contrôle](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

