---
description: 'En savoir plus sur : paramètres de cache de base de données'
title: Paramètres du cache de base de données
TOCTitle: Database Cache Parameters
ms:assetid: 715e5495-0cd8-430f-bf21-509cf03bfbfd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269293(v=EXCHG.10)
ms:contentKeyID: 32765585
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
ms.openlocfilehash: 77d83ea8998da7c00fd294f81b94099d23d524e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543469"
---
# <a name="database-cache-parameters"></a>Paramètres du cache de base de données


_**S’applique à :** Windows | Serveur Windows_

## <a name="database-cache-parameters"></a>Paramètres du cache de base de données

Cette rubrique contient des paramètres qui sont utilisés pour le cache de base de données.

*JET_paramBatchIOBufferMax*  
22  

Ce paramètre contrôle la taille d’une partie auxiliaire du cache des pages de base de données qui est utilisé pour simuler des e/s de regroupement de nuages de points lorsqu’il n’est pas disponible. La taille est dans les pages de base de données.

**Windows XP et versions ultérieures :**  Ce paramètre est obsolète et n’affecte pas le fonctionnement du moteur de base de données.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>256</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>0, 2 – 2147483647</p></td>
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
<td><p>Oui</p></td>
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


*JET_paramCacheSize*  
41  

Ce paramètre peut être utilisé pour contrôler la taille du cache de la page de base de données au moment de l’exécution. En règle générale, le cache ajuste automatiquement sa taille en fonction des niveaux d’activité de la base de données et de l’ordinateur. Si l’application définit ce paramètre sur zéro, le cache ajuste sa propre taille de cette manière. Toutefois, si l’application définit ce paramètre sur une valeur différente de zéro, le cache s’ajuste à cette taille cible (dans les pages de base de données). Le cache conserve sa taille à ce seuil jusqu’à ce qu’une nouvelle taille soit donnée ou jusqu’à ce qu’il soit relâché pour choisir sa propre taille.

**Remarque**  La taille du cache est toujours soumise aux limites imposées par **JET_paramCacheSizeMin** et **JET_paramCacheSizeMax**.

Lorsque ce paramètre est lu, la taille réelle du cache dans les pages de la base de données est retournée. Cette taille peut être utilisée par l’application comme entrée pour conduire son ajustement manuel de la taille du cache.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>Spécial</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p><strong>Windows 2000 :</strong>  1 – 1048575</p>
<p><strong>Windows XP :</strong>  1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Oui</p></td>
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
<td><p>Oui</p></td>
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


*JET_paramCacheSizeMin*  
60  

Ce paramètre configure la taille minimale du cache des pages de base de données. La taille est dans les pages de base de données.

Par défaut, le cache de base de données ajuste automatiquement sa taille entre les limites définies par **JET_paramCacheSizeMin** et **JET_paramCacheSizeMax**.

**Windows 2000 :**  Sur Windows 2000, ce paramètre doit être défini sur une valeur à peu près égal à quatre fois le nombre de threads qui se trouveront à l’intérieur de l’API ESE en même temps. Cela est nécessaire pour éviter les blocages provoqués par un nombre insuffisant de tampons de cache de pages de base de données pour effectuer des opérations complexes telles que les fractionnements d’arborescences B +.

**Windows XP et versions ultérieures :**  Le gestionnaire de cache définit automatiquement sa propre taille de cache minimale pour éviter les interblocages.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p><strong>Windows 2000 :</strong>  64</p>
<p><strong>Windows XP :</strong>  1</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p><strong>Windows 2000 :</strong>  1 – 1048575</p>
<p><strong>Windows XP :</strong>  1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p><strong>Windows 2000 :</strong>  º</p>
<p><strong>Windows XP :</strong>  Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p><strong>Windows 2000 :</strong>  º</p>
<p><strong>Windows XP :</strong>  Oui</p></td>
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
<td><p>Oui</p></td>
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


*JET_paramCacheSizeMax*  
23  

Ce paramètre configure la taille maximale du cache des pages de base de données. La taille est dans les pages de base de données.

Par défaut, le cache de base de données ajuste automatiquement sa taille entre les limites définies par **JET_paramCacheSizeMin** et **JET_paramCacheSizeMax**.

**Remarque**   Si ce paramètre est laissé à sa valeur par défaut, la taille maximale du cache sera définie sur la taille de la mémoire physique lors de l’appel de [JetInit](./jetinit-function.md) .

