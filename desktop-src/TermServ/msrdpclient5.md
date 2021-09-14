---
title: MsRdpClient5, classe
description: Contrôle client Microsoft RDP (redistribuable)-version 6.
ms.assetid: 30DC49A8-A9B1-4F74-B578-5761FA0C1315
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la classe MsRdpClient5
- Services Bureau à distance de la classe MsRdpClient5, Description
topic_type:
- apiref
api_name:
- MsRdpClient5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca53765f137e524f1605cdc0bbcabadbc12e89da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919716"
---
# <a name="msrdpclient5-class"></a>MsRdpClient5, classe

Contrôle client Microsoft RDP (redistribuable)-version 6

Cette classe implémente les interfaces suivantes.

-   [**IMsRdpClient5**](imsrdpclient5.md)
-   [**IMsRdpClient4**](imsrdpclient4.md)
-   [**IMsRdpClient3**](imsrdpclient3.md)
-   [**IMsRdpClient2**](imsrdpclient2.md)
-   [**IMsRdpClient**](imsrdpclientshell2.md)
-   [**IMsTscAx**](imstscax-interface.md)
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
-   [**IMsTscAxEvents**](imstscaxevents-interface.md)
-   [**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
-   [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)

**MsRdpClient5** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MsRdpClient5** possède ces méthodes.



| Méthode                                                                                      | Description                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Connecter**](imstscax-connect.md)                                                         | Établit une connexion à l’aide des propriétés actuellement définies sur le contrôle.<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | Crée un objet de canal virtuel côté client pour chaque nom de canal virtuel spécifié.<br/>                                                                                                                                                                                              |
| [**Déconnecter**](imstscax-disconnect.md)                                                   | Déconnecte la connexion active.<br/>                                                                                                                                                                                                                                                 |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                            | Récupère les codes d’erreur et les messages d’erreur.<br/>                                                                                                                                                                                                                                      |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)                   | Récupère les options définies pour un canal virtuel.<br/>                                                                                                                                                                                                                                   |
| [**NotifyRedirectDeviceChange**](imsrdpclientnonscriptable-notifyredirectdevicechange.md)  | notifie le module de redirection de l’appareil du contrôle de Bureau à distance ActiveX qu’une modification de l’appareil s’est produite sur le système. Cette méthode passe les notifications [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) au contrôle.<br/>                                                        |
| [**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md) | appelé après qu’un contrôle ActiveX affiche une boîte de dialogue d’authentification (par exemple, la boîte de dialogue erreur de certificat).<br/>                                                                                                                                                             |
| [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) | appelé avant qu’un contrôle ActiveX affiche une boîte de dialogue d’authentification (par exemple, la boîte de dialogue erreur de certificat).<br/>                                                                                                                                                            |
| [**OnAutoReconnected**](imstscaxevents-onautoreconnected.md)                               | Appelé lorsque le contrôle client se reconnecte automatiquement à une session à distance.<br/>                                                                                                                                                                                                  |
| [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md)                           | Appelée lorsqu’un client se trouve dans le processus de reconnexion automatique d’une session à un serveur hôte de session Bureau à distance.<br/>                                                                                                                                                                      |
| [**OnAutoReconnecting2**](imstscaxevents-onautoreconnecting2.md)                           | Appelée lorsqu’un client se trouve dans le processus de reconnexion automatique d’une session à un serveur hôte de session Bureau à distance.<br/>                                                                                                                                                                      |
| [**OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md)                       | Appelé lorsque le client reçoit des données sur un canal virtuel scriptable.<br/>                                                                                                                                                                                                              |
| [**OnConfirmClose**](imstscaxevents-onconfirmclose.md)                                     | Appelée lorsque le client appelle la méthode [**IMsRdpClient :: RequestClose**](imsrdpclient-requestclose.md) .<br/>                                                                                                                                                                           |
| [**OnConnected**](imstscaxevents-onconnected.md)                                           | Appelé lorsque le contrôle client est en train d’établir une connexion avec un serveur hôte de session Bureau à distance.<br/>                                                                                                                                                                       |
| [**OnConnecting**](imstscaxevents-onconnecting.md)                                         | Appelé lorsque le contrôle client commence à se connecter à un serveur en réponse à un appel à [**IMsTscAx :: connecter**](imstscax-connect.md).<br/>                                                                                                                                               |
| [**OnConnectionBarPullDown**](imstscaxevents-onconnectionbarpulldown.md)                   | Appelé lorsque l’utilisateur a fait glisser vers le dessous de la barre de connexion.<br/>                                                                                                                                                                                                                       |
| [**OnDevicesButtonPressed**](imstscaxevents-ondevicesbuttonpressed.md)                     | Appelé lorsque le bouton appareils de la barre de connexion a été enfoncé.<br/>                                                                                                                                                                                                             |
| [**OnDisconnected**](imstscaxevents-ondisconnected.md)                                     | Appelé lorsque le contrôle client a été déconnecté du serveur hôte de session Bureau à distance.<br/>                                                                                                                                                                                              |
| [**OnEnterFullScreenMode**](imstscaxevents-onenterfullscreenmode.md)                       | Appelé lorsque le client passe en mode plein écran. Par exemple, cet événement est appelé quand l’utilisateur appuie sur la combinaison de touches de [raccourci](terminal-services-shortcut-keys.md) du mode plein écran (Ctrl + Alt + Attn).<br/>                                                                     |
| [**OnFatalError**](imstscaxevents-onfatalerror.md)                                         | Appelé lorsque le contrôle client rencontre une erreur irrécupérable.<br/>                                                                                                                                                                                                                           |
| [**OnFocusReleased**](imstscaxevents-onfocusreleased.md)                                   | Appelé lorsque la combinaison de touches de focus de mise en sortie est enfoncée. Par exemple, cet événement est appelé quand l’utilisateur appuie sur la touche CTRL + ALT + gauche ou sur la combinaison de touches CTRL + ALT + flèche droite.<br/>                                                                                             |
| [**OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md)               | Appelé quand aucune entrée de souris ou de clavier n’a été effectuée par l’utilisateur pendant la période définie par la méthode [**IMsRdpClientAdvancedSettings ::p ut \_ MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) .<br/>                                                |
| [**OnLeaveFullScreenMode**](imstscaxevents-onleavefullscreenmode.md)                       | Appelé lorsque le client quitte le mode plein écran. Par exemple, cet événement est appelé quand l’utilisateur appuie sur la combinaison de touches de [raccourci](terminal-services-shortcut-keys.md) du mode plein écran (Ctrl + Alt + Attn).<br/>                                                                     |
| [**OnLoginComplete**](imstscaxevents-onlogincomplete.md)                                   | appelé lorsque le contrôle client a réussi à se connecter à un serveur hôte de Session bureau à distance, en suivant l’affichage de la boîte de dialogue Windows Logon.<br/>                                                                                                                                      |
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

