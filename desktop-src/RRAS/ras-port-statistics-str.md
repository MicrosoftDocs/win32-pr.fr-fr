---
title: Structure RAS_PORT_STATISTICS (rassapi. h)
description: La \_ structure des statistiques du port RAS \_ signale les statistiques collectées par un serveur RAS pour un port connecté.
ms.assetid: c42c7059-ff92-4f49-a86e-2f47a083aa8e
keywords:
- RAS_PORT_STATISTICS de la structure RAS
- Point d’accès RAS du pointeur de structure PRAS_PORT_STATISTICS
topic_type:
- apiref
api_name:
- RAS_PORT_STATISTICS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e60fb001da3f8401e47c366eecc86aced22b77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013872"
---
# <a name="ras_port_statistics-structure"></a>Structure des statistiques du \_ port RAS \_

\[la structure des **\_ \_ statistiques du PORT RAS** n’est pas prise en charge à partir de Windows Vista.\]

La structure des **\_ \_ statistiques du port RAS** signale les statistiques collectées par un serveur RAS pour un port connecté. Le serveur RAS réinitialise les différents compteurs de statistiques chaque fois que le port est connecté. Appelez la fonction [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) pour forcer le serveur RAS à réinitialiser les compteurs des statistiques.

Pour un port qui fait partie d’une connexion à liaisons multiples, cette structure fournit deux ensembles de statistiques. Le premier jeu contient les statistiques cumulatives pour tous les ports de la connexion. Ces statistiques sont les mêmes pour tous les ports de la connexion. Le deuxième jeu contient les statistiques de ce port uniquement. Si le port ne fait pas partie d’une connexion multilien, les deux ensembles de statistiques ont les mêmes informations. Pour déterminer si un port fait partie d’une connexion multilien, vérifiez le \_ bit de liaison multilien dans le membre **Flags** de la structure [**du \_ port RAS \_ 0**](ras-port-0-str.md) du port.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _RAS_PORT_STATISTICS {
  DWORD dwBytesXmited;
  DWORD dwBytesRcved;
  DWORD dwFramesXmited;
  DWORD dwFramesRcved;
  DWORD dwCrcErr;
  DWORD dwTimeoutErr;
  DWORD dwAlignmentErr;
  DWORD dwHardwareOverrunErr;
  DWORD dwFramingErr;
  DWORD dwBufferOverrunErr;
  DWORD dwBytesXmitedUncompressed;
  DWORD dwBytesRcvedUncompressed;
  DWORD dwBytesXmitedCompressed;
  DWORD dwBytesRcvedCompressed;
  DWORD dwPortBytesXmited;
  DWORD dwPortBytesRcved;
  DWORD dwPortFramesXmited;
  DWORD dwPortFramesRcved;
  DWORD dwPortCrcErr;
  DWORD dwPortTimeoutErr;
  DWORD dwPortAlignmentErr;
  DWORD dwPortHardwareOverrunErr;
  DWORD dwPortFramingErr;
  DWORD dwPortBufferOverrunErr;
  DWORD dwPortBytesXmitedUncompressed;
  DWORD dwPortBytesRcvedUncompressed;
  DWORD dwPortBytesXmitedCompressed;
  DWORD dwPortBytesRcvedCompressed;
} RAS_PORT_STATISTICS, *PRAS_PORT_STATISTICS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwBytesXmited**
</dt> <dd>

Spécifie le nombre total d’octets transmis par la connexion.

</dd> <dt>

**dwBytesRcved**
</dt> <dd>

Spécifie le nombre total d’octets reçus par la connexion.

</dd> <dt>

**dwFramesXmited**
</dt> <dd>

Spécifie le nombre total de trames transmises par la connexion.

</dd> <dt>

**dwFramesRcved**
</dt> <dd>

Spécifie le nombre total de trames reçues par la connexion.

</dd> <dt>

**dwCrcErr**
</dt> <dd>

Spécifie le nombre total d’erreurs CRC sur la connexion. Les erreurs CRC sont provoquées par l’échec d’une vérification de redondance cyclique. Une erreur CRC indique qu’un ou plusieurs caractères du paquet de données reçus ont été détectés comme étant déformés à l’arrivée.

</dd> <dt>

**dwTimeoutErr**
</dt> <dd>

Spécifie le nombre total d’erreurs de délai d’attente sur la connexion. Des erreurs de délai d’attente se produisent lorsqu’un caractère attendu n’est pas reçu dans le temps. Dans ce cas, le logiciel suppose que les données ont été perdues et demande qu’il soit renvoyé.

</dd> <dt>

**dwAlignmentErr**
</dt> <dd>

Spécifie le nombre total d’erreurs d’alignement sur la connexion. Des erreurs d’alignement se produisent lorsqu’un caractère reçu n’est pas celui attendu. Cela se produit généralement lorsqu’un caractère est perdu ou lorsqu’une erreur de délai d’attente se produit.

</dd> <dt>

**dwHardwareOverrunErr**
</dt> <dd>

Spécifie le nombre total d’erreurs de saturation matérielle sur la connexion. Ces erreurs indiquent le nombre de fois que l’ordinateur expéditeur a transmis des caractères plus rapidement que le matériel de l’ordinateur récepteur peut les traiter. Si ce problème persiste, réduisez la vitesse de connexion BPS sur le client.

