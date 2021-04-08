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
ms.openlocfilehash: 912dc3e1e8588e18ef0d1db8fbf7edccfca7bdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034695"
---
# <a name="event-log-parameters"></a>Paramètres du journal des événements


_**S’applique à :** Windows | Serveur Windows_

## <a name="event-log-parameters"></a>Paramètres du journal des événements

Cette rubrique contient des paramètres qui sont utilisés pour le journal des événements.

JET_paramEventLogCache  
Ce paramètre contrôle la taille (en octets) d’un cache de messages EventLog qui contiendra les messages EventLog émis par le moteur de base de données pendant l’arrêt du service EventLog. Ces messages mis en cache seront vidés dans le journal des événements lorsque le service devient opérationnel. Tous les messages qui dépassent le cache sont supprimés.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>0 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Tous</p></td>
</tr>
</tbody>
</table>


*JET_paramEventLoggingLevel*  
  
Ce paramètre configure le niveau de détail des messages EventLog émis dans le journal des événements par le moteur de base de données. Des numéros plus élevés entraînent des messages EventLog plus détaillés.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>JET_EventLoggingLevelMax</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>JET_EventLoggingDisable – JET_EventLoggingLevelMax</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Instance</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Windows XP et versions ultérieures</p></td>
</tr>
</tbody>
</table>


*JET_paramEventSource*  
4  

Ce paramètre fournit une chaîne spécifique à l’application qui sera ajoutée à tous les messages du journal des événements émis par le moteur de base de données. Cela permet de corréler facilement les messages du journal des événements avec l’application source. Si une chaîne vide est spécifiée (comme c’est le cas par défaut), le nom de l’exécutable de l’application hôte sera utilisé.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>String</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>0 – 259 caractères</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Instance</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Tous</p></td>
</tr>
</tbody>
</table>


*JET_paramEventSourceKey*  
49  

Ce paramètre peut être utilisé pour contrôler le journal des événements que le moteur de base de données utilise pour ses messages de journal des événements. Par défaut, tous les messages du journal des événements sont envoyés dans le journal des événements de l’application. Si le nom de la clé de registre d’un autre journal des événements est configuré, les messages du journal des événements y seront à la place.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>String</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>0 – 259 caractères</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Instance</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Tous</p></td>
</tr>
</tbody>
</table>


*JET_paramNoInformationEvent*  
50  

Lorsque ce paramètre a la valeur true, les messages du journal des événements d’information qui seraient normalement générés par le moteur de base de données seront supprimés.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>Faux</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Instance</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Tous</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
