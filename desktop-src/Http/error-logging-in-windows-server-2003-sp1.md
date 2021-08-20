---
title: journalisation des erreurs dans Windows Server 2003 SP1
description: journalisation des erreurs dans Windows Server 2003 SP1
ms.assetid: 8c7fcc66-5446-4e25-8e6d-1a9260c55e36
keywords:
- journalisation des erreurs dans Windows Server 2003 avec Service Pack 1 (SP1)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a71d5a84dfba8ecb9a78ed38d3ad112f0820e6b578bce77e189e5047a25f458b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014807"
---
# <a name="error-logging-in-windows-server-2003-sp1"></a>journalisation des erreurs dans Windows Server 2003 SP1

## <a name="addition-of-w3c-style-headers"></a>Ajout d’en-têtes de style W3C

à compter de Windows server 2003 avec Service Pack 1 (SP1), le journal des erreurs de l’API du serveur HTTP comprend des en-têtes de style W3C permettant d’analyser les fichiers journaux à l’aide d’analyseurs de journaux standard. Le modèle ci-dessous répertorie tous les champs qui peuvent être consignés dans le fichier journal des erreurs http.

``` syntax
#Software: <Name of the HTTP Server>
#Version: 1.0 <Log format version>
#Date: <Log file creation date and time>
#Fields: <date time s-computername c-ip c-port s-ip s-port cs-version
         cs-method cs-uri cs(User-Agent) cs(Cookie) cs(referrer) 
         cs-host sc-status sc-bytes cs-bytes time-taken s-siteid  
         s- reason s-queuename <header names of fields logged>

```

## <a name="logging-additional-fields"></a>Journalisation des champs supplémentaires

Le journal des erreurs HTTP a été étendu pour inclure neuf champs supplémentaires afin de consigner les données relatives aux échecs qui se produisent. Les nouveaux champs d’erreur sont répertoriés ci-dessous :

-   Nom de l’ordinateur serveur \[ S-ComputerName\]
-   Agent utilisateur \[ cs ( \_ agent utilisateur)\]
-   Cookie \[ cs (cookie)\]
-   \[point de renvoi CS (Referrer)\]
-   Nom d’hôte \[ CS-Host\]
-   Octets reçus par le serveur \[ , SC-octets\]
-   Octets reçus et traités par le serveur \[ cs-bytes\]
-   Temps nécessaire pour traiter le temps de requête \[ -pris\]
-   Queue-Name (réservé pour IIS) \[ S-QUEUENAME\]

## <a name="selecting-fileds-to-log-in-the-http-error-log-file"></a>Sélection des fichiers à consigner dans le fichier journal des erreurs HTTP

La clé de Registre **ErrorLoggingFields** a été ajoutée pour contrôler les champs consignés dans le journal des erreurs http. Ces valeurs de Registre se trouvent sous une \\ clé de paramètres http située à l’emplacement suivant :

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
      Services
         HTTP
            Parameters