**Windows Vista :**  À compter de Windows Vista, la valeur par défaut de ce paramètre a été modifiée pour clarifier ce comportement.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong>  512</p>
<p><strong>Windows Vista :</strong>  2 milliards</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p><strong>Windows 2000 :</strong>  1 – 1048575</p>
<p><strong>Windows XP :</strong>  1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p><strong>Windows 2000 :</strong>  º</p>
<p><strong>Windows XP :</strong>  Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p><strong>Windows XP et windows 2000 :</strong>  º</p>
<p><strong>Windows Vista et Windows Server 2003 :</strong>  Oui</p></td>
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
<td><p>Oui</p></td>
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


*JET_paramCheckpointDepthMax*  
24 

Ce paramètre contrôle le vidage des pages de base de données à partir du cache des pages de base de données afin de réduire le temps nécessaire à la récupération d’un incident. Le paramètre est un seuil en octets pour le nombre de fichiers journaux des transactions qui doivent être relus après un incident.

Si l’enregistrement circulaire est activé à l’aide de [JET_paramCircularLog](./transaction-log-parameters.md) , ce paramètre contrôle également la quantité approximative de fichiers du journal des transactions qui seront conservés sur le disque.

Il est important que ce paramètre ne soit pas défini trop bas. Étant donné que la valeur de ce paramètre est proche de zéro, le cache devient de plus en plus agressif lors du vidage des pages de base de données sur le disque. Cela aboutit non seulement à un nombre accru d’écritures dans les fichiers de base de données, mais aussi à un nombre accru de lectures dans ces fichiers. Cela peut entraîner des problèmes de performances très importants dans certains cas. Malheureusement, la définition de la plus petite valeur optimale pour ce paramètre ne peut être effectuée qu’à l’aide de l’expérimentation avec l’application cible.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>20971520</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong>  0 – 2147483647</p>
<p><strong>Windows Vista :</strong>  Toutes les valeurs</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong> Ce paramètre est global.</p>
<p><strong>Windows Vista :</strong>  Ce paramètre est par instance.</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Oui</p></td>
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


*JET_paramCheckpointIOMax*  
135  

Ce paramètre contrôle le nombre maximal d’écritures simultanées que le moteur de base de données utilisera pour vider les pages modifiées de la base de données dans le but d’avancer le point de contrôle. La valeur de ce paramètre peut être utilisée pour équilibrer la vitesse à laquelle le point de contrôle peut être avancé par rapport à l’impact négatif que ce processus aura sur le temps de réponse pour les autres opérations d’e/s sur les disques contenant la base de données.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>96</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>8 – 1024</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Oui</p></td>
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
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Windows Vista et versions ultérieures</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableViewCache*  
127  

Lorsque ce paramètre a la **valeur true**, le moteur de base de données utilise les données de base de données directement à partir du cache de fichiers Windows au lieu de copier les données mises en cache dans sa propre mémoire privée. Toutes les données de base de données modifiées seront toujours mises en cache dans la mémoire privée.

L’objectif de ce mode est de réduire davantage la quantité de mémoire privée utilisée par le moteur de base de données pour mettre en cache les données de la base de données.

Le cache de vue ne peut être utilisé que si l’utilisation du cache de fichiers Windows est activée en affectant à JET_paramEnableFileCache la **valeur true**.

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
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Windows Vista et versions ultérieures</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKCorrInterval*  
25  

Ce paramètre définit l’intervalle de temps, en microsecondes, pendant lequel deux accès à une page de base de données sont considérés comme corrélés. Cet intervalle de corrélation contrôle la sensibilité de l’algorithme de remplacement de page (LRU-K) du cache aux accès aux pages successives. Cela affecte à son tour les pages qu’il choisit de conserver en cache.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>128000</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p><strong>Windows 2000, Windows XP et Windows Server 2003 : </strong>    0 – 2147483647</p>
<p><strong>Windows Vista :</strong>  Toutes les valeurs</p></td>
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
<td><p>Oui</p></td>
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


*JET_paramLRUKHistoryMax*  
26  

Ce paramètre définit le nombre maximal de pages de base de données non mises en cache pour lesquelles les heures d’accès à la page de base de données sont conservées. Ces enregistrements d’historique permettent à l’algorithme de remplacement de page (LRU-K) du cache de détecter plus précisément les pages populaires qui ont été supprimées incorrectement dans le cache des pages de base de données.

