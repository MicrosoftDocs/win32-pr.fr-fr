---
title: Interface IMsRdpClient10
description: Fournit les méthodes et les propriétés nécessaires à la configuration et à l’utilisation du contrôle client. Dérive de l’interface IMsRdpClient9.
ms.assetid: 601f70aa-85f1-4180-921b-9f1bb31d4def
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, Description
topic_type:
- apiref
api_name:
- IMsRdpClient10
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 561541f170fbe6dc5342b359e5deae69d0c92469ad2d692ee4ea3b9d59904885
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737239"
---
# <a name="imsrdpclient10-interface"></a>Interface IMsRdpClient10

Fournit les méthodes et les propriétés nécessaires à la configuration et à l’utilisation du contrôle client. Dérive de l’interface [**IMsRdpClient9**](imsrdpclient9.md) .

## <a name="members"></a>Membres

L’interface **IMsRdpClient10** hérite de [**IMsRdpClient9**](imsrdpclient9.md). **IMsRdpClient10** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IMsRdpClient10** possède ces méthodes.



| Méthode                                                                             | Description                                                                         |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**attachEvent**](imsrdpclient9-attachevent.md)                                   | Joint un événement.<br/>                                                       |
| [**detachEvent**](imsrdpclient9-detachevent.md)                                   | Détache un événement.<br/>                                                       |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                   | Récupère la description de l’erreur pour les événements de déconnexion de la session.<br/>       |
| [**GetStatusText**](imsrdpclient7-getstatustext.md)                               | Récupère le texte d’État pour le code d’état spécifié.<br/>                 |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)          | Récupère les options définies pour un canal virtuel.<br/>                         |
| [**Reconnexion**](imsrdpclient8-reconnect.md)                                       | Se reconnecte à la session à distance avec la largeur et la hauteur du nouveau bureau.<br/>  |
| [**RequestClose**](imsrdpclient-requestclose.md)                                  | demande un arrêt approprié du contrôle de Bureau à distance ActiveX.<br/>      |
| [**SendRemoteAction**](imsrdpclient8-sendremoteaction.md)                         | Entraîne l’exécution d’une action dans la session à distance.<br/>                  |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)          | définit les options de canal virtuel pour le contrôle de ActiveX Bureau à distance.<br/> |
| [**SyncSessionDisplaySettings**](imsrdpclient9-syncsessiondisplaysettings.md)     | Synchronise les paramètres d’affichage de la session.<br/>                                   |
| [**UpdateSessionDisplaySettings**](/previous-versions/windows/desktop/legacy/mt703457(v=vs.85)) | Met à jour les paramètres d’affichage de la session.<br/>                                        |



 

### <a name="properties"></a>Propriétés

L’interface **IMsRdpClient10** possède les propriétés suivantes.



| Propriété                                                                             | Type d’accès           | Description                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Lecture seule<br/>  | Récupère un pointeur vers l’interface [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) . L’interface peut être utilisée pour définir des paramètres avancés pour le contrôle client.<br/> |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>              | Lecture seule<br/>  | Récupère un pointeur vers l’interface [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) . L’interface peut être utilisée pour définir des paramètres avancés pour le contrôle client.<br/>         |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>              | Lecture seule<br/>  | Récupère un pointeur vers l’interface [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .<br/>                                                                                    |
| [**AdvancedSettings5**](imsrdpclient4-advancedsettings5.md)<br/>              | Lecture seule<br/>  | Récupère un pointeur vers une interface [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .<br/>                                                                                     |
| [**AdvancedSettings6**](imsrdpclient5-advancedsettings6.md)<br/>              | Lecture seule<br/>  | Récupère l’interface [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) .<br/>                                                                                                 |
| [**AdvancedSettings7**](imsrdpclient6-advancedsettings7.md)<br/>              | Lecture seule<br/>  | Récupère l’interface [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) .<br/>                                                                                                 |
| [**AdvancedSettings8**](imsrdpclient7-advancedsettings8.md)<br/>              | Lecture seule<br/>  | Récupère un objet qui prend en charge l’interface [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) .<br/>                                                                         |
| [**AdvancedSettings9**](imsrdpclient8-advancedsettings9.md)<br/>              | Lecture seule<br/>  | Contient un objet qui prend en charge l’interface [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) .<br/>                                                                          |
| [**La**](imsrdpclient-colordepth.md)<br/>                             | Lecture/écriture<br/> | Profondeur de couleur (en bits par pixel) de la connexion du contrôle.<br/>                                                                                                                               |
| [**ConnectedStatusText**](imsrdpclient2-connectedstatustext.md)<br/>          | Lecture/écriture<br/> | Contient le texte affiché dans la zone cliente du contrôle pendant que le contrôle est dans l’état connecté.<br/>                                                                              |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | Lecture seule<br/>  | Contient des informations étendues sur la raison de la déconnexion du contrôle.<br/>                                                                                                                     |
| [**Large**](imsrdpclient-fullscreen.md)<br/>                             | Lecture/écriture<br/> | Détermine si le contrôle client est en mode plein écran.<br/>                                                                                                                                   |
| [**MsRdpClientShell**](imsrdpclient5-msrdpclientshell.md)<br/>                | Lecture seule<br/>  | Récupère l’interface de paramètre client scriptable [**IMsRdpClientShell**](imsrdpclientshell.md).<br/>                                                                                               |
| [**RemoteProgram**](imsrdpclient5-remoteprogram.md)<br/>                      | Lecture seule<br/>  | Récupère un objet qui prend en charge l’interface [**ITSRemoteProgram**](itsremoteprogram.md) .<br/>                                                                                                   |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>                    | Lecture seule<br/>  | Récupère un objet qui prend en charge l’interface [**ITSRemoteProgram2**](itsremoteprogram2.md) .<br/>                                                                                                 |
| [**RemoteProgram3**](imsrdpclient10-remoteprogram3.md)<br/>                   | Lecture seule<br/>  | Objet qui prend en charge l’interface [**ITSRemoteProgram3**](itsremoteprogram3.md) .<br/>                                                                                                           |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Lecture seule<br/>  | Récupère un pointeur vers l’interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) . Cette interface peut être utilisée pour définir des paramètres sécurisés pour le contrôle client.<br/>   |
| [**SecuredSettings3**](imsrdpclient7-securedsettings3.md)<br/>                | Lecture seule<br/>  | Récupère un objet qui prend en charge l’interface [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) .<br/>                                                                           |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/>              | Lecture seule<br/>  | Récupère ce qui a été passé via un script à l’interface [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) .<br/>                                                             |
| [**TransportSettings2**](imsrdpclient6-transportsettings2.md)<br/>            | Lecture seule<br/>  | Récupère l’interface [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) .<br/>                                                                                               |
| [**TransportSettings3**](imsrdpclient7-transportsettings3.md)<br/>            | Lecture seule<br/>  | Récupère un objet qui prend en charge l’interface [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) .<br/>                                                                       |
| [**TransportSettings4**](imsrdpclient9-transportsettings4.md)<br/>            | Lecture seule<br/>  | Récupère un objet qui prend en charge l’interface [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) .<br/>                                                                       |



 

## <a name="remarks"></a>Remarques

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                                                                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                                                                                                           |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                   |
| CLSID<br/>                    | Le CLSID \_ MsRdpClient10 est défini en tant que C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> Le CLSID \_ MsRdpClient10NotSafeForScripting est défini en tant que A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> |
| IID<br/>                      | IID \_ IMsRdpClient10 est défini en tant que 7ED92C39-EB38-4927-A70A-708AC5A59321<br/>                                                                                                        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

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

 