```

La valeur de Registre **ErrorLoggingFields** est une valeur DWORD qui contient des valeurs de bit pour chacun des champs pouvant être journalisés. Pour activer la journalisation d’un champ spécifique, définissez sa valeur de bit correspondante sur 1 et redémarrez le service HTTP. Pour désactiver la journalisation, définissez la valeur de bit sur 0. Pour configurer plusieurs champs, utilisez une opération or au niveau du bit des valeurs individuelles. Par exemple, pour activer les champs de journalisation des cookies et des référents, la valeur doit être 0x00020000 \| 0x00040000 = 0x00060000. Si la clé de Registre **ErrorLoggingFields** est absente, les champs par défaut sont journalisés. La valeur **ErrorLoggingFields** pour enregistrer les champs par défaut est 0x7c884c7. Pour activer la journalisation de tous les champs affichés dans le tableau ci-dessous, définissez la valeur sur 0x7dff4e7.

Les champs de journalisation des erreurs sont répertoriés dans le tableau suivant :



| Champ de journal            | Consigné par défaut | Valeur en bits  |
|----------------------|-------------------|------------|
| Date                 | Oui               | 0x00000001 |
| Temps                 | Oui               | 0x00000002 |
| Nom de l’ordinateur serveur | Non                | 0x00000020 |
| Adresse IP du client    | Oui               | 0x00000004 |
| Port client          | Oui               | 0x00400000 |
| Adresse IP du serveur    | Oui               | 0x00000040 |
| Port du serveur          | Oui               | 0x00008000 |
| Version du protocole     | Oui               | 0x00080000 |
| Méthode               | Oui               | 0x00000080 |
| URI                  | Oui               | 0x00800000 |
| User Agent           | Non                | 0x00010000 |
| Cookie               | Non                | 0x00020000 |
| référant             | Non                | 0x00040000 |
| Host                 | Non                | 0x00100000 |
| État du protocole      | Oui               | 0x00000400 |
| SC-Bytes             | Non                | 0x00001000 |
| CS-Bytes             | Non                | 0x00002000 |
| Durée           | Non                | 0x00004000 |
| SiteId               | Oui               | 0x01000000 |
| Phrase motif        | Oui               | 0x02000000 |
| Nom de la file d’attente           | Non                | 0x04000000 |
| ID de flux            | Non                | 0x ???????? |



 

## <a name="time-and-date-rollover"></a>Substitution d’heure et de date

Par défaut, un nouveau fichier journal des erreurs HTTP est créé (substitution de fichier terme) quand le fichier journal actuel atteint une taille spécifiée. à compter de Windows Server 2003 avec SP1, de nouveaux fichiers journaux des erreurs peuvent être créés en fonction de la date et de l’heure. Les substitutions de date et d’heure sont contrôlées par deux nouvelles valeurs de Registre : **ErrorLoggingRolloverType** et **ErrorLoggingLocaltimeRollover**. Pour permettre la substitution d’heure et de date, ces valeurs de Registre doivent être ajoutées au registre. Le service http doit être redémarré lorsque ces clés sont ajoutées au registre. Les clés de registre de substitution du fichier journal sont créées sous la clé suivante :

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

La clé de Registre **ErrorLoggingRolloverType** indique le type de substitution souhaité et est défini par défaut sur la substitution basée sur la taille. La substitution peut également être définie sur une base quotidienne, hebdomadaire, mensuelle ou horaire. Lorsque la substitution de fichier est basée sur le temps, une valeur **ErrorLoggingLocaltimeRollover** de 0 indique que l’heure de substitution est exprimée en GMT et une valeur de 1 indique que l’heure de substitution est exprimée en heure locale. La clé **ErrorLoggingRolloverType** peut prendre une valeur comprise entre 0 et 4, comme indiqué dans le tableau suivant.



| Valeur du type de substitution | Description                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 0                   | Substitution basée sur la taille. Les fichiers journaux sont restaurés lorsque le fichier atteint la taille définie dans la clé de Registre **ErrorLogFileTruncateSize** . |
| 1                   | La substitution du fichier journal a lieu quotidiennement.                                                                                                         |
| 2                   | La substitution du fichier journal se produit toutes les semaines.                                                                                                        |
| 3                   | La substitution du fichier journal a lieu tous les mois.                                                                                                       |
| 4                   | La substitution de fichier journal se produit toutes les heures.                                                                                                        |



 

Les conventions d’affectation de noms pour les fichiers qui stockent les journaux d’erreurs sont différentes pour la taille, la date et la substitution temporelle. Le tableau suivant répertorie les conventions d’affectation de noms pour les fichiers journaux http.



| Type Tollover | Nom du fichier journal  | Description                                                                                                                         |
|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Taille          | HTTPERRn. LOG   | Le fichier journal est recyclé lorsqu’il atteint une taille spécifique. n est le numéro de fichier et est incrémenté lorsque le fichier journal est restauré. |
| Quotidien         | htYYMMDD. log   | Le fichier journal est recyclé quotidiennement.                                                                                                     |
| Chaque semaine        | htYYMMww. log   | Le fichier journal est recyclé chaque semaine, où SS est la semaine du mois.                                                                 |
| Chaque mois       | htYYMM. log     | Le fichier journal est recyclé chaque mois.                                                                                               |
| Toutes les heures        | htYYMMDDhh. log | Le fichier journal est recyclé toutes les heures, où HH est l’heure du jour exprimée en notation de 0-24 heures.                                   |



 

 

 