**Windows XP et Windows Server 2003 :**  Ce paramètre est ignoré sur Windows XP et Windows Server 2003 et n’affecte pas le fonctionnement du moteur de base de données.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p><strong>Windows 2000 :</strong>  1024</p>
<p><strong>Windows Vista :</strong>  100000</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p><strong>Windows 2000 :</strong>  0 – 4194303</p>
<p><strong>Windows Vista :</strong>  Toutes les valeurs</p></td>
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
<td><p>Oui</p></td>
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


*JET_paramLRUKPolicy*  
27  

Ce paramètre configure le nombre d’accès à la page de base de données qui sont pris en compte pour déterminer l’utilité de la page. Ce paramètre est essentiellement le K dans LRU-K, l’algorithme de remplacement de page du cache de page de la base de données.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>1-2</p></td>
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
<td><p>Oui</p></td>
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


*JET_paramLRUKTimeout*  
28

Ce paramètre indique la durée, en secondes, au terme de laquelle une page du cache de la page de base de données est considérée comme ayant perdu un accès à la page dans le but d’évaluer l’utilité de la page.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>100</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong>  1 – 2147483647</p>
<p><strong>Windows Vista :</strong>   1 – 4294967295</p></td>
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
<td><p>Oui</p></td>
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


*JET_paramLRUKTrxCorrInterval*  
29  

Ce paramètre est obsolète et n’affecte pas le fonctionnement du moteur de base de données.

*JET_paramStartFlushThreshold*  
31  

Ce paramètre contrôle le moment où le cache de la page de base de données commence à supprimer des pages du cache pour libérer de l’espace pour les pages qui ne sont pas mises en cache. Lorsque le nombre de tampons de page dans le cache descend sous ce seuil, un processus en arrière-plan est démarré pour réapprovisionner ce pool de mémoires tampons disponibles. Ce seuil est toujours relatif à la taille maximale du cache définie par **JET_paramCacheSizeMax**. Ce seuil doit également toujours être inférieur au seuil d’arrêt défini par **JET_paramStopFlushThreshold**.

La hauteur de distance du seuil de démarrage détermine le temps de réponse que le cache de page de la base de données doit avoir pour produire des tampons disponibles avant que l’application en ait besoin. Un seuil de démarrage élevé donnera plus de temps au processus en arrière-plan. Toutefois, un seuil de démarrage élevé implique un seuil d’arrêt plus élevé et réduit la taille effective du cache des pages de base de données pour les pages modifiées (Windows 2000) ou pour toutes les pages (Windows XP et versions ultérieures).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong>  5 (1%)</p>
<p><strong>Windows Vista :</strong>  20 millions (1%)</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p><strong>Windows 2000 :</strong>  1 – 1048575</p>
<p><strong>Windows XP :</strong>  1 – 4294967295</p>
<p><strong>Windows Vista :</strong>  Toutes les valeurs</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Oui</p></td>
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
<td><p>Oui</p></td>
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


*JET_paramStopFlushThreshold*  
32  

Ce paramètre contrôle le moment où le cache de la page de base de données met fin à la suppression des pages du cache pour libérer de l’espace pour les pages qui ne sont pas mises en cache. Lorsque le nombre de tampons de page dans le cache dépasse ce seuil, le processus en arrière-plan qui a démarré pour réapprovisionner ce pool de mémoires tampons disponibles est arrêté. Ce seuil est toujours relatif à la taille maximale du cache définie par **JET_paramCacheSizeMax**. Ce seuil doit également être toujours supérieur au seuil de démarrage défini par **JET_paramStartFlushThreshold**.

La distance entre le seuil de démarrage et le seuil d’arrêt affecte l’efficacité avec laquelle les pages de base de données sont vidées par le processus en arrière-plan. Un plus grand fossé rendra plus probable l’Association des écritures aux pages voisines. Toutefois, un seuil d’arrêt élevé réduira la taille effective du cache des pages de base de données pour les pages modifiées (Windows 2000) ou pour toutes les pages (Windows XP et versions ultérieures).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong>  10 (2%)</p>
<p><strong>Windows Vista :</strong>  40 millions (2%)</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p><strong>Windows 2000 :</strong>  1 – 1048575</p>
<p><strong>Windows XP :</strong>  1 – 4294967295</p>
<p><strong>Windows Vista :</strong>  Toutes les valeurs</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Oui</p></td>
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
<td><p>Oui</p></td>
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
