---
title: Interface IMsRdpClient9
description: Fournit les méthodes et les propriétés nécessaires à la configuration et à l’utilisation du contrôle client. Dérive de l’interface IMsRdpClient8.
ms.assetid: 353f0328-d8a3-4466-bf23-c6d6b8a47e5d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, Description
topic_type:
- apiref
api_name:
- IMsRdpClient9
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3350fd4b9153319f9a1084ffc3fd37784eb6ad3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464798"
---
# <a name="imsrdpclient9-interface"></a>Interface IMsRdpClient9

Fournit les méthodes et les propriétés nécessaires à la configuration et à l’utilisation du contrôle client. Dérive de l’interface [**IMsRdpClient8**](imsrdpclient8.md) .

## <a name="members"></a>Membres

L’interface **IMsRdpClient9** hérite de [**IMsRdpClient8**](imsrdpclient8.md). **IMsRdpClient9** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IMsRdpClient9** possède ces méthodes.



| Méthode                                                                             | Description                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attachEvent**](imsrdpclient9-attachevent.md)                                   | Joint un événement.<br/>                                                                                                                                                               |
| [**Se connecter**](imstscax-connect.md)                                                | Établit une connexion à l’aide des propriétés actuellement définies sur le contrôle.<br/>                                                                                                        |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                    | Crée un objet de canal virtuel côté client pour chaque nom de canal virtuel spécifié.<br/>                                                                                            |
| [**detachEvent**](imsrdpclient9-detachevent.md)                                   | Détache un événement.<br/>                                                                                                                                                               |
| [**Déconnecter**](imstscax-disconnect.md)                                          | Déconnecte la connexion active.<br/>                                                                                                                                               |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                   | Récupère la description de l’erreur pour les événements de déconnexion de la session.<br/>                                                                                                               |
| [**GetStatusText**](imsrdpclient7-getstatustext.md)                               | Récupère le texte d’État pour le code d’état spécifié.<br/>                                                                                                                         |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)          | Récupère les options définies pour un canal virtuel.<br/>                                                                                                                                 |
| [**Reconnexion**](imsrdpclient8-reconnect.md)                                       | Se reconnecte à la session à distance avec la largeur et la hauteur du nouveau bureau.<br/>                                                                                                          |
| [**RequestClose**](imsrdpclient-requestclose.md)                                  | Demande un arrêt approprié du contrôle ActiveX Bureau à distance.<br/>                                                                                                              |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                      | Envoie des données au serveur hôte de session Bureau à distance via un canal virtuel qui a été créé précédemment à l’aide de la méthode [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .<br/> |
| [**SendRemoteAction**](imsrdpclient8-sendremoteaction.md)                         | Entraîne l’exécution d’une action dans la session à distance.<br/>                                                                                                                          |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)          | Définit les options de canal virtuel pour le contrôle ActiveX Bureau à distance.<br/>                                                                                                         |
| [**SyncSessionDisplaySettings**](imsrdpclient9-syncsessiondisplaysettings.md)     | Synchronise les paramètres d’affichage de la session.<br/>                                                                                                                                           |
| [**UpdateSessionDisplaySettings**](/previous-versions/windows/desktop/legacy/mt703457(v=vs.85)) | Met à jour les paramètres d’affichage de la session.<br/>                                                                                                                                                |



 

### <a name="properties"></a>Propriétés

L’interface **IMsRdpClient9** possède les propriétés suivantes.



