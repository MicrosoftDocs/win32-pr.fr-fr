---
title: MsRdpClient9NotSafeForScripting, classe
description: Contrôle client Microsoft RDP-version 10.
ms.assetid: 6F782984-1A17-449E-958F-EF887C340C49
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la classe MsRdpClient9NotSafeForScripting
- Services Bureau à distance de la classe MsRdpClient9NotSafeForScripting, Description
topic_type:
- apiref
api_name:
- MsRdpClient9NotSafeForScripting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55c87511a25115d11e7e49c4551d09451ec55910ce077be5703fb323d0d77ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988899"
---
# <a name="msrdpclient9notsafeforscripting-class"></a>MsRdpClient9NotSafeForScripting, classe

Contrôle client Microsoft RDP-version 10

Cette classe implémente les interfaces suivantes.

-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient6**](imsrdpclient6.md)
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
-   [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
-   [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
-   [**IMsRdpPreferredRedirectionInfo**](imsrdppreferredredirectioninfo.md)
-   [**IMsRdpExtendedSettings**](imsrdpextendedsettings.md)

**MsRdpClient9NotSafeForScripting** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MsRdpClient9NotSafeForScripting** possède ces méthodes.



| Méthode                                                                                      | Description                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attachEvent**](imsrdpclient9-attachevent.md)                                            | Joint un événement. <br/>                                                                                                                                                                                                                                                                |
| [**Connecter**](imstscax-connect.md)                                                         | Établit une connexion à l’aide des propriétés actuellement définies sur le contrôle.<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | Crée un objet de canal virtuel côté client pour chaque nom de canal virtuel spécifié.<br/>                                                                                                                                                                                              |
| [**detachEvent**](imsrdpclient9-detachevent.md)                                            | Détache un événement. <br/>                                                                                                                                                                                                                                                                |
| [**Déconnecter**](imstscax-disconnect.md)                                                   | Déconnecte la connexion active.<br/>                                                                                                                                                                                                                                                 |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                            | Récupère les codes d’erreur et les messages d’erreur.<br/>                                                                                                                                                                                                                                      |
| [**GetStatusText**](imsrdpclient7-getstatustext.md)                                        | Récupère le texte d’État pour le code d’état spécifié.<br/>                                                                                                                                                                                                                           |
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
| [**Reconnexion**](imsrdpclient8-reconnect.md)                                                | Se reconnecte à la session à distance avec la largeur et la hauteur du nouveau bureau.<br/>                                                                                                                                                                                                            |
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | Demande un arrêt approprié du contrôle client.<br/>                                                                                                                                                                                                                                |
| [**ResetPassword**](imstscnonscriptable-resetpassword.md)                                  | Réinitialise tous les États de mot de passe dans le contrôle.<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | Envoie une série de séquences de touches au contrôle. Les séquences de touches sont sous forme de code d’analyse, c’est-à-dire les données de clavier des véritables clés physiques.<br/>                                                                                                                                       |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                               | Envoie des données au serveur hôte de session Bureau à distance via un canal virtuel qui a été créé précédemment à l’aide de la méthode [**IMsTscAx :: CreateVirtualChannels**](imstscax-createvirtualchannels.md) .<br/>                                                                                         |
| [**SendRemoteAction**](imsrdpclient8-sendremoteaction.md)                                  | Entraîne l’exécution d’une action dans la session à distance.<br/>                                                                                                                                                                                                                            |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)                   | Définit les options de canal virtuel pour le contrôle client.<br/>                                                                                                                                                                                                                           |
| [**SyncSessionDisplaySettings**](imsrdpclient9-syncsessiondisplaysettings.md)              | Synchronise les paramètres d’affichage de la session. <br/>                                                                                                                                                                                                                                            |
| [**UpdateSessionDisplaySettings**](/previous-versions/windows/desktop/legacy/mt703457(v=vs.85))          | Met à jour les paramètres d’affichage de la session. <br/>                                                                                                                                                                                                                                                 |



 

### <a name="properties"></a>Propriétés

