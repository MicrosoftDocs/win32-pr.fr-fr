---
title: Structure RAS_PORT_0 (rassapi. h)
description: La \_ structure du port RAS \_ 0 contient des informations qui décrivent un port RAS.
ms.assetid: 750fc705-0770-427b-b7d6-7876b8b9118a
keywords:
- RAS_PORT_0 de la structure RAS
- Point d’accès RAS du pointeur de structure PRAS_PORT_0
topic_type:
- apiref
api_name:
- RAS_PORT_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d66725415d86aea44138f23fb3748e3187820f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013881"
---
# <a name="ras_port_0-structure"></a>\_Structure du port RAS \_ 0

\[cette version de la structure du **\_ PORT RAS \_ 0** n’est pas prise en charge à partir de Windows Vista. Utilisez à la place le [**\_ port RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) plus récent défini dans mprapi. h.\]

La structure du **\_ port RAS \_ 0** contient des informations qui décrivent un port RAS.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _RAS_PORT_0 {
  WCHAR wszPortName[RASSAPI_MAX_PORT_NAME];
  WCHAR wszDeviceType[RASSAPI_MAX_DEVICETYPE_NAME];
  WCHAR wszDeviceName[RASSAPI_MAX_DEVICE_NAME];
  WCHAR wszMediaName[RASSAPI_MAX_MEDIA_NAME];
  DWORD reserved;
  DWORD Flags;
  WCHAR wszUserName[UNLEN + 1];
  WCHAR wszComputer[NETBIOS_NAME_LEN];
  DWORD dwStartSessionTime;
  WCHAR wszLogonDomain[DNLEN + 1];
  BOOL  fAdvancedServer;
} RAS_PORT_0, *PRAS_PORT_0;
```



## <a name="members"></a>Membres

<dl> <dt>

**wszPortName**
</dt> <dd>

Chaîne Unicode terminée par le caractère null qui spécifie le nom du port, par exemple « COM1 ».

</dd> <dt>

**wszDeviceType**
</dt> <dd>

Chaîne Unicode terminée par le caractère null qui spécifie le type de l’appareil sur lequel la connexion a été établie, par exemple modem ou RNIS. La liste des types d’appareils qui peuvent être spécifiés dans ce membre inclut tous les types d’appareils installés sur le serveur, y compris les périphériques tiers.

</dd> <dt>

**wszDeviceName**
</dt> <dd>

Chaîne Unicode terminée par le caractère null qui spécifie le nom de l’appareil sur lequel la connexion a été établie, par exemple « Hayes 9600 » ou « PCIMACISDN1 ».

</dd> <dt>

**wszMediaName**
</dt> <dd>

Spécifie une chaîne Unicode terminée par le caractère null qui spécifie le nom du média utilisé pour la connexion, par exemple *rasser* ou *rastapi*.

</dd> <dt>

**reserved**
</dt> <dd>

Réservé.

</dd> <dt>

**Indicateurs**
</dt> <dd>

Spécifie un jeu d’indicateurs binaires qui spécifient la nature de la connexion établie sur ce port. Ce membre peut être une combinaison des indicateurs suivants.



| Valeur                                                                                                                                                                        | Signification                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GATEWAY_ACTIVE"></span><span id="gateway_active"></span><dl> <dt>**PASSERELLE \_ active**</dt> </dl>             | Si cet indicateur est défini, la passerelle NetBIOS est active sur le serveur.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="MESSENGER_PRESENT"></span><span id="messenger_present"></span><dl> <dt>**MESSENGER \_ présent**</dt> </dl>    | Si cet indicateur est défini, le service Messenger s’exécute sur le client distant.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="PORT_MULTILINKED"></span><span id="port_multilinked"></span><dl> <dt>**PORT à \_ liaisons multiples**</dt> </dl>       | Si cet indicateur est défini, le port est lié à des liaisons multiples avec d’autres ports. Utilisez ces informations pour afficher l’état de la connexion en tant que port à liaisons multiples. <br/> Pour un port à liaisons multiples, la structure des [**\_ \_ statistiques du port RAS**](ras-port-statistics-str.md) contient deux ensembles de statistiques : un pour le port seul et un autre pour les ports combinés dans la connexion à liaisons multiples.<br/> |
| <span id="PPP_CLIENT"></span><span id="ppp_client"></span><dl> <dt>**\_client PPP**</dt> </dl>                         | Si cet indicateur est défini, le client distant s’est connecté à l’aide de PPP. Si cet indicateur n’est pas défini, le client distant s’est connecté à l’aide du protocole AMB.<br/>                                                                                                                                                                                                                                        |
| <span id="REMOTE_LISTEN"></span><span id="remote_listen"></span><dl> <dt>**écoute à distance \_**</dt> </dl>                | Si cet indicateur est défini, le paramètre RemoteListen de la passerelle NetBIOS est défini sur 1 sur le serveur.<br/>                                                                                                                                                                                                                                                                               |
| <span id="USER_AUTHENTICATED"></span><span id="user_authenticated"></span><dl> <dt>**UTILISATEUR \_ authentifié**</dt> </dl> | Si cet indicateur est défini, un client distant est connecté au serveur et l’utilisateur a été authentifié. Cochez cet indicateur pour vous assurer qu’un client est réellement connecté à un port.<br/>                                                                                                                                                                                                   |



 

Si les \_ indicateurs Messenger présent, passerelle \_ active et écoute distante \_ sont définis, utilisez le service Messenger pour envoyer un message administratif au client distant. Si MESSENGER \_ est présent et que \_ l’écoute à distance est définie, mais \_ que la passerelle est active, n’envoyez des messages au client qu’à partir du serveur RAS auquel le client est connecté.

</dd> <dt>

**wszUserName**
</dt> <dd>

Chaîne Unicode terminée par le caractère null qui spécifie le nom de l’utilisateur distant connecté à ce port.

</dd> <dt>

**wszComputer**
</dt> <dd>

Chaîne Unicode terminée par le caractère null qui spécifie le nom de l’ordinateur client distant.

</dd> <dt>

**dwStartSessionTime**
</dt> <dd>

Spécifie la durée, en secondes, à partir du 1er janvier 1970, que le client s’est connecté au serveur RAS sur ce port. Utilisez les fonctions d’heure standard pour mettre en forme cette valeur pour l’affichage.

</dd> <dt>

**wszLogonDomain**
</dt> <dd>

Spécifie une chaîne Unicode terminée par le caractère null qui spécifie le nom du domaine sur lequel l’utilisateur distant a été authentifié. Cette chaîne est le nom de domaine uniquement, sans \\ \\ préfixe «».

</dd> <dt>

**fAdvancedServer**
</dt> <dd>

spécifie un indicateur différent de zéro si le serveur RAS associé à ce port est un serveur avancé tel que Windows 2000 advanced server. Utilisez ces informations pour déterminer le nom du serveur qui contient la base de données de comptes d’utilisateur. Si le serveur RAS est un serveur avancé, récupérez le nom du serveur de comptes d’utilisateur en concaténant le préfixe « \\ \\ » au nom renvoyé dans le membre **wszLogonDomain** . En effet, pour un serveur avancé, le nom de domaine d’ouverture de session locale est le même que le nom du serveur. Si le serveur RAS est une station de travail, utilisez la fonction [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) pour obtenir le nom du serveur de compte d’utilisateur.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du service d’accès à distance (RAS)](about-remote-access-service.md)
</dt> <dt>

[Structures d’administration de serveur RAS](ras-server-administration-structures.md)
</dt> <dt>

[**\_Port RAS \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**\_statistiques du port RAS \_**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminPortEnum**](rasadminportenum.md)
</dt> </dl>

 

 





