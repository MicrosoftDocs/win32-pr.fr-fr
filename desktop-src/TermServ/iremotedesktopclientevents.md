---
title: Interface IRemoteDesktopClientEvents
description: Fournit des méthodes qui reçoivent des informations du serveur qui sont liées aux événements de contrôle du client.
ms.assetid: CF1DA4C8-94A5-4E6A-AEB7-6F46117E9DF2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IRemoteDesktopClientEvents
- Services Bureau à distance de l’interface IRemoteDesktopClientEvents, Description
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bae11edf7e6c603c534afb75fe5c90bcc868f1e359f1d78748dd94b18b5627e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657069"
---
# <a name="iremotedesktopclientevents-interface"></a>Interface IRemoteDesktopClientEvents

Fournit des méthodes qui reçoivent des informations du serveur qui sont liées aux événements de contrôle du client. Les événements incluent la connexion et la déconnexion, les demandes en mode plein écran, la réussite de l’ouverture de session et les conditions d’erreur.

## <a name="members"></a>Membres

L’interface **IRemoteDesktopClientEvents** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IRemoteDesktopClientEvents** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IRemoteDesktopClientEvents** possède ces méthodes.



| Méthode                                                                                      | Description                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnAdminMessageReceived**](iremotedesktopclientevents-onadminmessagereceived.md)         | Appelé lorsque le contrôle client reçoit un message d’administration. <br/>                                                                                      |
| [**OnAutoReconnected**](iremotedesktopclientevents-onautoreconnected.md)                   | Appelé lorsque le contrôle client se reconnecte automatiquement à une session à distance. <br/>                                                                       |
| [**OnAutoReconnecting**](iremotedesktopclientevents-onautoreconnecting.md)                 | Appelé lorsque le contrôle client tente de rétablir automatiquement une connexion à une session à distance. <br/>                                                  |
| [**OnConnected**](iremotedesktopclientevents-onconnected.md)                               | Appelé lorsque le contrôle client s’est connecté à une session à distance.<br/>                                                                                        |
| [**OnConnecting**](iremotedesktopclientevents-onconnecting.md)                             | Appelé lorsque le contrôle client tente d’établir une connexion à une session à distance. <br/>                                                                  |
| [**OnDialogDismissed**](iremotedesktopclientevents-ondialogdismissed.md)                   | Appelé après la fermeture d’une boîte de dialogue affichée par le contrôle client. <br/>                                                                                 |
| [**OnDialogDisplaying**](iremotedesktopclientevents-ondialogdisplaying.md)                 | Appelé avant que le contrôle affiche une boîte de dialogue. <br/>                                                                                                        |
| [**OnDisconnected**](iremotedesktopclientevents-ondisconnected.md)                         | Appelé lorsque le contrôle client a été déconnecté d’une session à distance. <br/>                                                                             |
| [**OnKeyCombinationPressed**](iremotedesktopclientevents-onkeycombinationpressed.md)       | Appelé lorsque des combinaisons de touches spéciales sont activées dans la session à distance. <br/>                                                                                 |
| [**OnLoginCompleted**](iremotedesktopclientevents-onlogincompleted.md)                     | Appelé lorsque le contrôle client a réussi à se connecter à une session à distance. <br/>                                                                          |
| [**OnNetworkStatusChanged**](iremotedesktopclientevents-onnetworkstatuschanged.md)         | Appelé lorsque l’état du réseau a changé. <br/>                                                                                                             |
| [**OnRemoteDesktopSizeChanged**](iremotedesktopclientevents-onremotedesktopsizechanged.md) | Appelé lorsque la taille du Bureau à distance a changé. <br/>                                                                                                        |
| [**OnStatusChanged**](iremotedesktopclientevents-onstatuschanged.md)                       | Appelé lorsque le contrôle client a mis à jour son état. <br/>                                                                                                  |
| [**OnTouchPointerCursorMoved**](iremotedesktopclientevents-ontouchpointercursormoved.md)   | Appelé lorsque le curseur tactile a été déplacé et que la propriété [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) a la valeur true. <br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                           |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                 |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| CLSID<br/>                    | Le CLSID \_ RemoteDesktopClient est défini en tant que EAB16C5D-EED1-4E95-868B-0FBA1B42C092<br/>       |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents est défini comme 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[référence de contrôle de ActiveX Bureau à distance](remote-desktop-activex-control-reference.md)
</dt> </dl>

 

