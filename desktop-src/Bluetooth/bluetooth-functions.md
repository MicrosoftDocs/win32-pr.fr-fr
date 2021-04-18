---
title: Fonctions Bluetooth
description: Les fonctions de cette section sont utilisées pour gérer les appareils et les services Bluetooth.
ms.assetid: 5cd4a050-51f3-40f4-b434-be639e109f0f
keywords:
- Bluetooth, référence, fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad5343f0d609185f3bb472570b8454931fc6a18b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463207"
---
# <a name="bluetooth-functions"></a>Fonctions Bluetooth

Les fonctions de cette section sont utilisées pour gérer les appareils et les services Bluetooth.

Bluetooth est également pris en charge à l’aide de l’interface de programmation Windows Sockets. Pour plus d’informations sur la programmation de Bluetooth à l’aide de l’interface Windows Sockets, consultez [prise en charge de Windows Sockets pour Bluetooth](windows-sockets-support-for-bluetooth.md).



| Section                                                                                | Content                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)                     | Envoie une demande d’authentification à un appareil Bluetooth distant.                                                                                                                                 |
| [**BluetoothAuthenticateDeviceEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedeviceex)                 | Envoie une demande d’authentification à un appareil Bluetooth distant. En outre, cette fonction permet de transmettre des données hors bande dans l’appel de fonction pour l’appareil en cours d’authentification. |
| [**BluetoothAuthenticateMultipleDevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatemultipledevices)   | Permet à l’appelant de demander l’authentification de plusieurs appareils au cours d’une seule instance de l’Assistant de connexion Bluetooth.                                                            |
| [**BluetoothDisplayDeviceProperties**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothdisplaydeviceproperties)           | Appelle la feuille de propriétés informations sur l’appareil du panneau de configuration.                                                                                                                                  |
| [**BluetoothEnableDiscovery**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenablediscovery)                           | Modifie l’état de découverte d’une radio ou radio Bluetooth locale.                                                                                                                             |
| [**BluetoothEnableIncomingConnections**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenableincomingconnections)       | Modifie si une radio Bluetooth locale accepte les connexions entrantes.                                                                                                                        |
| [**BluetoothEnumerateInstalledServices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenumerateinstalledservices)     | Énumère les GUID (identificateurs globaux uniques) des services qui sont activés sur un périphérique Bluetooth.                                                                                    |
| [**BluetoothFindDeviceClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfinddeviceclose)                           | Ferme un handle d’énumération associé à une requête d’appareil.                                                                                                                          |
| [**BluetoothFindFirstDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstdevice)                           | Commence l’énumération des périphériques Bluetooth locaux.                                                                                                                                            |
| [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)                             | Commence l’énumération des radios Bluetooth locales.                                                                                                                                             |
| [**BluetoothFindNextDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextdevice)                             | Recherche le périphérique Bluetooth suivant.                                                                                                                                                              |
| [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)                               | Recherche la radio Bluetooth suivante.                                                                                                                                                               |
| [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)                             | Ferme le handle d’énumération associé à la recherche de radios Bluetooth.                                                                                                               |
| [**BluetoothGetDeviceInfo**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetdeviceinfo)                               | Récupère des informations sur un périphérique Bluetooth distant. L’appareil Bluetooth doit avoir été précédemment identifié par un appel de fonction de recherche d’appareil réussi.                           |
| [**BluetoothGetRadioInfo**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetradioinfo)                                 | Obtient des informations sur une radio Bluetooth.                                                                                                                                                  |
| [**BluetoothIsConnectable**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisconnectable)                               | Détermine si une radio ou des radios Bluetooth est connectable.                                                                                                                                |
| [**BluetoothIsDiscoverable**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisdiscoverable)                             | Détermine si une radio ou des radios Bluetooth est détectable.                                                                                                                               |
| [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication)       | Inscrit une fonction de rappel qui est appelée lorsqu’un périphérique Bluetooth particulier demande une authentification.                                                                                      |
| [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex)   | Inscrit une application pour une demande de code confidentiel, une comparaison numérique et une fonction de rappel.                                                                                                         |
| [**BluetoothRemoveDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothremovedevice)                                 | Supprime l’authentification entre un périphérique Bluetooth et l’ordinateur, en vidant toutes les informations mises en cache relatives à l’appareil.                                                                          |
| [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes)                       | Énumère le flux d’enregistrement SDP et appelle la fonction de rappel pour chaque attribut de l’enregistrement.                                                                                    |
| [**BluetoothSdpGetAttributeValue**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetattributevalue)                 | Récupère la valeur d’attribut pour un identificateur d’attribut.                                                                                                                                    |
| [**BluetoothSdpGetContainerElementData**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetcontainerelementdata)     | Itère au sein d’un flux de conteneur et retourne chaque élément contenu dans l’élément conteneur.                                                                                     |
| [**BluetoothSdpGetElementData**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetelementdata)                       | Récupère et analyse un élément unique à partir d’un flux SDP.                                                                                                                                     |
| [**BluetoothSdpGetString**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetstring)                                 | Convertit une chaîne brute incorporée dans l’enregistrement SDP en chaîne Unicode.                                                                                                               |
| [**BluetoothSelectDevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices)                               | Active la sélection du périphérique Bluetooth.                                                                                                                                                           |
| [**BluetoothSelectDevicesFree**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevicesfree)                       | Libère les ressources associées à un appel précédent à la fonction [**BluetoothSelectDevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices) .                                                                     |
| [**BluetoothSendAuthenticationResponse**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponse)     | Appelée lors de la réception d’une demande d’authentification pour envoyer la réponse de la clé de clé.                                                                                                               |
| [**BluetoothSendAuthenticationResponseEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponseex) | Appelée lorsqu’une demande d’authentification pour envoyer la réponse de la clé de clé ou de comparaison numérique est reçue.                                                                                         |
| [**BluetoothSetLocalServiceInfo**](/previous-versions/windows/desktop/legacy/bb870603(v=vs.85))                   | Définit les informations de service local pour une radio Bluetooth spécifique.                                                                                                                                |
| [**BluetoothSetServiceState**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsetservicestate)                           | Active ou désactive les services pour un appareil Bluetooth.                                                                                                                                          |
| [**BluetoothUnregisterAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothunregisterauthentication)         | Supprime l’inscription d’une routine de rappel précédemment inscrite avec un appel à la fonction [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .      |
| [**BluetoothUpdateDeviceRecord**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothupdatedevicerecord)                     | Met à jour le cache de l’ordinateur local sur un appareil Bluetooth.                                                                                                                                    |



 

 

 