La classe **MsRdpClient9NotSafeForScripting** possède les propriétés suivantes.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Propriété</th>
<th style="text-align: left;">Type d’accès</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-advancedsettings.md"><strong>AdvancedSettings</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Pointeur d’interface <a href="imstscadvancedsettings-interface.md"><strong>IMsTscAdvancedSettings</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-advancedsettings2.md"><strong>AdvancedSettings2</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Pointeur vers l’interface <a href="imsrdpclientadvancedsettings-interface.md"><strong>IMsRdpClientAdvancedSettings</strong></a> , utilisé pour définir des paramètres avancés pour le contrôle client.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient2-advancedsettings3.md"><strong>AdvancedSettings3</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Pointeur vers l’interface <a href="imsrdpclientadvancedsettings2.md"><strong>IMsRdpClientAdvancedSettings2</strong></a> , utilisé pour définir des paramètres avancés pour le contrôle client.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient3-advancedsettings4.md"><strong>AdvancedSettings4</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Pointeur vers l’interface <a href="imsrdpclientadvancedsettings3.md"><strong>IMsRdpClientAdvancedSettings3</strong></a> , utilisé pour définir des paramètres avancés pour le contrôle client.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient4-advancedsettings5.md"><strong>AdvancedSettings5</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Pointeur d’interface <a href="imsrdpclientadvancedsettings4.md"><strong>IMsRdpClientAdvancedSettings4</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient5-advancedsettings6.md"><strong>AdvancedSettings6</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Interface à <a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient6-advancedsettings7.md"><strong>AdvancedSettings7</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Interface à <a href="imsrdpclientadvancedsettings6.md"><strong>IMsRdpClientAdvancedSettings6</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient7-advancedsettings8.md"><strong>AdvancedSettings8</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Objet qui prend en charge l’interface <a href="imsrdpclientadvancedsettings7.md"><strong>IMsRdpClientAdvancedSettings7</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient8-advancedsettings9.md"><strong>AdvancedSettings9</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Interface <a href="imsrdpclientadvancedsettings8.md"><strong>IMsRdpClientAdvancedSettings8</strong></a> qui représente l’objet de paramètres.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-allowcredentialsaving.md"><strong>AllowCredentialSaving</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si la boîte de dialogue informations d’identification affiche une case à cocher pour activer l’enregistrement des informations d’identification.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-allowpromptingforcredentials.md"><strong>AllowPromptingForCredentials</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">spécifie si le contrôle de ActiveX Bureau à distance peut inviter l’utilisateur à fournir des informations d’identification.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscnonscriptable-binarypassword.md"><strong>BinaryPassword</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Cette propriété n'est pas prise en charge.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscnonscriptable-binarysalt.md"><strong>BinarySalt</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Cette propriété n'est pas prise en charge.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-cipherstrength.md"><strong>CipherStrength</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Force de chiffrement maximale du contrôle actuel.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscnonscriptable-cleartextpassword.md"><strong>ClearTextPassword</strong></a><br/></td>
<td style="text-align: left;">Écriture seule<br/></td>
<td style="text-align: left;">Bureau à distance ActiveX mot de passe de contrôle, au format texte en clair.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-colordepth.md"><strong>La</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Profondeur de couleur du contrôle actuel.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-connected.md"><strong>Connecté</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">État de connexion du contrôle actuel.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient2-connectedstatustext.md"><strong>ConnectedStatusText</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Texte affiché dans la zone cliente du contrôle pendant que le contrôle est dans l’état connecté.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-connectingtext.md"><strong>ConnectingText</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Texte qui apparaît centré dans le contrôle pendant la connexion du contrôle.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Chaîne de texte à afficher pour la barre de connexion.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-desktopheight.md"><strong>DesktopHeight</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Hauteur du contrôle actuel, en pixels, sur le Bureau à distance initial.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-desktopwidth.md"><strong>DesktopWidth</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Largeur, en pixels, du contrôle actif sur le Bureau à distance initial.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>DeviceCollection</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Collection des périphériques PnP disponibles pour la redirection.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-disableconnectionbar.md"><strong>DisableConnectionBar</strong></a><br/></td>
<td style="text-align: left;">Écriture seule<br/></td>
<td style="text-align: left;">spécifie si le contrôle de ActiveX Bureau à distance doit désactiver la barre de connexion.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-disableremoteappcapscheck.md"><strong>DisableRemoteAppCapsCheck</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">spécifie si le contrôle de ActiveX Bureau à distance ne doit pas vérifier les fonctionnalités RemoteApp du serveur.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-disconnectedtext.md"><strong>DisconnectedText</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Texte qui apparaît centré dans le contrôle avant qu’une connexion ne soit terminée.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-domain.md"><strong>Domaine</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Domaine sur lequel l’utilisateur actuel ouvre une session.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Collection de lecteurs de disque disponibles pour la redirection.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si CredSSP est activé pour cette connexion.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-extendeddisconnectreason.md"><strong>ExtendedDisconnectReason</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Informations étendues sur la raison de la déconnexion du contrôle client.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient-fullscreen.md"><strong>Large</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Indique si le contrôle est en mode plein écran.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-fullscreentitle.md"><strong>FullScreenTitle</strong></a><br/></td>
<td style="text-align: left;">Écriture seule<br/></td>
<td style="text-align: left;">Titre de la fenêtre qui s’affiche lorsque le contrôle est en mode plein écran.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-getremotemonitorsboundingbox.md"><strong>GetRemoteMonitorsBoundingBox</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Spécifie le rectangle englobant du moniteur distant.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-horizontalscrollbarvisible.md"><strong>HorizontalScrollBarVisible</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Indique si le contrôle a affiché une barre de défilement horizontale.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-launchedviaclientshellinterface.md"><strong>LaunchedViaClientShellInterface</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si l’utilisateur a lancé le contrôle client à l’aide de l’interface de Accès web des services Bureau à distance.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-markrdpsettingssecure.md"><strong>MarkRdpSettingsSecure</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si les paramètres RDP sont marqués comme sécurisés.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient5-msrdpclientshell.md"><strong>MsRdpClientShell</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Paramètres client pour le lanceur du portail Web.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si le paramètre NegotiateSecurityLayer est pris en charge pour cette connexion.<br/>
<blockquote>
[!Note]<br />
Lorsque <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> est activé et présent sur le client, ou lorsque SSL (Secure Sockets Layer) (SSL) est activé avec l’authentification utilisateur, NegotiateSecurityLayer est ignoré.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscnonscriptable-portablepassword.md"><strong>PortablePassword</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Cette propriété n'est pas prise en charge.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscnonscriptable-portablesalt.md"><strong>PortableSalt</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Cette propriété n'est pas prise en charge.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si la boîte de dialogue demander les informations d’identification doit s’afficher.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-promptforcredsonclient.md"><strong>PromptForCredsOnClient</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si le contrôle client affiche une boîte de dialogue qui vous invite à entrer des informations d’identification.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdppreferredredirectioninfo-useredirectionservername.md"><strong>Propriété</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Contient une propriété nommée.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-publishercertificatechain.md"><strong>PublisherCertificateChain</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie la chaîne du certificat de l’éditeur. La chaîne est stockée dans un variant de type VT_BYREF qui contient un pointeur vers une structure <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context"><strong>CERT_CHAIN_CONTEXT</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si les appareils PnP attachés de manière dynamique et qui sont énumérés dans une session sont disponibles pour la redirection.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si les lecteurs PnP attachés de manière dynamique et qui sont énumérés dans une session sont disponibles pour la redirection.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-redirectionwarningtype.md"><strong>RedirectionWarningType</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Contrôle la présence et l’apparence de la boîte de dialogue de redirection.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-remotemonitorcount.md"><strong>RemoteMonitorCount</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Spécifie le nombre de moniteurs à distance.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-remotemonitorlayoutmatcheslocal.md"><strong>RemoteMonitorLayoutMatchesLocal</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Spécifie si la disposition du moniteur distant est identique à la disposition du moniteur local.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient5-remoteprogram.md"><strong>RemoteProgram</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Paramètre RemoteApp du client.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient7-remoteprogram2.md"><strong>RemoteProgram2</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Objet qui prend en charge l’interface <a href="itsremoteprogram2.md"><strong>ITSRemoteProgram2</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-securedsettings.md"><strong>SecuredSettings</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Pointeur d’interface <a href="imstscsecuredsettings-interface.md"><strong>IMsTscSecuredSettings</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient-securedsettings2.md"><strong>SecuredSettings2</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Pointeur vers l’interface <a href="imsrdpclientsecuredsettings-interface.md"><strong>IMsRdpClientSecuredSettings</strong></a> , utilisé pour définir des paramètres sécurisés pour le contrôle client.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient7-securedsettings3.md"><strong>SecuredSettings3</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Objet qui prend en charge l’interface <a href="imsrdpclientsecuredsettings2.md"><strong>IMsRdpClientSecuredSettings2</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-securedsettingsenabled.md"><strong>SecuredSettingsEnabled</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Indique si l’interface <a href="imstscsecuredsettings-interface.md"><strong>IMsTscSecuredSettings</strong></a> est disponible.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-server.md"><strong>Serveur</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Nom du serveur auquel le contrôle actuel est connecté.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si la boîte de dialogue Avertissement de sécurité de redirection doit s’afficher avant le démarrage d’une session.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-startconnected.md"><strong>StartConnected</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Indique si le contrôle établira la connexion au serveur hôte de session Bureau à distance dès le démarrage.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient5-transportsettings.md"><strong>TransportSettings</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Paramètre de la passerelle des services Bureau à distance du client.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient6-transportsettings2.md"><strong>TransportSettings2</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Interface à <a href="imsrdpclienttransportsettings2.md"><strong>IMsRdpClientTransportSettings2</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient7-transportsettings3.md"><strong>TransportSettings3</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Objet qui prend en charge l’interface <a href="imsrdpclienttransportsettings3.md"><strong>IMsRdpClientTransportSettings3</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient9-transportsettings4.md"><strong>TransportSettings4</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Objet qui prend en charge l’interface <a href="imsrdpclienttransportsettings4.md"><strong>IMsRdpClientTransportSettings4</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-trustedzonesite.md"><strong>TrustedZoneSite</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si le site Web à partir duquel l’utilisateur a lancé la connexion se trouve dans la liste des sites de confiance de l’ordinateur client.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable2-uiparentwindowhandle.md"><strong>UIParentWindowHandle</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Handle de fenêtre qui doit être la fenêtre parente pour le contrôle. Cela permet aux fenêtres affichées par le contrôle d’être correctement modales par rapport à toutes les fenêtres affichées par l’application parente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-usemultimon.md"><strong>UseMultimon</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">spécifie si le contrôle de ActiveX Bureau à distance doit utiliser plusieurs analyses.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdppreferredredirectioninfo-useredirectionservername.md"><strong>UseRedirectionServerName</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Indique s’il faut utiliser le nom du serveur de redirection.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-username.md"><strong>Nom d’utilisateur</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Informations d’identification d’ouverture de session de nom d’utilisateur.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-version.md"><strong>Version</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Numéro de version du contrôle actuel.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-verticalscrollbarvisible.md"><strong>VerticalScrollBarVisible</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Indique si le contrôle affiche une barre de défilement verticale.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si la boîte de dialogue d’avertissement de sécurité doit inclure un avertissement sur la redirection du presse-papiers avant de démarrer une session.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-warnaboutdirectxredirection.md"><strong>WarnAboutDirectXRedirection</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Cette propriété n'est pas utilisée.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-warnaboutprinterredirection.md"><strong>WarnAboutPrinterRedirection</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si la boîte de dialogue de redirection affiche un message sur la redirection de l’imprimante avant de démarrer une session.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a><br/></td>
<td style="text-align: left;">Lecture/écriture<br/></td>
<td style="text-align: left;">Spécifie si l’avertissement de sécurité doit inclure un avertissement concernant l’envoi d’informations d’identification au serveur distant avant le démarrage d’une session.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                    |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>               |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>               |
| CLSID<br/>                    | Le CLSID \_ MsRdpClient9NotSafeForScripting est défini en tant que 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Bureau à distance ActiveX les classes de contrôle](remote-desktop-activex-control-classes.md)
</dt> </dl>

