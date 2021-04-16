---
title: MsRdpClient3a, classe
description: Contrôle client Microsoft RDP (redistribuable)-version 4a.
ms.assetid: F2E3D49F-B3F9-40EF-9B93-C87F55DB0352
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la classe MsRdpClient3a
- Services Bureau à distance de la classe MsRdpClient3a, Description
topic_type:
- apiref
api_name:
- MsRdpClient3a
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c316f1f96ff4ccc77014daea2467dda17a164259
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508414"
---
# <a name="msrdpclient3a-class"></a>MsRdpClient3a, classe

Contrôle client Microsoft RDP (redistribuable)-version 4a

Cette classe implémente les interfaces suivantes.

-   [**IMsRdpClient3**](imsrdpclient3.md)
-   [**IMsRdpClient2**](imsrdpclient2.md)
-   [**IMsRdpClient**](imsrdpclientshell2.md)
-   [**IMsTscAx**](imstscax-interface.md)
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
-   [**IMsTscAxEvents**](imstscaxevents-interface.md)
-   [**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)

**MsRdpClient3a** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MsRdpClient3a** possède ces méthodes.



| Méthode                                                                                      | Description                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Connecter**](imstscax-connect.md)                                                         | Établit une connexion à l’aide des propriétés actuellement définies sur le contrôle.<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | Crée un objet de canal virtuel côté client pour chaque nom de canal virtuel spécifié.<br/>                                                                                                                                                                                              |
| [**Déconnecter**](imstscax-disconnect.md)                                                   | Déconnecte la connexion active.<br/>                                                                                                                                                                                                                                                 |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)                   | Récupère les options définies pour un canal virtuel.<br/>                                                                                                                                                                                                                                   |
| [**NotifyRedirectDeviceChange**](imsrdpclientnonscriptable-notifyredirectdevicechange.md)  | Notifie le module de redirection de périphérique du contrôle ActiveX Bureau à distance qu’une modification de périphérique s’est produite sur le système. Cette méthode passe les notifications [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) au contrôle.<br/>                                                        |
| [**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md) | Appelé après qu’un contrôle ActiveX affiche une boîte de dialogue d’authentification (par exemple, la boîte de dialogue erreur de certificat).<br/>                                                                                                                                                             |
| [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) | Appelé avant qu’un contrôle ActiveX affiche une boîte de dialogue d’authentification (par exemple, la boîte de dialogue erreur de certificat).<br/>                                                                                                                                                            |
| [**OnAutoReconnected**](imstscaxevents-onautoreconnected.md)                               | Appelé lorsque le contrôle client se reconnecte automatiquement à une session à distance.<br/>                                                                                                                                                                                                  |
| [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md)                           | Appelée lorsqu’un client se trouve dans le processus de reconnexion automatique d’une session à un serveur hôte de session Bureau à distance.<br/>                                                                                                                                                                      |
| [**OnAutoReconnecting2**](imstscaxevents-onautoreconnecting2.md)                           | Appelée lorsqu’un client se trouve dans le processus de reconnexion automatique d’une session à un serveur hôte de session Bureau à distance.<br/>                                                                                                                                                                      |
| [**OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md)                       | Appelé lorsque le client reçoit des données sur un canal virtuel scriptable.<br/>                                                                                                                                                                                                              |
| [**OnConfirmClose**](imstscaxevents-onconfirmclose.md)                                     | Appelée lorsque le client appelle la méthode [**IMsRdpClient :: RequestClose**](imsrdpclient-requestclose.md) .<br/>                                                                                                                                                                           |
| [**OnConnected**](imstscaxevents-onconnected.md)                                           | Appelé lorsque le contrôle client est en train d’établir une connexion avec un serveur hôte de session Bureau à distance.<br/>                                                                                                                                                                       |
| [**OnConnecting**](imstscaxevents-onconnecting.md)                                         | Appelé lorsque le contrôle client commence à se connecter à un serveur en réponse à un appel à [**IMsTscAx :: Connect**](imstscax-connect.md).<br/>                                                                                                                                               |
| [**OnConnectionBarPullDown**](imstscaxevents-onconnectionbarpulldown.md)                   | Appelé lorsque l’utilisateur a fait glisser vers le dessous de la barre de connexion.<br/>                                                                                                                                                                                                                       |
| [**OnDevicesButtonPressed**](imstscaxevents-ondevicesbuttonpressed.md)                     | Appelé lorsque le bouton appareils de la barre de connexion a été enfoncé.<br/>                                                                                                                                                                                                             |
| [**OnDisconnected**](imstscaxevents-ondisconnected.md)                                     | Appelé lorsque le contrôle client a été déconnecté du serveur hôte de session Bureau à distance.<br/>                                                                                                                                                                                              |
| [**OnEnterFullScreenMode**](imstscaxevents-onenterfullscreenmode.md)                       | Appelé lorsque le client passe en mode plein écran. Par exemple, cet événement est appelé quand l’utilisateur appuie sur la combinaison de touches de [raccourci](terminal-services-shortcut-keys.md) du mode plein écran (Ctrl + Alt + Attn).<br/>                                                                     |
| [**OnFatalError**](imstscaxevents-onfatalerror.md)                                         | Appelé lorsque le contrôle client rencontre une erreur irrécupérable.<br/>                                                                                                                                                                                                                           |
| [**OnFocusReleased**](imstscaxevents-onfocusreleased.md)                                   | Appelé lorsque la combinaison de touches de focus de mise en sortie est enfoncée. Par exemple, cet événement est appelé quand l’utilisateur appuie sur la touche CTRL + ALT + gauche ou sur la combinaison de touches CTRL + ALT + flèche droite.<br/>                                                                                             |
| [**OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md)               | Appelé quand aucune entrée de souris ou de clavier n’a été effectuée par l’utilisateur pendant la période définie par la méthode [**IMsRdpClientAdvancedSettings ::p ut \_ MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) .<br/>                                                |
| [**OnLeaveFullScreenMode**](imstscaxevents-onleavefullscreenmode.md)                       | Appelé lorsque le client quitte le mode plein écran. Par exemple, cet événement est appelé quand l’utilisateur appuie sur la combinaison de touches de [raccourci](terminal-services-shortcut-keys.md) du mode plein écran (Ctrl + Alt + Attn).<br/>                                                                     |
| [**OnLoginComplete**](imstscaxevents-onlogincomplete.md)                                   | Appelé lorsque le contrôle client a réussi à se connecter à un serveur hôte de session Bureau à distance, en suivant l’affichage de la boîte de dialogue ouverture de session Windows.<br/>                                                                                                                                      |
| [**OnLogonError**](imstscaxevents-onlogonerror.md)                                         | Appelée lorsqu’une erreur d’ouverture de session ou un autre événement d’ouverture de session se produit.<br/>                                                                                                                                                                                                                             |
| [**OnMouseInputModeChanged**](imstscaxevents-onmouseinputmodechanged.md)                   | Appelé lorsque le mode d’entrée de la souris a changé.<br/>                                                                                                                                                                                                                                      |
| [**OnNetworkStatusChanged**](imstscaxevents-onnetworkstatuschanged.md)                     | Appelé lorsque l’état du réseau a changé.<br/>                                                                                                                                                                                                                                        |
| [**OnReceivedTSPublicKey**](imstscaxevents-onreceivedtspublickey.md)                       | Appelé pendant la séquence de connexion lorsque le client récupère la clé publique du serveur. Cet événement est appelé uniquement si la propriété **NotifyTSPublicKey** a **la \_ valeur variant true**.<br/>                                                                                              |
| [**OnRemoteDesktopSizeChange**](imstscaxevents-onremotedesktopsizechange.md)               | Appelé pour indiquer que la taille du contrôle client sur le Bureau à distance a changé en réponse à une opération de contrôle client.<br/>                                                                                                                                                |
| [**OnRemoteProgramDisplayed**](imstscaxevents-onremoteprogramdisplayed.md)                 | Appelé lorsqu’un programme RemoteApp est affiché.<br/>                                                                                                                                                                                                                                      |
| [**OnRemoteProgramResult**](imstscaxevents-onremoteprogramresult.md)                       | Appelée lorsqu’un programme RemoteApp retourne un résultat au contrôle client.<br/>                                                                                                                                                                                                            |
| [**OnRemoteWindowDisplayed**](imstscaxevents-onremotewindowdisplayed.md)                   | Appelé lorsqu’une fenêtre RemoteApp est affichée.<br/>                                                                                                                                                                                                                                       |
| [**OnRequestContainerMinimize**](imstscaxevents-onrequestcontainerminimize.md)             | Appelé lorsque l’utilisateur appuie sur le bouton **réduire** de la barre de connexion en mode plein écran. Le déclenchement de cet événement est une demande que l’application conteneur réduit.<br/>                                                                                              |
| [**OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md)                       | Appelée lorsque le client demande à basculer en mode plein écran et que la méthode [**IMsTscAdvancedSettings ::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) est appelée pour définir la propriété **ContainerHandledFullScreen** sur une valeur différente de zéro.<br/> |
| [**OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md)                 | Appelée lorsque le client demande à conserver le mode plein écran et que la propriété [**IMsTscAdvancedSettings ::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) a été définie sur une valeur différente de zéro.<br/>                                                   |
| [**OnServiceMessageReceived**](imstscaxevents-onservicemessagereceived.md)                 | Appelé lorsque le client reçoit un message système.<br/>                                                                                                                                                                                                                                  |
| [**OnUserNameAcquired**](imstscaxevents-onusernameacquired.md)                             | Appelée lorsque le nom d’utilisateur a été acquis par le contrôle.<br/>                                                                                                                                                                                                                        |
| [**OnWarning**](imstscaxevents-onwarning.md)                                               | Appelé lorsque le contrôle client rencontre une condition d’erreur qui n’est pas irrécupérable.<br/>                                                                                                                                                                                                    |
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | Demande un arrêt approprié du contrôle client.<br/>                                                                                                                                                                                                                                |
| [**ResetPassword**](imstscnonscriptable-resetpassword.md)                                  | Réinitialise tous les États de mot de passe dans le contrôle.<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | Envoie une série de séquences de touches au contrôle. Les séquences de touches sont sous forme de code d’analyse, c’est-à-dire les données de clavier des véritables clés physiques.<br/>                                                                                                                                       |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                               | Envoie des données au serveur hôte de session Bureau à distance via un canal virtuel qui a été créé précédemment à l’aide de la méthode [**IMsTscAx :: CreateVirtualChannels**](imstscax-createvirtualchannels.md) .<br/>                                                                                         |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)                   | Définit les options de canal virtuel pour le contrôle client.<br/>                                                                                                                                                                                                                           |



 