</dd> <dt>

**dwFramingErr**
</dt> <dd>

Spécifie le nombre total d’erreurs de tramage sur la connexion. Une erreur de trame se produit lorsqu’un caractère asynchrone est reçu avec un bit de démarrage ou d’arrêt non valide.

</dd> <dt>

**dwBufferOverrunErr**
</dt> <dd>

Spécifie le nombre total d’erreurs de dépassement de mémoire tampon sur la connexion. Une erreur de dépassement de mémoire tampon se produit lorsque l’ordinateur expéditeur transmet des caractères plus rapidement que l’ordinateur récepteur ne peut les gérer. Si ce problème persiste, réduisez la vitesse de connexion BPS sur le client.

</dd> <dt>

**dwBytesXmitedUncompressed**
</dt> <dd>

Spécifie le nombre total d’octets transmis non compressés par la connexion.

</dd> <dt>

**dwBytesRcvedUncompressed**
</dt> <dd>

Spécifie le nombre total d’octets reçus non compressés par la connexion.

</dd> <dt>

**dwBytesXmitedCompressed**
</dt> <dd>

Spécifie le nombre total d’octets transmis compressés par la connexion.

</dd> <dt>

**dwBytesRcvedCompressed**
</dt> <dd>

Spécifie le nombre total d’octets reçus compressés par la connexion.

</dd> <dt>

**dwPortBytesXmited**
</dt> <dd>

Spécifie le nombre total d’octets transmis par le port.

</dd> <dt>

**dwPortBytesRcved**
</dt> <dd>

Spécifie le nombre total d’octets reçus par le port.

</dd> <dt>

**dwPortFramesXmited**
</dt> <dd>

Spécifie le nombre total de trames transmises par le port.

</dd> <dt>

**dwPortFramesRcved**
</dt> <dd>

Spécifie le nombre total de trames reçues par le port.

</dd> <dt>

**dwPortCrcErr**
</dt> <dd>

Spécifie le nombre total d’erreurs CRC sur le port. Les erreurs CRC sont provoquées par l’échec d’une vérification de redondance cyclique. Une erreur CRC indique qu’un ou plusieurs caractères du paquet de données reçus ont été détectés comme étant déformés à l’arrivée.

</dd> <dt>

**dwPortTimeoutErr**
</dt> <dd>

Spécifie le nombre total d’erreurs de délai d’attente sur le port. Des erreurs de délai d’attente se produisent lorsqu’un caractère attendu n’est pas reçu dans le temps. Dans ce cas, le logiciel suppose que les données ont été perdues et demande qu’il soit renvoyé.

</dd> <dt>

**dwPortAlignmentErr**
</dt> <dd>

Spécifie le nombre total d’erreurs d’alignement sur le port. Des erreurs d’alignement se produisent lorsqu’un caractère reçu n’est pas celui attendu. Cela se produit généralement lorsqu’un caractère est perdu ou lorsqu’une erreur de délai d’attente se produit.

</dd> <dt>

**dwPortHardwareOverrunErr**
</dt> <dd>

Spécifie le nombre total d’erreurs de saturation matérielle sur le port. Ces erreurs indiquent le nombre de fois que l’ordinateur expéditeur a transmis des caractères plus rapidement que le matériel de l’ordinateur récepteur peut les traiter. Si ce problème persiste, réduisez la vitesse de connexion BPS sur le client.

</dd> <dt>

**dwPortFramingErr**
</dt> <dd>

Spécifie le nombre total d’erreurs de tramage sur le port. Une erreur de trame se produit lorsqu’un caractère asynchrone est reçu avec un bit de démarrage ou d’arrêt non valide.

</dd> <dt>

**dwPortBufferOverrunErr**
</dt> <dd>

Spécifie le nombre total d’erreurs de dépassement de mémoire tampon sur le port. Une erreur de dépassement de mémoire tampon se produit lorsque l’ordinateur expéditeur transmet des caractères plus rapidement que l’ordinateur récepteur ne peut les gérer. Si ce problème persiste, réduisez la vitesse de connexion BPS sur le client.

</dd> <dt>

**dwPortBytesXmitedUncompressed**
</dt> <dd>

Spécifie le nombre total d’octets transmis non compressés par le port. Si le port fait partie d’une connexion multilien, ce membre n’est pas valide. Utilisez plutôt les statistiques de compression pour la connexion.

</dd> <dt>

**dwPortBytesRcvedUncompressed**
</dt> <dd>

Spécifie le nombre total d’octets reçus non compressés par le port. Si le port fait partie d’une connexion multilien, ce membre n’est pas valide. Utilisez plutôt les statistiques de compression pour la connexion.

</dd> <dt>

**dwPortBytesXmitedCompressed**
</dt> <dd>

Spécifie le nombre total d’octets transmis compressés par le port. Si le port fait partie d’une connexion multilien, ce membre n’est pas valide. Utilisez plutôt les statistiques de compression pour la connexion.

</dd> <dt>

**dwPortBytesRcvedCompressed**
</dt> <dd>

Spécifie le nombre total d’octets reçus compressés par le port. Si le port fait partie d’une connexion multilien, ce membre n’est pas valide. Utilisez plutôt les statistiques de compression pour la connexion.

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

[**\_Port RAS \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortClearStatistics**](rasadminportclearstatistics.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





