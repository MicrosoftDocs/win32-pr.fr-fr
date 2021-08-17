---
description: Le tableau suivant décrit les \_ options de socket AppleTalk AppleTalk qui s’appliquent aux sockets créés pour la famille d’adresses AppleTalk (AF \_ AppleTalk).
ms.assetid: 1a6b18e3-1fea-4ba2-8076-c38e7f679e9e
title: Options de socket SOL_APPLETALK (Atalkwsh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SOL_APPLETALK
- Windows
api_type:
- HeaderDef
api_location:
- Atalkwsh.h
ms.openlocfilehash: 5ea45b4007a3bd36d2cfbceda5b7ec4f2cff20d9bb2387fb2d184710a8a4492c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740006"
---
# <a name="sol_appletalk-socket-options"></a>\_Options de socket AppleTalk AppleTalk

Le tableau suivant décrit les options de socket **\_ AppleTalk AppleTalk** qui s’appliquent aux sockets créés pour la famille d’adresses AppleTalk (AF \_ AppleTalk). Consultez les pages de référence des fonctions [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) et [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour plus d’informations sur l’obtention et la définition des options de Socket.

Pour énumérer les protocoles et découvrir les propriétés prises en charge pour chaque protocole installé, utilisez la fonction [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

<dl> <dt><span id="SOL_APPLETALK_Socket_Options"></span><span id="sol_appletalk_socket_options"></span><span id="SOL_APPLETALK_SOCKET_OPTIONS"></span>**\_Options de socket AppleTalk AppleTalk**</dt> <dd> <dl> <dt> 

| Option                          | Obtenir | Définissez | Type Optval                          | Description                                                                                                                                                                                          |
|---------------------------------|-----|-----|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_confirmer le \_ nom               | oui |     | **\_TUPLE du NBP WSH \_**                  | Confirme qu’un nom AppleTalk donné est lié à l’adresse spécifiée.                                                                                                                                  |
| par conséquent, \_ DÉSinscrire le \_ nom            |     | oui | **\_nom du Registre WSH \_**              | Annule l’inscription du nom sur le réseau.                                                                                                                                                               |
| \_GETLOCALZONES               | oui |     | **\_zones de recherche WSH \_**               | Retourne une liste de noms de zone connus du nom d’adaptateur donné.                                                                                                                                        |
| \_GETMYZONE                   | oui |     | Char \[\]                            | Retourne la zone par défaut sur le réseau.                                                                                                                                                             |
| \_GETNETINFO                  | oui |     | **\_recherche WSH \_ NETDEF \_ sur l' \_ adaptateur** | Retourne les valeurs d’amorçage pour le réseau ainsi que la zone par défaut. Le paramètre *optlen* doit être au moins un octet supérieur à la taille de la **\_ recherche WSH \_ NETDEF \_ sur \_** la structure de l’adaptateur.  |
| \_GETZONELIST                 | oui |     | **\_zones de recherche WSH \_**               | Retourne les noms de zone à partir de la liste des zones Internet. Le paramètre *optlen* doit être au moins d’un octet plus grand que la taille de la structure de **\_ \_ zones de recherche WSH** .                                       |
| \_Rechercher \_ MYZONE              | oui |     |                                      | Comme \_ GETMYZONE                                                                                                                                                                                |
| \_nom de recherche \_                | oui |     | **\_nom de recherche WSH \_**                | Recherche un nom de NBP spécifié et retourne les tuples correspondants des informations de nom et NBP. Le paramètre *optlen* doit être au moins un octet supérieur à la taille de la \_ structure de nom de recherche WSH \_ . |
| \_Rechercher \_ NETDEF sur \_ l' \_ adaptateur | oui |     | **\_recherche WSH \_ NETDEF \_ sur l' \_ adaptateur** | Comme c’est le cas \_ GETNETINFO.                                                                                                                                                                              |
| \_zones de recherche \_               | oui |     | **\_zones de recherche WSH \_**               | Comme c’est le cas \_ GETZONELIST.                                                                                                                                                                             |
| \_ \_ zones de recherche \_ sur l' \_ adaptateur  | oui |     | **\_zones de recherche WSH \_**               | Comme c’est le cas \_ GETLOCALZONES.                                                                                                                                                                           |
| ainsi, \_ PAP \_ obtient l' \_ État du serveur \_    | oui |     | **\_État du \_ \_ serveur \_ d’accès WSH PAP**    | Retourne l’État PAP d’un serveur donné                                                                                                                                                           |
| DONC \_ PAP \_ prime \_ lecture            |     | oui | Char \[\]                            | Cet appel prime une lecture sur une connexion PAP afin que l’expéditeur puisse commencer à envoyer les données                                                                                                                 |
| par conséquent, \_ PAP \_ définir l' \_ État du serveur \_    |     | oui | Char \[\]                            | Définit l’État à envoyer si un autre client demande l’État                                                                                                                                     |
| \_nom du Registre \_              |     | oui | **\_nom du Registre WSH \_**              | Inscrit le nom donné sur le réseau AppleTalk.                                                                                                                                                    |
| \_supprimer le \_ nom                |     | oui | **\_nom du Registre WSH \_**              | Identique au nom de l’annulation de l' \_ inscription \_                                                                                                                                                                         |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_APPLETALK_options"></span><span id="windows_support_for_sol_appletalk_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_APPLETALK_OPTIONS"></span>**Windows Prise en charge des \_ options AppleTalk AppleTalk**</dt> <dd> <dl> <dt> 

| Option                          | Windows Vista et versions ultérieures | Windows Server 2003 | Windows XP | Windows 2000 | Windows 4 | Windows 9x/Me |
|---------------------------------|-------------------------|---------------------|------------|--------------|-------------|---------------|
| \_confirmer le \_ nom               |                         | x                   | x          | x            | x           |               |
| par conséquent, \_ DÉSinscrire le \_ nom            |                         | x                   | x          | x            | x           |               |
| \_GETLOCALZONES               |                         | x                   | x          | x            | x           |               |
| \_GETMYZONE                   |                         | x                   | x          | x            | x           |               |
| \_GETNETINFO                  |                         | x                   | x          | x            | x           |               |
| \_GETZONELIST                 |                         | x                   | x          | x            | x           |               |
| \_Rechercher \_ MYZONE              |                         | x                   | x          | x            | x           |               |
| \_nom de recherche \_                |                         | x                   | x          | x            | x           |               |
| \_Rechercher \_ NETDEF sur \_ l' \_ adaptateur |                         | x                   | x          | x            | x           |               |
| \_zones de recherche \_               |                         | x                   | x          | x            | x           |               |
| \_ \_ zones de recherche \_ sur l' \_ adaptateur  |                         | x                   | x          | x            | x           |               |
| ainsi, \_ PAP \_ obtient l' \_ État du serveur \_    |                         | x                   | x          | x            | x           |               |
| DONC \_ PAP \_ prime \_ lecture            |                         | x                   | x          | x            | x           |               |
| par conséquent, \_ PAP \_ définir l' \_ État du serveur \_    |                         | x                   | x          | x            | x           |               |
| \_nom du Registre \_              |                         | x                   | x          | x            | x           |               |
| \_supprimer le \_ nom                |                         | x                   | x          | x            | x           |               |



 

les options de **SOL \_ APPLETALK** sont uniquement prises en charge sur les versions serveur de Windows 2000 et Windows NT 4,0.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Les options de socket **\_ AppleTalk AppleTalk** et les structures utilisées par ces options de socket sont définies dans le fichier d’en-tête *Atalkwsh. h* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Atalkwsh. h</dt> </dl> |



 

 