### <a name="properties"></a>Propriétés

La classe **MsRdpClient3a** possède les propriétés suivantes.



| Propriété                                                                             | Type d’accès           | Description                                                                                                                                                               |
|:-------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings**](imstscax-advancedsettings.md)<br/>                     | Lecture seule<br/>  | Pointeur d’interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .<br/>                                                                       |
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Lecture seule<br/>  | Pointeur vers l’interface [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) , utilisé pour définir des paramètres avancés pour le contrôle client.<br/> |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>              | Lecture seule<br/>  | Pointeur vers l’interface [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) , utilisé pour définir des paramètres avancés pour le contrôle client.<br/>         |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>              | Lecture seule<br/>  | Pointeur vers l’interface [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) , utilisé pour définir des paramètres avancés pour le contrôle client.<br/>         |
| [**BinaryPassword**](imstscnonscriptable-binarypassword.md)<br/>              | Lecture/écriture<br/> | Cette propriété n'est pas prise en charge.<br/>                                                                                                                                |
| [**BinarySalt**](imstscnonscriptable-binarysalt.md)<br/>                      | Lecture/écriture<br/> | Cette propriété n'est pas prise en charge.<br/>                                                                                                                                |
| [**CipherStrength**](imstscax-cipherstrength.md)<br/>                         | Lecture seule<br/>  | Force de chiffrement maximale du contrôle actuel.<br/>                                                                                                        |
| [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md)<br/>        | Écriture seule<br/> | Le mot de passe du contrôle ActiveX Bureau à distance, au format texte en clair.<br/>                                                                                              |
| [**La**](imsrdpclient-colordepth.md)<br/>                             | Lecture/écriture<br/> | Profondeur de couleur du contrôle actuel.<br/>                                                                                                                            |
| [**Connecté**](imstscax-connected.md)<br/>                                   | Lecture seule<br/>  | État de connexion du contrôle actuel.<br/>                                                                                                                   |
| [**ConnectedStatusText**](imsrdpclient2-connectedstatustext.md)<br/>          | Lecture/écriture<br/> | Texte affiché dans la zone cliente du contrôle pendant que le contrôle est dans l’état connecté.<br/>                                                          |
| [**ConnectingText**](imstscax-connectingtext.md)<br/>                         | Lecture/écriture<br/> | Texte qui apparaît centré dans le contrôle pendant la connexion du contrôle.<br/>                                                                                 |
| [**DesktopHeight**](imstscax-desktopheight.md)<br/>                           | Lecture/écriture<br/> | Hauteur du contrôle actuel, en pixels, sur le Bureau à distance initial.<br/>                                                                                        |
| [**DesktopWidth**](imstscax-desktopwidth.md)<br/>                             | Lecture/écriture<br/> | Largeur, en pixels, du contrôle actif sur le Bureau à distance initial.<br/>                                                                                         |
| [**DisconnectedText**](imstscax-disconnectedtext.md)<br/>                     | Lecture/écriture<br/> | Texte qui apparaît centré dans le contrôle avant qu’une connexion ne soit terminée.<br/>                                                                               |
| [**Domaine**](imstscax-domain.md)<br/>                                         | Lecture/écriture<br/> | Domaine sur lequel l’utilisateur actuel ouvre une session.<br/>                                                                                                                  |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | Lecture seule<br/>  | Informations étendues sur la raison de la déconnexion du contrôle client.<br/>                                                                                      |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                             | Lecture/écriture<br/> | Indique si le contrôle est en mode plein écran.<br/>                                                                                                          |
| [**FullScreenTitle**](imstscax-fullscreentitle.md)<br/>                       | Écriture seule<br/> | Titre de la fenêtre qui s’affiche lorsque le contrôle est en mode plein écran.<br/>                                                                                            |
| [**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)<br/> | Lecture seule<br/>  | Indique si le contrôle a affiché une barre de défilement horizontale.<br/>                                                                                           |
| [**PortablePassword**](imstscnonscriptable-portablepassword.md)<br/>          | Lecture/écriture<br/> | Cette propriété n'est pas prise en charge.<br/>                                                                                                                                |
| [**PortableSalt**](imstscnonscriptable-portablesalt.md)<br/>                  | Lecture/écriture<br/> | Cette propriété n'est pas prise en charge.<br/>                                                                                                                                |
| [**SecuredSettings**](imstscax-securedsettings.md)<br/>                       | Lecture seule<br/>  | Pointeur d’interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .<br/>                                                                          |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Lecture seule<br/>  | Pointeur vers l’interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) , utilisé pour définir des paramètres sécurisés pour le contrôle client.<br/>    |
| [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md)<br/>         | Lecture seule<br/>  | Indique si l’interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) est disponible.<br/>                                                 |
| [**Serveur**](imstscax-server.md)<br/>                                         | Lecture/écriture<br/> | Nom du serveur auquel le contrôle actuel est connecté.<br/>                                                                                              |
| [**StartConnected**](imstscax-startconnected.md)<br/>                         | Lecture/écriture<br/> | Indique si le contrôle établira la connexion au serveur hôte de session Bureau à distance dès le démarrage.<br/>                                                   |
| [**Nom d’utilisateur**](imstscax-username.md)<br/>                                     | Lecture/écriture<br/> | Informations d’identification d’ouverture de session de nom d’utilisateur.<br/>                                                                                                                                |
| [**Version**](imstscax-version.md)<br/>                                       | Lecture seule<br/>  | Numéro de version du contrôle actuel.<br/>                                                                                                                     |
| [**VerticalScrollBarVisible**](imstscax-verticalscrollbarvisible.md)<br/>     | Lecture seule<br/>  | Indique si le contrôle affiche une barre de défilement verticale.<br/>                                                                                                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| CLSID<br/>                    | Le CLSID \_ MsRdpClient3a est défini en tant que 6A6F4B83-45C5-4CA9-BDD9-0D81C12295E4<br/>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes de contrôles ActiveX Bureau à distance](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

