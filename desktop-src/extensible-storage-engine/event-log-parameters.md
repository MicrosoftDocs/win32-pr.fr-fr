---
description: En savoir plus sur les paramètres du journal des événements
title: Paramètres du journal des événements
TOCTitle: Event Log Parameters
ms:assetid: c660f555-2627-4d25-8f1c-8c1dc8a3a381
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294086(v=EXCHG.10)
ms:contentKeyID: 32765701
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a1c127f538ae80e8bec3dc5a34d5924b838b51ee
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465876"
---
# <a name="event-log-parameters"></a>Paramètres du journal des événements


_**S’applique à :** Windows | Windows Serveurs_

## <a name="event-log-parameters"></a>Paramètres du journal des événements

Cette rubrique contient des paramètres qui sont utilisés pour le journal des événements.

JET_paramEventLogCache  
Ce paramètre contrôle la taille (en octets) d’un cache de messages EventLog qui contiendra les messages EventLog émis par le moteur de base de données pendant l’arrêt du service EventLog. Ces messages mis en cache seront vidés dans le journal des événements lorsque le service devient opérationnel. Tous les messages qui dépassent le cache sont supprimés.


| | | <p>Valeur par défaut :</p> | <p>0</p> | | <p>Tapez :</p> | <p>Integer</p> | | <p>Plage valide :</p> | <p>0 – 2147483647</p> | | <p>Étendue :</p> | <p>Global</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>No</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Affecte la disposition physique :</p> | <p>No</p> | | <p>Affecte la fiabilité :</p> | <p>No</p> | | <p>Affecte les performances :</p> | <p>No</p> | | <p>Affecte les ressources :</p> | <p>Yes</p> | | <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramEventLoggingLevel*  
  
Ce paramètre configure le niveau de détail des messages EventLog émis dans le journal des événements par le moteur de base de données. Des numéros plus élevés entraînent des messages EventLog plus détaillés.


| | | <p>Valeur par défaut :</p> | <p>JET_EventLoggingLevelMax</p> | | <p>Tapez :</p> | <p>Integer</p> | | <p>Plage valide :</p> | <p>JET_EventLoggingDisable – JET_EventLoggingLevelMax</p> | | <p>Étendue :</p> | <p>Instance</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Affecte la disposition physique :</p> | <p>No</p> | | <p>Affecte la fiabilité :</p> | <p>No</p> | | <p>Affecte les performances :</p> | <p>No</p> | | <p>Affecte les ressources :</p> | <p>No</p> | | <p>Disponibilité :</p> | <p>Windows XP et versions ultérieures</p> | 



*JET_paramEventSource*  
4  

Ce paramètre fournit une chaîne spécifique à l’application qui sera ajoutée à tous les messages du journal des événements émis par le moteur de base de données. Cela permet de corréler facilement les messages du journal des événements avec l’application source. Si une chaîne vide est spécifiée (comme c’est le cas par défaut), le nom de l’exécutable de l’application hôte sera utilisé.


| | | <p>Valeur par défaut :</p> | <p>""</p> | | <p>Tapez :</p> | <p>String</p> | | <p>Plage valide :</p> | <p>0 – 259 caractères</p> | | <p>Étendue :</p> | <p>Instance</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Affecte la disposition physique :</p> | <p>No</p> | | <p>Affecte la fiabilité :</p> | <p>No</p> | | <p>Affecte les performances :</p> | <p>No</p> | | <p>Affecte les ressources :</p> | <p>No</p> | | <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramEventSourceKey*  
49  

Ce paramètre peut être utilisé pour contrôler le journal des événements que le moteur de base de données utilise pour ses messages de journal des événements. Par défaut, tous les messages du journal des événements sont envoyés dans le journal des événements de l’application. Si le nom de la clé de registre d’un autre journal des événements est configuré, les messages du journal des événements y seront à la place.


| | | <p>Valeur par défaut :</p> | <p>""</p> | | <p>Tapez :</p> | <p>String</p> | | <p>Plage valide :</p> | <p>0 – 259 caractères</p> | | <p>Étendue :</p> | <p>Instance</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Affecte la disposition physique :</p> | <p>No</p> | | <p>Affecte la fiabilité :</p> | <p>No</p> | | <p>Affecte les performances :</p> | <p>No</p> | | <p>Affecte les ressources :</p> | <p>No</p> | | <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramNoInformationEvent*  
50  

Lorsque ce paramètre a la valeur true, les messages du journal des événements d’information qui seraient normalement générés par le moteur de base de données seront supprimés.


| | | <p>Valeur par défaut :</p> | <p>Faux</p> | | <p>Tapez :</p> | <p>Boolean</p> | | <p>Plage valide :</p> | <p>False, True</p> | | <p>Étendue :</p> | <p>Instance</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Affecte la disposition physique :</p> | <p>No</p> | | <p>Affecte la fiabilité :</p> | <p>No</p> | | <p>Affecte les performances :</p> | <p>No</p> | | <p>Affecte les ressources :</p> | <p>No</p> | | <p>Disponibilité :</p> | <p>Tous</p> | 



### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