| Propriété                                                                             | Type d’accès           | Description                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings**](imstscax-advancedsettings.md)<br/>                     | Lecture seule<br/>  | Récupère un pointeur d’interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .<br/>                                                                                                                                          |
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Lecture seule<br/>  | Récupère un pointeur vers l’interface [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) . L’interface peut être utilisée pour définir des paramètres avancés pour le contrôle client.<br/>                                             |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>              | Lecture seule<br/>  | Récupère un pointeur vers l’interface [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) . L’interface peut être utilisée pour définir des paramètres avancés pour le contrôle client.<br/>                                                     |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>              | Lecture seule<br/>  | Récupère un pointeur vers l’interface [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .<br/>                                                                                                                                |
| [**AdvancedSettings5**](imsrdpclient4-advancedsettings5.md)<br/>              | Lecture seule<br/>  | Récupère un pointeur vers une interface [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .<br/>                                                                                                                                 |
| [**AdvancedSettings6**](imsrdpclient5-advancedsettings6.md)<br/>              | Lecture seule<br/>  | Récupère l’interface [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) .<br/>                                                                                                                                             |
| [**AdvancedSettings7**](imsrdpclient6-advancedsettings7.md)<br/>              | Lecture seule<br/>  | Récupère l’interface [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) .<br/>                                                                                                                                             |
| [**AdvancedSettings8**](imsrdpclient7-advancedsettings8.md)<br/>              | Lecture seule<br/>  | Récupère un objet qui prend en charge l’interface [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) .<br/>                                                                                                                     |
| [**AdvancedSettings9**](imsrdpclient8-advancedsettings9.md)<br/>              | Lecture seule<br/>  | Contient un objet qui prend en charge l’interface [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) .<br/>                                                                                                                      |
| [**CipherStrength**](imstscax-cipherstrength.md)<br/>                         | Lecture seule<br/>  | Récupère la force de chiffrement maximale du contrôle actuel.<br/>                                                                                                                                                                           |
| [**La**](imsrdpclient-colordepth.md)<br/>                             | Lecture/écriture<br/> | Profondeur de couleur (en bits par pixel) de la connexion du contrôle.<br/>                                                                                                                                                                           |
| [**Connecté**](imstscax-connected.md)<br/>                                   | Lecture seule<br/>  | Récupère l’état de connexion du contrôle actuel.<br/>                                                                                                                                                                                      |
| [**ConnectedStatusText**](imsrdpclient2-connectedstatustext.md)<br/>          | Lecture/écriture<br/> | Contient le texte affiché dans la zone cliente du contrôle pendant que le contrôle est dans l’état connecté.<br/>                                                                                                                          |
| [**ConnectingText**](imstscax-connectingtext.md)<br/>                         | Lecture/écriture<br/> | Spécifie le texte qui apparaît centré dans le contrôle pendant la connexion du contrôle.<br/>                                                                                                                                                    |
| [**DesktopHeight**](imstscax-desktopheight.md)<br/>                           | Lecture/écriture<br/> | Spécifie la hauteur, en pixels, du contrôle actuel sur le Bureau à distance initial.<br/>                                                                                                                                                           |
| [**DesktopWidth**](imstscax-desktopwidth.md)<br/>                             | Lecture/écriture<br/> | Spécifie la largeur, en pixels, du contrôle actif sur le Bureau à distance initial.<br/>                                                                                                                                                            |
| [**DisconnectedText**](imstscax-disconnectedtext.md)<br/>                     | Lecture/écriture<br/> | Spécifie le texte qui apparaît centré dans le contrôle avant qu’une connexion ne soit terminée.<br/>                                                                                                                                                  |
| [**Domaine**](imstscax-domain.md)<br/>                                         | Lecture/écriture<br/> | Spécifie le domaine auquel l’utilisateur actuel se connecte.<br/>                                                                                                                                                                                     |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | Lecture seule<br/>  | Contient des informations étendues sur la raison de la déconnexion du contrôle.<br/>                                                                                                                                                                 |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                             | Lecture/écriture<br/> | Détermine si le contrôle client est en mode plein écran.<br/>                                                                                                                                                                               |
| [**FullScreenTitle**](imstscax-fullscreentitle.md)<br/>                       | Écriture seule<br/> | Spécifie le titre de la fenêtre qui s’affiche lorsque le contrôle est en mode plein écran.<br/>                                                                                                                                                               |
| [**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)<br/> | Lecture seule<br/>  | Indique si le contrôle a affiché une barre de défilement horizontale.<br/>                                                                                                                                                                        |
| [**MsRdpClientShell**](imsrdpclient5-msrdpclientshell.md)<br/>                | Lecture seule<br/>  | Récupère l’interface de paramètre client scriptable [**IMsRdpClientShell**](imsrdpclientshell.md).<br/>                                                                                                                                           |
| [**RemoteProgram**](imsrdpclient5-remoteprogram.md)<br/>                      | Lecture seule<br/>  | Récupère un objet qui prend en charge l’interface [**ITSRemoteProgram**](itsremoteprogram.md) .<br/>                                                                                                                                               |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>                    | Lecture seule<br/>  | Récupère un objet qui prend en charge l’interface [**ITSRemoteProgram2**](itsremoteprogram2.md) .<br/>                                                                                                                                             |
| [**SecuredSettings**](imstscax-securedsettings.md)<br/>                       | Lecture seule<br/>  | Récupère un pointeur d’interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .<br/>                                                                                                                                            |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Lecture seule<br/>  | Récupère un pointeur vers l’interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) . Cette interface peut être utilisée pour définir des paramètres sécurisés pour le contrôle client.<br/>                                               |
| [**SecuredSettings3**](imsrdpclient7-securedsettings3.md)<br/>                | Lecture seule<br/>  | Récupère un objet qui prend en charge l’interface [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) .<br/>                                                                                                                       |
| [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md)<br/>         | Lecture seule<br/>  | Indique si l’interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) est disponible. Autrement dit, si la page Web contenant le contrôle se trouve actuellement dans l’une des zones de sécurité d’URL Internet Explorer autorisées.<br/> |
| [**Serveur**](imstscax-server.md)<br/>                                         | Lecture/écriture<br/> | Spécifie le nom du serveur auquel le contrôle actuel est connecté.<br/>                                                                                                                                                                 |
| [**StartConnected**](imstscax-startconnected.md)<br/>                         | Lecture/écriture<br/> | Indique si le contrôle établira la connexion au serveur hôte de session Bureau à distance dès le démarrage.<br/>                                                                                                                                |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/>              | Lecture seule<br/>  | Récupère ce qui a été passé via un script à l’interface [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) .<br/>                                                                                                         |
| [**TransportSettings2**](imsrdpclient6-transportsettings2.md)<br/>            | Lecture seule<br/>  | Récupère l’interface [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) .<br/>                                                                                                                                           |
| [**TransportSettings3**](imsrdpclient7-transportsettings3.md)<br/>            | Lecture seule<br/>  | Récupère un objet qui prend en charge l’interface [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) .<br/>                                                                                                                   |
| [**TransportSettings4**](imsrdpclient9-transportsettings4.md)<br/>            | Lecture seule<br/>  | Récupère un objet qui prend en charge l’interface [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) .<br/>                                                                                                                   |
| [**Nom d’utilisateur**](imstscax-username.md)<br/>                                     | Lecture/écriture<br/> | Spécifie les informations d’identification d’ouverture de session de nom d’utilisateur.<br/>                                                                                                                                                                                                   |
| [**Version**](imstscax-version.md)<br/>                                       | Lecture seule<br/>  | Spécifie le numéro de version du contrôle actuel.<br/>                                                                                                                                                                                        |
| [**VerticalScrollBarVisible**](imstscax-verticalscrollbarvisible.md)<br/>     | Lecture seule<br/>  | Indique si le contrôle affiche une barre de défilement verticale.<br/>                                                                                                                                                                               |



 

## <a name="remarks"></a>Notes

L’interface **IMsRdpClient9** a été étendue par les interfaces suivantes, chaque nouvelle interface héritant de toutes les méthodes et propriétés des interfaces précédentes :

-   [**IMsRdpClient10**](imsrdpclient10.md)

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                                                                                                                                                                                                                                                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                                                                                                                                                                                                                                                                                               |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                          |
| CLSID<br/>                    | Le CLSID \_ MsRdpClient10 est défini en tant que C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> Le CLSID \_ MsRdpClient10NotSafeForScripting est défini en tant que A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> Le CLSID \_ MsRdpClient9 est défini en tant que 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> Le CLSID \_ MsRdpClient9NotSafeForScripting est défini en tant que 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClient9 est défini en tant que 28904001-04B6-436C-A55B-0AF1A0883DC9<br/>                                                                                                                                                                                                                                                                                                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[Référence Connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

