---
description: 'En savoir plus sur les paramètres suivants : informations'
title: Paramètres d’information
TOCTitle: Informational Parameters
ms:assetid: 48500fc9-6d89-45b8-92ad-afb997b729f3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269241(v=EXCHG.10)
ms:contentKeyID: 32765543
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
ms.openlocfilehash: a8923b544726e474775684f54fed47d8b4ba281e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753317"
---
# <a name="informational-parameters"></a>Paramètres d’information


_**S’applique à :** Windows | Serveur Windows_

## <a name="informational-parameters"></a>Paramètres d’information

Cette rubrique contient des paramètres utilisés pour exposer des informations sur le moteur de base de données.

*JET_paramKeyMost*  
134  

Ce paramètre en lecture seule indique la longueur de clé d’index maximale autorisée qui peut être sélectionnée pour la taille de page de la base de données actuelle (telle que configurée par JET_paramDatabasePageSize).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>JET_cbKeyMost4KBytePage</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>255 – 65535</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>N/A</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>N/A</p></td>
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
<td><p>À compter de Windows Server 2008 et Windows Vista</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxColtyp*  
131  

Ce paramètre en lecture seule retourne la [JET_COLTYP](./jet-coltyp.md) maximale (JET_coltypMax) pour cette version du moteur de base de données. Cette valeur peut être utilisée pour tester la prise en charge d’un [JET_COLTYP](./jet-coltyp.md)spécifique. Si un [JET_COLTYP](./jet-coltyp.md) donné est inférieur à la valeur de ce paramètre, il est pris en charge par le moteur de base de données.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>JET_coltypUnsignedShort + 1</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>0 – 255</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>N/A</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>N/A</p></td>
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
<td><p>À compter de Windows Server 2008 et Windows Vista</p></td>
</tr>
</tbody>
</table>


*JET_paramLVChunkSizeMost*  
163  

Paramètre en lecture seule qui retourne la taille de segment de valeur longue en fonction de la taille de page configurée. Si une valeur long doit être lue ou écrite avec plusieurs appels de colonne jet {set, Retrieve}, l’utilisation d’une mémoire tampon dont la taille est un multiple de la taille de segment est plus efficace.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>2 ko page = 1966 octets<br />
4 ko page = 4014 octets<br />
8 ko page = 8110 octets<br />
16 ko page = 4050 octets<br />
32KO page = 8150 octets</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>0-10000</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p></p></td>
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
<td><p>Nécessite Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008.</p></td>
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
[JET_COLTYP](./jet-coltyp.md)
