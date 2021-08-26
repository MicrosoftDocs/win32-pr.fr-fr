---
title: Paramètres de configuration
description: Le comportement de l’API du point de contrôle et de l’API de l’hôte du périphérique peut être modifié en modifiant les paramètres du Registre.
ms.assetid: 81893cde-d28f-41ec-a6c1-159b3eb84274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68438f6eb425da253aa7f59af3b7d060bacacadb865d4546ddbc0f37fecd9ed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008109"
---
# <a name="configuration-settings"></a>Paramètres de configuration

Le comportement de l' [API du point de contrôle](control-point-api.md) et de l’API de l' [hôte du périphérique](device-host-api.md) peut être modifié en modifiant les paramètres du Registre.

Sept valeurs de Registre affectent le comportement :

-   **DownloadScope**
-   **DeviceLifeTime**
-   \\Hôte d’appareil **UPnP** \\ **Limite de taille de fichier**
-   \\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Limite de taille de fichier**
-   **MaxCache**
-   **TTL**
-   **ReceiveScope**

Il existe deux valeurs de Registre appelées **limite de taille de fichier**, une pour les documents de description et l’autre pour les réponses qui utilisent le protocole SOAP (Simple Object Access Protocol).

L’emplacement de chacune des sept valeurs dans le Registre est le suivant :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         UPnPControl Point
            DownloadScope
         UPnP Device Host
            Devices
               DeviceLifeTime
            File Size Limit
         Windows
            CurrentVersion
               UPnP
                  File Size Limit
   SYSTEM
      CurentControlSet
         Services
            SSDPSRV
               Parameters
                  MaxCache
                  TTL
                  ReceiveScope
```

## <a name="registry-value-descriptions"></a>Descriptions des valeurs de Registre

Les valeurs de Registre sont expliquées dans la liste suivante. Chaque valeur de Registre est un nombre **\_ DWORD reg** (un entier 32 bits). L’effet de chaque valeur est global.

<dl> <dt>

<span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**DownloadScope**
</dt> <dd>

Spécifie les adresses IP valides pour l’URL du document de description de l’appareil. Si l’adresse IP de l’hôte spécifié dans l’URL du document de description ne se trouve pas dans l’étendue spécifiée par **DownloadScope**, cette adresse IP n’est pas valide et l’objet de l’appareil n’est pas créé.

Les valeurs valides sont indiquées dans le tableau suivant. La valeur par défaut est 1.



| Valeur de **DownloadScope** | Signification                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                          | L’adresse IP de l’hôte doit être une adresse de sous-réseau.                                                                                                                                                                |
| 1                          | L’adresse IP de l’hôte doit être une adresse de sous-réseau ou une adresse privée de 10. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (comme spécifié par la norme RFC 1918) ou 169,254. *x*. *x* (comme spécifié par la norme RFC 3330). |
| 2                          | L’adresse IP de l’hôte doit être une adresse de sous-réseau, une adresse privée ou une adresse qui se trouve dans les tronçons de durée de vie (TTL) du point de contrôle.                                                              |
| 3                          | L’adresse IP de l’hôte peut être n’importe quelle adresse.                                                                                                                                                                      |
| >3                      | Identique à celui de la valeur 0.                                                                                                                                                                              |



 

</dd> <dt>

<span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**DeviceLifeTime**
</dt> <dd>

Facultatif. Spécifie la durée de vie d’un appareil, en secondes, qui remplace la valeur fournie dans le message d’annonce de l’appareil. Si **DeviceLifeTime** est présent, la valeur spécifiée dans l’annonce de l’appareil est ignorée et la valeur de Registre est utilisée à la place. Cela s’applique à tous les appareils.

Les valeurs valides sont comprises entre 900 et **Max \_ DWORD**. La valeur par défaut est 1800. Si **DeviceLifeTime** est défini sur 0, la valeur par défaut est utilisée.

</dd> <dt>

<span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\Hôte d’appareil **UPnP** \\ **Limite de taille de fichier**
</dt> <dd>

Spécifie la taille maximale, en octets, de chaque document de description. ce paramètre n’est pas configurable dans les versions de Windows précédentes Windows XP Service Pack 2. Dans les versions précédentes, ce paramètre est codé en dur en tant que 102400.

Les valeurs valides sont comprises entre 10240 et **Max \_ DWORD**. La valeur par défaut est 102400.

</dd> <dt>

<span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Limite de taille de fichier**
</dt> <dd>

Spécifie la taille maximale, en octets, de la réponse SOAP acceptable. ce paramètre n’est pas configurable dans les versions de Windows précédentes Windows XP Service Pack 2. Dans les versions précédentes, ce paramètre est codé en dur en tant que 102400.

Les valeurs valides sont comprises entre 10240 et **Max \_ DWORD**. La valeur par défaut est 102400.

</dd> <dt>

<span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**MaxCache**
</dt> <dd>

Spécifie le nombre maximal d’entrées autorisées dans le cache SSDP (simple service Discovery Protocol).

Les valeurs valides sont comprises entre 10 et 30000. La valeur par défaut est 1000.

</dd> <dt>

<span id="TTL"></span><span id="ttl"></span>**EXPIRATION**
</dt> <dd>

Spécifie la durée de vie d’un paquet SSDP. Autrement dit, la **durée de vie** spécifie le nombre de tronçons autorisés pour un paquet.

Les valeurs valides sont comprises entre 1 et 255. La valeur par défaut est 1.

</dd> <dt>

<span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**ReceiveScope**
</dt> <dd>

Spécifie les adresses IP qui sont des sources valides d’un message. Si un message entrant provient d’une adresse qui ne se trouve pas dans l’étendue spécifiée par **ReceiveScope**, le message est ignoré. ce paramètre n’est pas configurable dans les versions de Windows précédentes Windows XP Service Pack 2. Dans les versions précédentes, un message est accepté sans tenir compte de sa source.

Les valeurs valides sont indiquées dans le tableau suivant. La valeur par défaut est 1.



| Valeur de **ReceiveScope** | Signification                                                                                                                                                                                                      |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                         | L’adresse IP de l’expéditeur doit être une adresse de sous-réseau.                                                                                                                                                                |
| 1                         | L’adresse IP de l’expéditeur doit être une adresse de sous-réseau ou une adresse privée de 10. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (comme spécifié par la norme RFC 1918) ou 169,254. *x*. *x* (comme spécifié par la norme RFC 3330). |
| 2                         | Non utilisé. Si **ReceiveScope** a la valeur 2, la valeur par défaut est utilisée.                                                                                                                                        |
| 3                         | L’adresse IP de l’expéditeur peut être n’importe quelle adresse.                                                                                                                                                                      |



 

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble de l’architecture UPnP](overview-of-universal-plug-and-play.md)
</dt> </dl>

 

 