La classe **MsRdpClient5** possède les propriétés suivantes.




| Propriété | Type d’accès | Description | 
|----------|-------------|-------------|
| <a href="imstscax-advancedsettings.md"><strong>AdvancedSettings</strong></a><br /> | Lecture seule<br /> | Pointeur d’interface <a href="imstscadvancedsettings-interface.md"><strong>IMsTscAdvancedSettings</strong></a> .<br /> | 
| <a href="imsrdpclient-advancedsettings2.md"><strong>AdvancedSettings2</strong></a><br /> | Lecture seule<br /> | Pointeur vers l’interface <a href="imsrdpclientadvancedsettings-interface.md"><strong>IMsRdpClientAdvancedSettings</strong></a> , utilisé pour définir des paramètres avancés pour le contrôle client.<br /> | 
| <a href="imsrdpclient2-advancedsettings3.md"><strong>AdvancedSettings3</strong></a><br /> | Lecture seule<br /> | Pointeur vers l’interface <a href="imsrdpclientadvancedsettings2.md"><strong>IMsRdpClientAdvancedSettings2</strong></a> , utilisé pour définir des paramètres avancés pour le contrôle client.<br /> | 
| <a href="imsrdpclient3-advancedsettings4.md"><strong>AdvancedSettings4</strong></a><br /> | Lecture seule<br /> | Pointeur vers l’interface <a href="imsrdpclientadvancedsettings3.md"><strong>IMsRdpClientAdvancedSettings3</strong></a> , utilisé pour définir des paramètres avancés pour le contrôle client.<br /> | 
| <a href="imsrdpclient4-advancedsettings5.md"><strong>AdvancedSettings5</strong></a><br /> | Lecture seule<br /> | Pointeur d’interface <a href="imsrdpclientadvancedsettings4.md"><strong>IMsRdpClientAdvancedSettings4</strong></a> .<br /> | 
| <a href="imsrdpclient5-advancedsettings6.md"><strong>AdvancedSettings6</strong></a><br /> | Lecture seule<br /> | Interface à <a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5</strong></a>.<br /> | 
| <a href="imstscnonscriptable-binarypassword.md"><strong>BinaryPassword</strong></a><br /> | Lecture/écriture<br /> | Cette propriété n'est pas prise en charge.<br /> | 
| <a href="imstscnonscriptable-binarysalt.md"><strong>BinarySalt</strong></a><br /> | Lecture/écriture<br /> | Cette propriété n'est pas prise en charge.<br /> | 
| <a href="imstscax-cipherstrength.md"><strong>CipherStrength</strong></a><br /> | Lecture seule<br /> | Force de chiffrement maximale du contrôle actuel.<br /> | 
| <a href="imstscnonscriptable-cleartextpassword.md"><strong>ClearTextPassword</strong></a><br /> | Écriture seule<br /> | Bureau à distance ActiveX mot de passe de contrôle, au format texte en clair.<br /> | 
| <a href="imsrdpclient-colordepth.md"><strong>La</strong></a><br /> | Lecture/écriture<br /> | Profondeur de couleur du contrôle actuel.<br /> | 
| <a href="imstscax-connected.md"><strong>Correctement</strong></a><br /> | Lecture seule<br /> | État de connexion du contrôle actuel.<br /> | 
| <a href="imsrdpclient2-connectedstatustext.md"><strong>ConnectedStatusText</strong></a><br /> | Lecture/écriture<br /> | Texte affiché dans la zone cliente du contrôle pendant que le contrôle est dans l’état connecté.<br /> | 
| <a href="imstscax-connectingtext.md"><strong>ConnectingText</strong></a><br /> | Lecture/écriture<br /> | Texte qui apparaît centré dans le contrôle pendant la connexion du contrôle.<br /> | 
| <a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a><br /> | Lecture/écriture<br /> | Chaîne de texte à afficher pour la barre de connexion.<br /> | 
| <a href="imstscax-desktopheight.md"><strong>DesktopHeight</strong></a><br /> | Lecture/écriture<br /> | Hauteur du contrôle actuel, en pixels, sur le Bureau à distance initial.<br /> | 
| <a href="imstscax-desktopwidth.md"><strong>DesktopWidth</strong></a><br /> | Lecture/écriture<br /> | Largeur, en pixels, du contrôle actif sur le Bureau à distance initial.<br /> | 
| <a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>DeviceCollection</strong></a><br /> | Lecture seule<br /> | Collection des périphériques PnP disponibles pour la redirection.<br /> | 
| <a href="imstscax-disconnectedtext.md"><strong>DisconnectedText</strong></a><br /> | Lecture/écriture<br /> | Texte qui apparaît centré dans le contrôle avant qu’une connexion ne soit terminée.<br /> | 
| <a href="imstscax-domain.md"><strong>Domain</strong></a><br /> | Lecture/écriture<br /> | Domaine sur lequel l’utilisateur actuel ouvre une session.<br /> | 
| <a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a><br /> | Lecture seule<br /> | Collection de lecteurs de disque disponibles pour la redirection.<br /> | 
| <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a><br /> | Lecture/écriture<br /> | Spécifie si CredSSP est activé pour cette connexion.<br /> | 
| <a href="imsrdpclient-extendeddisconnectreason.md"><strong>ExtendedDisconnectReason</strong></a><br /> | Lecture seule<br /> | Informations étendues sur la raison de la déconnexion du contrôle client.<br /> | 
| <a href="imsrdpclient-fullscreen.md"><strong>Large</strong></a><br /> | Lecture/écriture<br /> | Indique si le contrôle est en mode plein écran.<br /> | 
| <a href="imstscax-fullscreentitle.md"><strong>FullScreenTitle</strong></a><br /> | Écriture seule<br /> | Titre de la fenêtre qui s’affiche lorsque le contrôle est en mode plein écran.<br /> | 
| <a href="imstscax-horizontalscrollbarvisible.md"><strong>HorizontalScrollBarVisible</strong></a><br /> | Lecture seule<br /> | Indique si le contrôle a affiché une barre de défilement horizontale.<br /> | 
| <a href="imsrdpclient5-msrdpclientshell.md"><strong>MsRdpClientShell</strong></a><br /> | Lecture seule<br /> | Paramètres client pour le lanceur du portail Web.<br /> | 
| <a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a><br /> | Lecture/écriture<br /> | Spécifie si le paramètre NegotiateSecurityLayer est pris en charge pour cette connexion.<br /><blockquote>[!Note]<br />Lorsque <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> est activé et présent sur le client, ou lorsque SSL (Secure Sockets Layer) (SSL) est activé avec l’authentification utilisateur, NegotiateSecurityLayer est ignoré.</blockquote><br /> | 
| <a href="imstscnonscriptable-portablepassword.md"><strong>PortablePassword</strong></a><br /> | Lecture/écriture<br /> | Cette propriété n'est pas prise en charge.<br /> | 
| <a href="imstscnonscriptable-portablesalt.md"><strong>PortableSalt</strong></a><br /> | Lecture/écriture<br /> | Cette propriété n'est pas prise en charge.<br /> | 
| <a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a><br /> | Lecture/écriture<br /> | Spécifie si la boîte de dialogue demander les informations d’identification doit s’afficher.<br /> | 
| <a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a><br /> | Lecture/écriture<br /> | Spécifie si les appareils PnP attachés de manière dynamique et qui sont énumérés dans une session sont disponibles pour la redirection.<br /> | 
| <a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a><br /> | Lecture/écriture<br /> | Spécifie si les lecteurs PnP attachés de manière dynamique et qui sont énumérés dans une session sont disponibles pour la redirection.<br /> | 
| <a href="imsrdpclient5-remoteprogram.md"><strong>RemoteProgram</strong></a><br /> | Lecture seule<br /> | Paramètre RemoteApp du client.<br /> | 
| <a href="imstscax-securedsettings.md"><strong>SecuredSettings</strong></a><br /> | Lecture seule<br /> | Pointeur d’interface <a href="imstscsecuredsettings-interface.md"><strong>IMsTscSecuredSettings</strong></a> .<br /> | 
| <a href="imsrdpclient-securedsettings2.md"><strong>SecuredSettings2</strong></a><br /> | Lecture seule<br /> | Pointeur vers l’interface <a href="imsrdpclientsecuredsettings-interface.md"><strong>IMsRdpClientSecuredSettings</strong></a> , utilisé pour définir des paramètres sécurisés pour le contrôle client.<br /> | 
| <a href="imstscax-securedsettingsenabled.md"><strong>SecuredSettingsEnabled</strong></a><br /> | Lecture seule<br /> | Indique si l’interface <a href="imstscsecuredsettings-interface.md"><strong>IMsTscSecuredSettings</strong></a> est disponible.<br /> | 
| <a href="imstscax-server.md"><strong>Serveurs</strong></a><br /> | Lecture/écriture<br /> | Nom du serveur auquel le contrôle actuel est connecté.<br /> | 
| <a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a><br /> | Lecture/écriture<br /> | Spécifie si la boîte de dialogue Avertissement de sécurité de redirection doit s’afficher avant le démarrage d’une session.<br /> | 
| <a href="imstscax-startconnected.md"><strong>StartConnected</strong></a><br /> | Lecture/écriture<br /> | Indique si le contrôle établira la connexion au serveur hôte de session Bureau à distance dès le démarrage.<br /> | 
| <a href="imsrdpclient5-transportsettings.md"><strong>TransportSettings</strong></a><br /> | Lecture seule<br /> | Paramètre de la passerelle des services Bureau à distance du client.<br /> | 
| <a href="imsrdpclientnonscriptable2-uiparentwindowhandle.md"><strong>UIParentWindowHandle</strong></a><br /> | Lecture/écriture<br /> | Handle de fenêtre qui doit être la fenêtre parente pour le contrôle. Cela permet aux fenêtres affichées par le contrôle d’être correctement modales par rapport à toutes les fenêtres affichées par l’application parente.<br /> | 
| <a href="imstscax-username.md"><strong>Nom d’utilisateur</strong></a><br /> | Lecture/écriture<br /> | Informations d’identification d’ouverture de session de nom d’utilisateur.<br /> | 
| <a href="imstscax-version.md"><strong>Version</strong></a><br /> | Lecture seule<br /> | Numéro de version du contrôle actuel.<br /> | 
| <a href="imstscax-verticalscrollbarvisible.md"><strong>VerticalScrollBarVisible</strong></a><br /> | Lecture seule<br /> | Indique si le contrôle affiche une barre de défilement verticale.<br /> | 
| <a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a><br /> | Lecture/écriture<br /> | Spécifie si la boîte de dialogue d’avertissement de sécurité doit inclure un avertissement sur la redirection du presse-papiers avant de démarrer une session.<br /> | 
| <a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a><br /> | Lecture/écriture<br /> | Spécifie si l’avertissement de sécurité doit inclure un avertissement concernant l’envoi d’informations d’identification au serveur distant avant le démarrage d’une session.<br /> | 




 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| CLSID<br/>                    | Le CLSID \_ MsRdpClient5 est défini en tant que 4EB89FF4-7f78-4A0F-8B8D-2BF02E94E4B2<br/>      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Bureau à distance ActiveX les classes de contrôle](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

