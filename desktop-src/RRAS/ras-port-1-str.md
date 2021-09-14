---
title: Structure RAS_PORT_1 (rassapi. h)
description: La \_ structure du port \_ 1 RAS contient des informations sur un port RAS.
ms.assetid: f226ef16-feb4-41e0-ba60-ddb2f0acd305
keywords:
- RAS_PORT_1 de la structure RAS
- Point d’accès RAS du pointeur de structure PRAS_PORT_1
topic_type:
- apiref
api_name:
- RAS_PORT_1
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fe450e5ea5f8ceee48436dbbe05570d0d818a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013880"
---
# <a name="ras_port_1-structure"></a>\_Structure du port RAS \_ 1

\[cette version de la structure du **\_ PORT \_ 1 RAS** n’est pas prise en charge à partir de Windows Vista. Utilisez à la place le [**\_ port RAS \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) plus récent défini dans mprapi. h.\]

La structure du **\_ port \_ 1 RAS** contient des informations sur un port RAS.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _RAS_PORT_1 {
  RAS_PORT_0                rasport0;
  DWORD                     LineCondition;
  DWORD                     HardwareCondition;
  DWORD                     LineSpeed;
  WORD                      NumStatistics;
  WORD                      NumMediaParms;
  DWORD                     SizeMediaParms;
  RAS_PPP_PROJECTION_RESULT ProjResult;
} RAS_PORT_1, *PRAS_PORT_1;
```



## <a name="members"></a>Membres

<dl> <dt>

**rasport0**
</dt> <dd>

Spécifie une structure de [**\_ port RAS \_ 0**](ras-port-0-str.md) qui contient des informations sur le port, telles que le nom du port, le nom de l’utilisateur distant connecté au port, et ainsi de suite.

</dd> <dt>

**LineCondition**
</dt> <dd>

Spécifie l’état du port. Ce membre peut être l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                            | Signification                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RAS_PORT_NON_OPERATIONAL"></span><span id="ras_port_non_operational"></span><dl> <dt>**\_port RAS \_ non \_ opérationnel**</dt> </dl> | Le port n’est pas opérationnel. Recherchez dans le journal des événements les erreurs signalées par le serveur.<br/>                                                                         |
| <span id="RAS_PORT_DISCONNECTED"></span><span id="ras_port_disconnected"></span><dl> <dt>**\_port RAS \_ déconnecté**</dt> </dl>           | Le port est actuellement déconnecté.<br/>                                                                                                                         |
| <span id="RAS_PORT_CALLING_BACK"></span><span id="ras_port_calling_back"></span><dl> <dt>**\_port RAS \_ rappelé \_**</dt> </dl>          | Le serveur RAS rappelle le client RAS.<br/>                                                                                                              |
| <span id="RAS_PORT_LISTENING"></span><span id="ras_port_listening"></span><dl> <dt>**\_écoute du port RAS \_**</dt> </dl>                    | Le port attend qu’un client appelle dans.<br/>                                                                                                                |
| <span id="RAS_PORT_AUTHENTICATING"></span><span id="ras_port_authenticating"></span><dl> <dt>**PORT RAS d' \_ \_ authentification**</dt> </dl>     | Le serveur est en cours d’authentification du client distant.<br/>                                                                                           |
| <span id="RAS_PORT_AUTHENTICATED"></span><span id="ras_port_authenticated"></span><dl> <dt>**\_port RAS \_ authentifié**</dt> </dl>        | Le client distant est à présent authentifié.<br/>                                                                                                                     |
| <span id="RAS_PORT_INITIALIZING"></span><span id="ras_port_initializing"></span><dl> <dt>**\_ \_ initialisation du port RAS**</dt> </dl>           | L’appareil attaché au port est en cours d’initialisation. L’état du port passe à l’écoute du \_ port RAS \_ lorsque l’initialisation est terminée.<br/> |



 

</dd> <dt>

**HardwareCondition**
</dt> <dd>

Spécifie l’une des valeurs suivantes pour indiquer l’état de l’appareil attaché au port.



| Valeur                                                                                                                                                                                                  | Signification                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="RAS_MODEM_OPERATIONAL"></span><span id="ras_modem_operational"></span><dl> <dt>**\_modem RAS \_ opérationnel**</dt> </dl>                 | Le modem attaché à ce port est opérationnel et est prêt à recevoir les appels des clients.<br/> |
| <span id="RAS_MODEM_HARDWARE_FAILURE"></span><span id="ras_modem_hardware_failure"></span><dl> <dt>**\_ \_ défaillance matérielle du modem RAS \_**</dt> </dl> | Le modem attaché à ce port présente un problème matériel.<br/>                              |



 

</dd> <dt>

**LineSpeed**
</dt> <dd>

Spécifie la vitesse, en bits par seconde, avec laquelle l’ordinateur peut communiquer avec le port.

</dd> <dt>

**NumStatistics**
</dt> <dd>

Ce membre n’est pas utilisé. Les fonctions d’administration RAS, telles que la fonction [**RasAdminPortGetInfo**](rasadminportgetinfo.md) , utilisent la structure des [**\_ \_ statistiques du port RAS**](ras-port-statistics-str.md) pour retourner les statistiques des ports.

</dd> <dt>

**NumMediaParms**
</dt> <dd>

Spécifie le nombre de paramètres spécifiques au média pour ce port. Pour les supports série, il s’agit généralement du nombre de valeurs qui apparaissent dans le fichier SERIAL.INI.

</dd> <dt>

**SizeMediaParms**
</dt> <dd>

Spécifie la taille, en octets, de la mémoire tampon requise pour tous les paramètres spécifiques au média. La fonction [**RasAdminPortGetInfo**](rasadminportgetinfo.md) retourne une mémoire tampon qui contient un tableau de structures de [**\_ paramètres RAS**](ras-parameters-str.md) avec les paramètres et les valeurs de média pour le port.

</dd> <dt>

**ProjResult**
</dt> <dd>

Structure [**de \_ \_ \_ résultat de projection PPP RAS**](ras-ppp-projection-result-str.md) qui spécifie les informations de projection PPP pour ce port. Cette structure fournit des informations pour chaque protocole négocié lorsqu’un client RAS se connecte à un serveur.

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

[**\_paramètres RAS**](ras-parameters-str.md)
</dt> <dt>

[**\_Port RAS \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**\_statistiques du port RAS \_**](ras-port-statistics-str.md)
</dt> <dt>

[**résultat de la \_ projection PPP RAS \_ \_**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





