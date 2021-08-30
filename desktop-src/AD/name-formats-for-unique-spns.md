---
title: Formats de noms pour les SPN uniques
description: Un nom principal de service doit être unique dans la forêt dans laquelle il est enregistré.
ms.assetid: dd3f9f7c-b64c-4bd8-924f-a8880ee3b71e
ms.tgt_platform: multiple
keywords:
- Formats de noms pour les noms de principal du service (SPN) uniques
- Nom du principal du service AD, formats de noms pour
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5f135f0aa9bc7199e7b5338b94479f2a20d5b11
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881285"
---
# <a name="name-formats-for-unique-spns"></a>Formats de noms pour les SPN uniques

Un nom principal de service doit être unique dans la forêt dans laquelle il est enregistré. S’il n’est pas unique, l’authentification échoue. La syntaxe du SPN comporte quatre éléments : deux éléments obligatoires et deux éléments supplémentaires que vous pouvez utiliser, si nécessaire, pour produire un nom unique comme indiqué dans le tableau suivant.


```C++
<service class>/<host>:<port>/<service name>
```






| Élément | Description | 
|---------|-------------|
| "<service class>" | Chaîne qui identifie la classe générale du service ; par exemple, « SqlServer ». Il existe des noms de classe de service bien connus, tels que « www » pour un service Web ou « LDAP » pour un service d’annuaire. En général, il peut s’agir de n’importe quelle chaîne propre à la classe de service. Sachez que la syntaxe du SPN utilise une barre oblique (/) pour séparer les éléments, de sorte que ce caractère ne peut pas figurer dans un nom de classe de service. | 
| « &lt; hôte &gt; » | Nom de l’ordinateur sur lequel le service est en cours d’exécution. Il peut s’agir d’un nom DNS complet ou d’un nom NetBIOS. Sachez qu'il n'existe aucune garantie que les noms NetBIOS soient uniques dans une forêt ; par conséquent, un SPN qui contient un nom NetBIOS peut ne pas être unique. | 
| « &lt; port &gt; » | Numéro de port facultatif permettant de faire la distinction entre plusieurs instances de la même classe de service sur un seul ordinateur hôte. Omettez ce composant si le service utilise le port par défaut pour sa classe de service. | 
| "<service name>" | Nom facultatif utilisé dans les noms de principal du service d’un service réplicable pour identifier les données ou services fournis par le service ou le domaine pris en charge par le service. Ce composant peut avoir l’un des formats suivants :<ul><li>Nom unique ou objectGUID d’un objet dans Active Directory Domain Services, tel qu’un point de connexion de service (SCP).</li><li>Nom DNS du domaine pour un service qui fournit un service spécifié pour un domaine dans son ensemble.</li><li>Nom DNS d’un enregistrement SRV ou MX.</li></ul> | 




 

Les composants présents dans les SPN d’un service dépendent de la façon dont le service est identifié et répliqué. Il existe deux scénarios de base : les services basés sur l’hôte et les services réplicables.

## <a name="host-based-services"></a>Services basés sur l’hôte

Pour un service basé sur l’hôte, le &lt; composant « nom du service &gt; » est omis, car le service est identifié de manière unique par la classe de service et par le nom de l’ordinateur hôte sur lequel le service est installé.


```C++
<service class>/<host>
```



La classe de service seule est suffisante pour identifier les fonctionnalités fournies par le service pour les clients. Vous pouvez installer des instances de la classe de service sur de nombreux ordinateurs et chaque instance fournit des services identifiés avec son ordinateur hôte. FTP et Telnet sont des exemples de services basés sur l’hôte. Les noms principaux de service d’une instance de service basée sur l’hôte peuvent inclure le numéro de port si le service utilise un port autre que celui par défaut ou s’il existe plusieurs instances du service sur l’ordinateur hôte.


```C++
<service class>/<host>:<port>
```



## <a name="replicable-services"></a>Services réplicables

Pour un service réplicable, il peut y avoir une ou plusieurs instances du service (réplicas), et les clients ne différencient pas le réplica auquel ils se connectent, car chacun fournit le même service. Les SPN pour chaque réplica ont les mêmes « &lt; classe de service &gt; » et « &lt; nom de service &gt; », où « &lt; nom &gt; de service » identifie plus précisément les fonctionnalités fournies par le service. Seuls les &lt; composants « host &gt; » et « &lt; port » facultatifs &gt; varient d’un SPN à l’autres.


```C++
<service class>/<host>:<port>/<service name>
```



Par exemple, un service réplicable est une instance d’un service de base de données qui permet d’accéder à une base de données spécifiée. Dans ce cas, « &lt; classe &gt; de service » identifie l’application de base de données et « &lt; nom &gt; du service » identifie la base de données spécifique. « &lt; nom &gt; du service » peut être le nom unique d’un point de connexion de service (SCP) contenant les données de connexion de la base de données.


```C++
MyDBService/host1.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
```



Si les clients utilisent le nom NetBIOS pour composer le SPN d’un service, chaque réplica doit également inscrire un SPN contenant le nom NetBIOS.


```C++
MyDBService/host1/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3/CN=hrdb,OU=mktg,DC=example,DC=com
```



Un autre exemple de service réplicable est un service qui fournit des services à un domaine entier. Dans ce cas, le &lt; composant « nom du service &gt; » est le nom DNS du domaine pris en charge. Un KDC Kerberos est un exemple de ce type de service réplicable.

Sachez que si le nom DNS d’un ordinateur change, le système met à jour l' &lt; élément « host &gt; » pour tous les noms de principal du service (SPN) inscrits pour cet ordinateur hôte dans la forêt.

 

 




