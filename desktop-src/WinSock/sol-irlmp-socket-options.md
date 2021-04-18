---
description: Le tableau suivant décrit les \_ options de socket sol IRLMP qui s’appliquent aux sockets créés pour la famille d’adresses IrDA (Infrared Data Association) \_ et le protocole de gestion des liaisons infrarouges (IRLMP).
ms.assetid: 0457159d-8509-435c-8f57-752530d5df65
title: Options de socket SOL_IRLMP (AF \_ IrDA. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090193aec00eaebd87494afefbafc7b1450fdb44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540634"
---
# <a name="sol_irlmp-socket-options"></a>\_Options de socket IRLMP sol

Le tableau suivant décrit les options de socket **sol \_ IRLMP** qui s’appliquent aux sockets créés pour la famille d’adresses IrDA (Infrared Data Association) \_ et le protocole de gestion des liaisons infrarouges (IRLMP). Consultez les pages de référence des fonctions [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) et [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour plus d’informations sur l’obtention et la définition des options de Socket.

Pour énumérer les protocoles et découvrir les propriétés prises en charge pour chaque protocole installé, utilisez la fonction [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

<dl> <dt><span id="SOL_IRLMP_Socket_Options"></span><span id="sol_irlmp_socket_options"></span><span id="SOL_IRLMP_SOCKET_OPTIONS"></span>**\_Options de socket IRLMP sol**</dt> <dd> <dl> <dt> 

| Option                 | Obtenir | Définissez | Type Optval     | Description                                                            |
|------------------------|-----|-----|-----------------|------------------------------------------------------------------------|
| \_mode de découverte IRLMP \_ |     |     |                 |                                                                        |
| IRLMP \_ ENUMDEVICES     | Oui |     | **LISTE DEVICELIST**  | Retourne une liste d’ID de périphérique IrDA pour les périphériques à compatibilité infrarouge dans la plage. |
| IRLMP \_ \_ mode exclusif |     |     | DWORD (booléen) | Définit le socket pour contourner la couche TinyTP pour communiquer directement avec IrLMP. |
| \_requête IAS \_ IRLMP      | Oui |     | **\_requête IAS**  | Interroge IAS sur un service et un nom de classe donnés pour ses attributs.      |
| IRLMP \_ IAS \_ défini        |     | Oui | **\_ensemble IAS**    | Définit IAS comme valeur d’attribut pour un attribut et un nom de classe donnés. |
| IRLMP \_ \_ mode IRLPT     |     | Oui | DWORD (booléen) | Active la communication avec les imprimantes avec compatibilité infrarouge.                        |
| \_paramètres IRLMP      |     |     |                 |                                                                        |
| IRLMP \_ Send \_ PDU \_ Len  | Oui |     | DWORD           | Récupère la longueur maximale de PDU requise pour utiliser le \_ mode IRLMP 9WIRE \_ .   |
| \_mode Sharp \_ IRLMP     |     | Oui |                 |                                                                        |
| IRLMP \_ \_ mode TINYTP    |     | Oui |                 |                                                                        |
| IRLMP \_ \_ mode 9WIRE     | Oui | Oui | DWORD (booléen) | Place le socket IrDA en mode IrCOMM.                                 |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_IRLMP_options"></span><span id="windows_support_for_sol_irlmp_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_IRLMP_OPTIONS"></span>**Prise en charge de Windows pour les \_ options IRLMP sol**</dt> <dd> <dl> <dt> 

| Option                            | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows Me, Windows 98 | Windows NT 4.0 |
|-----------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|------------------------|----------------|
| \_mode de découverte IRLMP \_<br/> |           |                     |               |                     |            |              | x                      |                |
| IRLMP \_ ENUMDEVICES<br/>     | x         | x                   | x             | x                   | x          | x            | x                      |                |
| IRLMP \_ \_ mode exclusif<br/> |           |                     |               |                     |            |              |                        |                |
| \_requête IAS \_ IRLMP<br/>      | x         | x                   | x             | x                   | x          | x            | x                      |                |
| IRLMP \_ IAS \_ défini<br/>        | x         | x                   | x             | x                   | x          | x            | x                      |                |
| IRLMP \_ \_ mode IRLPT<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |
| \_paramètres IRLMP<br/>      |           |                     |               |                     |            |              | x                      |                |
| IRLMP \_ Send \_ PDU \_ Len<br/>  | x         | x                   | x             | x                   | x          | x            |                        |                |
| \_mode Sharp \_ IRLMP<br/>     |           |                     |               |                     |            |              |                        |                |
| IRLMP \_ \_ mode TINYTP<br/>    |           |                     |               |                     |            |              | x                      |                |
| IRLMP \_ \_ mode 9WIRE<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Les options de socket **sol \_ IRLMP** et les structures utilisées par ces options de socket sont définies dans le fichier d’en-tête *AF \_ IrDA. h* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>AF \_ IrDA. h</dt> </dl> |



 

 




